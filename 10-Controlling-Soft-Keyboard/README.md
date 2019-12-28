# Controlling the Soft Keyboard

On iOS, if we enter the soft keyboard, we can't really close it. To be able to close it, we want to wrap our entire screen with a special component:

## <TouchableWithoutFeedback>

*TouchableWithoutFeedback* allows us to register a touch listener without providing any feedback. We want to wrap our entire screen that will open the soft keyboard with it. Then we can listen for a click event on the screen. If the user clicks outside of the keyboard, we are then able to close the keyboard.

```javascript
return (
  <TouchableWithoutFeedback onPress={() => Keyboard.dismiss()}>
    ...
  </ TouchableWithoutFeedback>
)
```

We are making use of another special React API above: **Keyboard**. *Keyboard* lets us interact with the native device and control the soft keyboard.