# react-native-easy-select
[![NPM version](https://img.shields.io/npm/v/react-native-easy-select)](https://www.npmjs.com/package/react-native-easy-select)
[![License](https://img.shields.io/npm/l/react-native-easy-select)](https://github.com/havinhthai/react-native-easy-select/blob/master/LICENSE)
[![Update status](https://img.shields.io/david/havinhthai/react-native-easy-select)](https://www.npmjs.com/package/react-native-easy-select)

A flexible select component for React Native.

![Demo](https://s3-ap-southeast-1.amazonaws.com/cdn.tuidev.io/react-native-easy-select.gif)

## Table of Contents
- [Features](#features)
- [Install](#install)
- [Usage](#usage)
- [Props](#props)
- [Contribution](#contribution)
- [License](#license)

## Features
- Easy to use
- Easy to customize
- Pure javascript
- Lightweight package

## Install
```sh
yarn add react-native-easy-select
```
or
```sh
npm i --save react-native-easy-select
```

## Usage
```javascript
import Selector from 'react-native-easy-select'; // Import package

const Example = () => (
  <Selector
    theme="dropdown" // Default: 'simple'
    items={[
      { myLabel: 'English', myValue: 'english' },
      { myLabel: 'French', myValue: 'french' },
    ]}

    // Specify key
    valueKey="myValue" // Default: 'value'
    labelKey="myLabel" // Default: 'label'

    defaultValue="english" // Set default value
    placeholder="Select a language" // Placeholder for dropdown UI

    loading={false} // Set loading for selector

    // Styles
    textOptionStyle={{ color: 'green' }}
    placeholderContainerStyle={{ paddingVertical: 20 }}
    placeholderStyle={{ color: 'red' }}
    optionContainerStyle={{ backgroundColor: 'yellow' }}
    iconStyle={{ tintColor: 'black' }}
    loadingStyle={{ marginBottom: 10 }}

    // Change dropdown icon
    iconDropdownComponent={() => <AppText>Demo</AppText>}

    // On value change
    onChange={(value) => console.log(value)}
  />
);

export default Example;
```

## Props

| Name                         | Type                                                            | Default | Description                                                                                                                                                                                                                                              |
| --------------------------- | --------------------------------------------------------------- | ------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `items`                  | Array | `[]`  | **Required**. The items for the component to render. You can specify value and label via `valueKey` and `labelKey`                                             |
| `onChange`                     | Function           | `(value) => {}`         | **Required**. Callback when the change the value button is pressed.  |
| `valueKey`                     | String              | `'value'`         | Key name to specify value props of object  |
| `labelKey`                     | String              | `'label'`         | Key name to specify label props of object  |
| `theme`                     | String  = 'simple' or 'dropdown'            | `'simple'`         |  **Required**. Specify the UI for select components. Default is `simple` and dropdown UI is `dropdown`.  |
| `defaultValue`                     | String or Numer           | `''`         | Specify the default value of the selector. This value will be compared with the value of `valueKey`.  |
| `loading`                     | String or Numer           | `false`         | Show `ActivityIndicator` when loading.  |
| `iconDropdownComponent`                     | Function           | `null`         | Custom icon component to be rendered.  |
| `defaultValue`                     | String or Numer           | `''`         | Specify the default value of the selector. This value will be compared with the value of `valueKey`.  |
| `placeholder`                     | String           | `''`         | Set placeholder for dropdown UI.  |
| `containerStyle`                     | Object           | `null`         | Style overrides for container View of component.  |
| `optionContainerStyle`                     | Object           | `null`         | Style overrides for View container of each option.  |
| `placeholderContainerStyle`                     | Object           | `null`         | Style overrides for container View wrap of placeholder.  |
| `placeholderStyle`                     | Object           | `null`         | Style overrides for Text of placeholder.  |
| `textOptionStyle`                     | Object           | `null`         | Style overrides for Text of each option.  |
| `iconStyle`                     | Object           | `null`         | Style overrides for icon component.  |
| `loadingStyle`                     | Object           | `null`         | Style overrides for `ActivityIndicator` component.  |

## Contribution
Contribution are always **welcome and recommended**! Here is how:

- Fork the repository ([here is the guide](https://help.github.com/articles/fork-a-repo/)).
- Clone to your machine ```git clone https://github.com/YOUR_USERNAME/react-native-easy-select.git```
- Make your changes
- Create a pull request


## License
`react-native-easy-select` is released under the MIT license. See [LICENSE](./LICENSE) for details.  
  
Any question or support will welcome.
