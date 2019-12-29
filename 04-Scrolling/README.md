# Scrolling

Scrolling is not automatically given to us in React Native, we have to be explicit if we want our display to be able to scroll.

## <ScrollView />

We could have the main layout be a <ScrollView> so that the whole screen is scrollable, but it is very common to just have the container for the items that overflow be scrollable. All depends on what the layout is looking for.

A *ScrollView* is not always the best option, it will automatically fully render all of the child element inside of it, even the ones that are not in view on every render. If we had hundreds or thousands of elements, all of the elements will be fully rendered. This can be quite costly in terms of performance.

### If we want to control the width or the height of our ScrollView or items in the ScrollView, we want to wrap the ScrollView in a View and set styles there:

```javascript
<View style={styles.list}>
  <ScrollView>
    {pastGuesses.map(guess => {
      return renderListItem(guess);
    })}
  </ScrollView>
</View>
```

For a **ScrollView** nested inside of a **View** to operate properly on Android, the **View** holding the **ScrollView** will need a style property of **flex: 1**.


**ScrollView** is a flex container, but it has a special way to style it in addition to setting the *style* prop, as the *style* prop doesn't let us style everything.

## contentContainerStyle

Available on **FlatList** and **ScrollView**.

```javascript
<ScrollView contentContainerStyle={}>
  ...
</ScrollView>
```

