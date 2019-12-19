# react-native-component-inview

A React Native wrapper to check whether a component is in the view port to track impressions and clicks

## Installation

```bash
npm i --save react-native-component-inview # npm syntax
yarn add react-native-component-inview --save # yarn syntax
```

## Example

```
import InView from 'react-native-component-inview'

const checkVisible = (isVisible:boolean) => {
      if (isVisible){
        if (!this.state.isTheComponentInViewPort) {
          this.setState({isTheComponentInViewPort: true})
        }
      } else {
        if (this.state.isTheComponentInViewPort) {
          this.setState({isTheComponentInViewPort: false})
        }
      }
    }

<ScrollView>
  <InView onChange={(isVisible) => this.checkVisible(isVisible)}>
    <View style={styles.text}>
      <Text>⬇ This is the offer that we're tracking</Text>
    </View>
  </InView>
</ScrollView>
```
