# Scrolling

Scrolling is not automatically given to us in React Native, we have to be explicit if we want our display to be able to scroll.

## <ScrollView />

We could have the main layout be a <ScrollView> so that the whole screen is scrollable, but it is very common to just have the container for the items that overflow be scrollable. All depends on what the layout is looking for.

A *ScrollView* is not always the best option, it will automatically fully render all of the child element inside of it, even the ones that are not in view on every render. If we had hundreds or thousands of elements, all of the elements will be fully rendered. This can be quite costly in terms of performance.