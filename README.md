# react-native-component-inview

A React Native wrapper to check whether a component is in the view port to track impressions and clicks

![demo](https://github.com/changey/react-native-component-inview/blob/master/react-native-component-inview.gif)

## Installation

```bash
npm i --save react-native-component-inview # npm syntax
yarn add react-native-component-inview --save # yarn syntax
```

## Example

```
import InView from 'react-native-component-inview'

const [isInView, setIsInView] = useState(false)

const checkVisible = (isVisible:boolean) => {
    if (isVisible){
      setIsInView(isVisible)
    } else {
      setIsInView(isVisible)
    }
  }

<ScrollView>
  <InView onChange={(isVisible) => this.checkVisible(isVisible)}>
    <View style={[styles.item, {backgroundColor: isInView ? 'yellow' : '#f9c2ff'}]}>
      <Text>yay</Text>
    </View>
  </InView>
</ScrollView>
```
