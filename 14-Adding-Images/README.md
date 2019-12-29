# Adding Images

React Native ships with an **Image** component that we can extend to display images.

### The source prop lets us add either a locally sourced image from our project or an image from the web:

## Locally Sourced

```javascript
<Image source={require('../../assets/images/success.jpeg')} />
```

Behind the scenes, React Native loads the image and does optimizations.

## Remote Images

We pass in an object that has a uri proprety that holds a string that points to the domain of the image.

```javascript
<Image source={{uri: 'https://...'}} />
```

For a locally loaded image **we don't have to set the width and height of our image.** But for a remote image, React Native can't determine the width and height of an image before it is loaded. Therefore, **for network images, we always have to set a width and height.**

## Styling Images

We can add our own styling object:

```javascript
image: {
  width: '95%',
  height: 300,
  marginVertical: 20,
},
```

### If our image dimensions don't match our device dimensions, the Image tag gives us a resizeMode property to adjust the image accordingly. 'cover' is the default.

## To do fancy things like shadows and rounded edges, we will want to wrap the image in a View and then style the image container:

```javascript
<View style={styles.imageContainer}>
  <Image
    style={styles.image}
    source={require('../../assets/images/success.jpeg')}
  />
</View>


var styles = StyleSheet.create({
  container: {
    flex: 1,
    alignItems: 'center',
    justifyContent: 'center',
  },
  imageContainer: {
    width: '75%',
    marginVertical: 20,
    height: 300,
    alignItems: 'center',
    borderRadius: 250,
    borderColor: 'black',
    borderWidth: 1,
    overflow: 'hidden',
  },
  image: {
    width: '100%',
    height: '100%',
  },
});
```