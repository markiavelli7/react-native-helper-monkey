# Adding Icons

## Step One - Install the Dependencies

```bash
yarn add react-native-vector-icons
```

## Step Two - Link the Icons to iOS and Android

### iOS

1. Browse to *node_modules/react-native-vector-icons* and drag the folder *Fonts* into our project in Xcode. **Make sure that our app is checked under "Add to targets" and that "Create groups" is checked if we add the whole folder.**

2. Edit the *info.plist* file and add a property called **Fonts provided by application** and type in the files we just added:

Item 0 ... FontAwesome.ttf
Item 1 ... Foundation.ttf
...

3. Recompile the project. **If the build fails with an error about multiple info.plist files or duplicates of the .ttf files, go into the Project Build Phases/Copy Bundle Resources section and delete the info.plist file and the .ttf files. This will need to be done in the main app and the tvOS app as well.** NOTE: deleting the files from the Copy Bundle Resources section may cause the App and tvOSApp to become unchecked as targets in the info.plist file, this isn't an issue as long as the fonts will load.

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