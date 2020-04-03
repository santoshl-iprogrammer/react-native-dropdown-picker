
# React native dropdown picker
A picker (dropdown) component for react native which supports both Android & iOS.
## Getting Started
### Installation
##### via NPM
```sh
$ npm install react-native-dropdown-picker
```
##### via Yarn
```sh
$ yarn add react-native-dropdown-picker
```
### Basic Usage
First of all import the package.
```javascript
import DropDownPicker from 'react-native-dropdown-picker;
```
Render the component.
```javascript
<DropDownPicker
    items={[
        {label: 'Item 1', value: 'i1'},
        {label: 'Item 2', value: 'i2'},
    ]}
    defaultIndex={0}
    style={{minWidth: 150}}
    onChangeItem={item => console.log(item.label, item.value)}
/>
```
### Default item
You may want to select one of the items as default.
1. Add `selected: true` to the object.

    ```javascript
    items={[
        {label: 'Item 1', value: 'i1'},
        {label: 'Item 2', value: 'i2', selected: true},
    ]}
    ```
2. The `defaultIndex` property.

    ```javascript
    defaultIndex={1}
    ```
3. The `defaultValue` property.

    ```javascript
    defaultValue="i2"
    ```
### Placeholder
You may want to have a placeholder while the default value is null.

Add the following properties to the component.
```javascript
...
defaultNull
placeholder="Select an item"
...
```
### Styling the component
You have 3 options to style the component.
1. The `style` property.

    ```javacript
    style={{minWidth: 150}}
    ```
    It's also possible to extend the width of the component with `width: '100%'` which depends on the parent's style.

2. The `itemStyle` property.
        If you want the labels on the `left` and `right` side or to centerize them:

    ```javacript
    itemStyle={{alignItems: 'flex-start|flex-end|center'}}
    ```
3. The `labelStyle` property.
    This property gives full control over the label.
    ```javacript
    labelStyle={{fontSize: 14, color: '#000'}}
    ```
### Props
|Name|Description|Default|Required
|--|--|--|--
|`items`|The items for the component.||Yes
|`defaultIndex`|The index of the default item.|`0`|No
|`defaultValue`|The value of the default item.||No
|`defaultNull`|This sets the choice to null which must be used with `placeholder`|`false`|No
|`placeholder`|Default text to be shown to the user which must be used with `defaultNull`|'Select an item'|No
|`dropDownMaxHeight`|Height of the dropdown box.|`150`|No
|`style`|Additional styles for the component.|`{}`|No
|`itemStyle`|Additional styles for the items.|`{}`|No
|`labelStyle`|Additional styles for the labels.|`{}`|No
|`disabled`|This disables the component.|`false`|No
|`onChangeItem`|Callback which returns `item` and `index`. the `item` is the selected object.||No