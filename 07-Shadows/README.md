# Box Shadows

## iOS

Four properties are required to get a box shadow working or iOS:

```javascript
shadowColor: 'black',
shadowOffset: {height: 2, width: 0},
shadowRadius: 6,
shadowOpacity: 0.26,
```

## Android

On Android, we have to use the elevation property:

```javascript
elevation: 5,
```

We don't have as much control, but we get the default Material Design styling.