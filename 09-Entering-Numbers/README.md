# Numbers in <TextInput />

The *keyboardType* allows us to set numbers in a couple of different ways:

- **numeric**: Allows for us to enter decimals in with our input
- **number-pad**: On iOS removes the option to allow us to enter decimals. On android, it is still possible to enter decimals, so if we strictly need numbers, we need to use a regular expression to sanitize the input:

```javascript
function numberInputHandler(inputText) {
  setEnteredValue(inputText.replace(/[^0-9]/g, ''));
}
```