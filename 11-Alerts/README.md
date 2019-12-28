# Alerts

**Alert** is another API that React Native provides us. We import it from React Native and then this is how we can use it:

```javascript
Alert.alert()
```

Alert takes three main options:

1. *String*: this is the title at the top of the alert box
2. *String*: this is the message that is shown in the alert box
3. *Array of Objects*: Each JS object represents a button and has *onPress*, *style*, and *text* properties that control how the button displays and what it does.

The **style** prop has only one of three style options: *cancel*, *default*, or *destructive*. This controls the button coloring within the alert.

### Opening up an Alert when there is a Keyboard Active will cause strange things to happen with the keyboard.