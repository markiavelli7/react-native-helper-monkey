# Re-using Styles in React Native

There are two different ways to pass styles to components:

1. Create a default component with the styles that we want and then extend them
2. Create a global stylesheet and then extend the styles to the components that need them

## Create a Body Text Component

Extend the Body Text Component as our default <Text> component

## Set Up a Default StyleSheet

**default-styles.js**

```javascript
import {StyleSheet} from 'react-native'

export default StyleSheet.create({
  bodyText: {
    fontFamily: 'openSans-bold',
    color: 'red'
  }
})
```

Then to use it:

**exampleFile.js**

```javascript
import GlobalStyles from '../../utils/default-styles'

...
return (
  <Text style={[GlobalStyles.bodyText]}>...</Text>
)
```