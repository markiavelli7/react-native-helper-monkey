# Adding Fonts to a React Native Project

## Step One - Add the Fonts to the Project

At the root of the project, create an assets folder with a fonts sub-folder. Add each individual font that we need here (.ttf format).

## Step Two - Add a React Native Config File to the Project

At the root of the project we want to add this file that will point to where our assets are.

**react-native.config.js**

```javascript
module.exports = {
  assets: ['./assets/fonts'],
};
```

## Step Three - Run the React Native Link Command

```bash
yarn react-native link
```

This step takes the fonts in the /assets/fonts folder and adds them to our *Info.plist* file for iOS and creates the proper fonts directory for Android.

## Step Four - iOS Specific Commands

1. Open up the project workspace in XCode.
2. Find the Fonts in the Resources folder and select them all. In the right toolbar, there will be a **Target Membership** section. Make sure that the all of the boxes are checked for the app that we are running.
3. Double check that the fonts are included in the **Build Phases > Copy Bundle Resources Section**
4. From the Build Phases menu, delete the Info.plist file from all of the **Targets. If this isn't done, the build phase will find two Info.plist files and cause the build to fail.**

## Helpful iOS Article on Adding Fonts:

[Common Mistakes When Adding Fonts to Your iOS App](https://codewithchris.com/common-mistakes-with-adding-custom-fonts-to-your-ios-app/)