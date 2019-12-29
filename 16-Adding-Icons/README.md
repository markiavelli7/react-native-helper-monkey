# Adding Icons

## Step One - Install the Dependencies

```bash
yarn add react-native-vector-icons
```

## Step Two - Link the Icons to iOS and Android

### iOS

1. Add the following code to the Podfile:

```javascript
pod 'RNVectorIcons', :path => '../node_modules/react-native-vector-icons'
```

2. Run **pod update**

3. **For iOS**: Go into the project and verify that the icons are in the Info.plist file and verify that the App and its test file are checked in the Target Membership section in the right toolbar.

Inside of **Build Phases > Copy Bundle Resources:**

**Delete the info.plist file from all of the TARGET build lists if they exists. If they are not deleted, they will throw an error during the build phase.**