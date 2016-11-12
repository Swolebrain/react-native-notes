# react-native-notes

##Styles

Main props for **shadow** are shadowColor, shadowOffset, shadowOpacity, shadowRadius (like border-radius).


##Components used for styling purposes

```JavaScript
const Card = props => (
    <View style={styles.someStyle}>
      {props.children}
    </View>
);
```

##Enabling Scrolling

1. Identify the content that you expect to be scrollable (eg albumList).
2. Import a component called ScrollView and wrap the content you want to make Scrollable with the ScrollView component.
3. Find the root component of your app and give it a `flex: 1` style.

##Buttons

TouchableHighlight is the one that changes color (customizable) when tapped. TouchableOpacity dims itself when tapped.

##Bundling imports

You can have a file like index.js or imports.js where you say something like:
```JavaScript
export * from './Component1'
export * from './Component2'
export * from './Component3'
```
and it will work like a pass-through import/export so long as each of those files has the export written in this way (export default doesnt work):

```JavaScript
export { Component1 };
export { Component2 };
export { Component3 };
```
If you name the passthrough file index.js, then this allows you to import your common components without specifying the filename. For instance:

```JavaScript
import { Component1 } from './common'
```

##Textinput

You should disable autocorrect on email inputs by using the prop `autoCorrect={false}`

You can use the prop secureTextEntry (with value of true) to create a password input
