# react-native-tab-selector

> Made with create-react-library

[![NPM](https://img.shields.io/npm/v/react-native-tab-selector.svg)](https://www.npmjs.com/package/react-native-tab-selector) [![JavaScript Style Guide](https://img.shields.io/badge/code_style-standard-brightgreen.svg)](https://standardjs.com)

## Install

```bash
yarn add react-native-tab-selector
or
npm install --save react-native-tab-selector
```

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
        index={indexTab}
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
![Alt Text](https://github.com/Duya3fithou/react-native-tab-selector/example/ex.gif)
## License

MIT © [duya3fithou](https://github.com/duya3fithou)
