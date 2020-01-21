# Flexible Styling

If it is possible, we can hardcode our styling to account for variations in screen sizes:

```javascript
inputContainer: {
  alignItems: 'center',
  width: '90%',
  minWidth: 300,
  maxWidth: '95%',
},
```

In the above code, we are setting a width of 90% with a min-width of 300 attached and a max-width of 95%. If our device is smaller than 300px, then our max-width property will take over and not let the width go past 95%.

# The Dimensions API

```javascript
import {Dimensions} from 'react-native'
```

**Dimensions** is an object that allows us to find out how much width we have available:

```javascript
button: {
  width: Dimensions.get(window)
}
```

The **Dimensions.get()** method will let us get dimensions of the window or the screen. The difference is that on Android if we use window, the status bar height will be excluded from the calculation. This is usually the behavior that we want, so window is a better choice because it will work how we expect on iOS and Android.


## Dimensions 'if' Checks

```javascript
function marginTop(height) {
  if (height > 600) {
    return 10;
  } else {
    return 2.5;
  }
}

buttonContainer: {
  marginTop: marginTop(Dimensions.get('window').height),
},
```

## Calculating Sizes Dynamically

```javascript
imageContainer: {
  width: Dimensions.get('window').height * 0.4,
  height: Dimensions.get('window').height * 0.4,
  borderRadius: Dimensions.get('window').height + * 0.2,
}
```

## KeyboardAvoidingView

Adding this ReactNative component as a wrapper for our screen will ensure that the keyboard never covers up the text input:

```javascript
<KeyboardAvoidingView behavior="position" keyboardVerticalOffset={30}>
  <TouchableWithoutFeedback></TouchableWithoutFeedback>
</KeyboardAvoidingView>
```