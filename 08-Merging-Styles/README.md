# Merging Styles

Sometimes we want to create a component that we want to extend that we may also want to add some custom styling to:

```javascript
import React from 'react';
import {View, StyleSheet} from 'react-native';

function Card({children, style = {}}) {
  return <View style={{...styles.card, ...style}}>{children}</View>;
}

export default Card;

var styles = StyleSheet.create({
  card: {
    shadowColor: 'black',
    shadowOffset: {height: 2, width: 0},
    shadowRadius: 6,
    shadowOpacity: 0.26,
    backgroundColor: 'white',
    elevation: 5,
    padding: 20,
    borderRadius: 10,
  },
});
```

In the above code, we use some ES6 destructuring to destructure all of the styles that we pass in through *styles.card* as individual properties. We then also destructure the style object if we pass in a style object through the component using our Card component. Example customization:

```javascript
<Card style={styles.inputContainer}>
...
</Card>

var styles = StyleSheet.create({
  inputContainer: {
    alignItems: 'center',
    width: 300,
    maxWidth: '80%',
  },
});
```

The *styles.inputContainer* object will be passed through to the card component, destructured, and added to the styles object. Because it is added after the initial styles, if there are any duplicate declarations, the styles that are passed in last will be used.

