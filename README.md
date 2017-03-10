
# react-native-timer-component

## Getting started

`$ npm install react-native-timer-component --save`

### Mostly automatic installation

`$ react-native link react-native-timer-component`

### Manual installation


#### iOS

1. In XCode, in the project navigator, right click `Libraries` ➜ `Add Files to [your project's name]`
2. Go to `node_modules` ➜ `react-native-timer-component` and add `RNTimer.xcodeproj`
3. In XCode, in the project navigator, select your project. Add `libRNTimer.a` to your project's `Build Phases` ➜ `Link Binary With Libraries`
4. Run your project (`Cmd+R`)<

#### Android

1. Open up `android/app/src/main/java/[...]/MainActivity.java`
  - Add `import com.reactlibrary.RNTimerPackage;` to the imports at the top of the file
  - Add `new RNTimerPackage()` to the list returned by the `getPackages()` method
2. Append the following lines to `android/settings.gradle`:
  	```
  	include ':react-native-timer-component'
  	project(':react-native-timer-component').projectDir = new File(rootProject.projectDir, 	'../node_modules/react-native-timer-component/android')
  	```
3. Insert the following lines inside the dependencies block in `android/app/build.gradle`:
  	```
      compile project(':react-native-timer-component')
  	```

#### Windows
[Read it! :D](https://github.com/ReactWindows/react-native)

1. In Visual Studio add the `RNTimer.sln` in `node_modules/react-native-timer-component/windows/RNTimer.sln` folder to their solution, reference from their app.
2. Open up your `MainPage.cs` app
  - Add `using Cl.Json.RNTimer;` to the usings at the top of the file
  - Add `new RNTimerPackage()` to the `List<IReactPackage>` returned by the `Packages` method


## Usage
```javascript
import Timer from 'react-native-timer-component';

displayMessage () {
  console.log('Timer expired')
}

<Timer ms={5000} expired={() => {this.displayMessage}} />
```
## Props

* **ms** *integer* (required) - time in milliSeconds

* **expired** *function* - function to be executed when timer expired
