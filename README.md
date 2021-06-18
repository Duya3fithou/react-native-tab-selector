# react-native-tab-selector

> Made with create-react-library

[![NPM](https://img.shields.io/npm/v/react-native-tab-selector.svg)](https://www.npmjs.com/package/react-native-tab-selector) [![JavaScript Style Guide](https://img.shields.io/badge/code_style-standard-brightgreen.svg)](https://standardjs.com)

## Install

```bash
yarn add react-native-tab-selector
```
## Props

- **tabs**: `array[]` input of tab data
- **onChangeTab**: `void()` return current tab index active.
- **style**: Container style.
- **backgroundColor**: Background color of component.
- **styleTab**: custom style of each tab.
- **styleTitle**: custom style of text title tab.
## Usage

```jsx
import React, { useState } from 'react'
import { View, StyleSheet, Text } from 'react-native'
import TabSelectorAnimation from 'react-native-tab-selector'

const DATA = [{ title: 'Tab1' }, { title: 'Tab2' }, { title: 'Tab3' }]

const Example = () => {
  const [indexTab, setIndexTab] = useState(0)

  return (
    <View style={styles.wrapperAll}>
      <TabSelectorAnimation
        onChangeTab={setIndexTab}
        style={styles.tabSelector}
        tabs={DATA}
      />
      <Text style={styles.text}>{`Current tab is ${indexTab + 1}`}</Text>
    </View>
  )
}

const styles = StyleSheet.create({
  wrapperAll: {
    flex: 1,
    alignItems: 'center',
    justifyContent: 'center'
  },
  tabSelector: {
    marginHorizontal: 20
  },
  text: {
    fontSize: 20,
    marginTop: 20
  }
})

export default Example
```

## Demo
![Demo](https://github.com/Duya3fithou/react-native-tab-selector/blob/master/example/ex.gif)
## License

MIT © [duya3fithou](https://github.com/duya3fithou)
