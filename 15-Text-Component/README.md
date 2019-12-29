# The Text Component

We can wrap **Text** components in **Text** components. This lets us target specific text with special styling properties:

```javascript
<Text style={[GlobalStyles.bodyText]}>
  Number of Rounds:{' '}
  <Text style={[GlobalStyles.bodyText, styles.highlight]}>
    {numberOfRounds}
  </Text>
</Text>
```

Interestingly, the nested **Text** component will inherit its styles from the **Text** component that wraps it.

## Text Wrapping

By default, if Text is too large to fit on one line, it will wrap to another line. If we want to disable this wrapping behaviour, we can set the *numberOfLines* prop with the *ellipsizeMode* to truncate instead of wrap.