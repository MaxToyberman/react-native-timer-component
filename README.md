
# react-native-timer-component

## Getting started

`$ npm install react-native-timer-component --save`

## Usage
```javascript
import Timer from 'react-native-timer-component';

displayMessage () {
  console.log('Timer expired')
}

render () {
  return (
    <Timer ms={5000} expired={() => {this.displayMessage}} />
  );
}
```
## Props

* **ms** *integer* (required) - time in milliSeconds

* **expired** *function* - function to be executed when timer expired
