# Adding Icons

## Step One - Install the Dependencies

```bash
yarn add react-native-vector-icons
```

## Step Two - Link the Icons to iOS and Android

### iOS

1. Add a new folder at the root of the project called assets. Inside of this folder, create another folder to hold the *.ttf* icon files. Call this folder **icons** or something similar.

2. Add the *.ttf* files from the *node_modules/react-native-vector-icons* **Fonts** folder to our newly created *assets/icons* folder.

3. At the root of the project, create a new file called **react-native.config.js**. Inside of this file, add the following code:

```javascript
module.exports = {
  assets: [
    './assets/icons', 
    './assets/fonts'
  ]
}
```

NOTE: we are assuming that the assets folder will also contain another directory called *fonts* that will hold all of the *.ttf* files for all of the different fonts that we want to use in our project.

We are going to use the *react-native link* command to link our assets to the project

```bash
yarn react-native link
```

**This will link our assets in the icons and fonts folders to our React Native project.**

4. Go into the Xcode project and verify that all of the assets in the *icons* and *fonts* folders have been successfully added to the newly created **Resources** folder.

Also verify that all of the assets are included in the *info.plist* file.

3. Recompile the project. **If the build fails with an error about multiple info.plist files or duplicates of the .ttf files, go into the Project Build Phases/Copy Bundle Resources section and delete the info.plist file. This will need to be done in the main app and the tvOS app as well.** NOTE: deleting the files from the Copy Bundle Resources section may cause the App and tvOSApp to become unchecked as targets in the info.plist file, this isn't an issue as long as the fonts/icons will load.

### Android

Edit *android/app/build.gradle (NOT android/build.gradle)* and add the following:

```bash
apply from "../../node_modules/react-native-vector-icons/fonts.gradle"
```


# Using the Added Icons

To find the icons that we want to use, we can use this directory:

[React Native Icons Directory](https://oblador.github.io/react-native-vector-icons/)

## Adding the Icons to Files

Once we have picked an icon and determined the library that the icon comes from, here is how we use it in our project:

```javascript
import Icon from 'react-native-vector-icons/FontAwesome';

...

return (
  <View>
    <Icon name="rocket" size={30} color="#900" />
)
```

## Icon Properties
- **Any Text property**
- size: Size of the icon, can also be passed as *fontSize* in the style object
- name: What icon to show, see the Icons Directory link above
- color: Color the icon