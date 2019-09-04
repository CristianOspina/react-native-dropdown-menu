# react-native-dropdown-menu
Fork with **titles** support: in the initial state it shows a default title/placeholder for each dropdown, useful to specify for what the dropdown is about.


A `<DropdownMenu>` component for react-native ( iOS ).  Easy to use.   

 ![image](https://github.com/WheelerLee/react-native-dropdown-menu/blob/master/screenshot1.gif?raw=true)

## Install
```shell
npm i react-native-dropdown-menu --save
```
or
```shell
yarn add react-native-dropdown-menu
```

## Usage
```js
import DropdownMenu from 'react-native-dropdown-menu';

export default class Demo extends Component {

  constructor(props) {
    super(props);
    this.state = {
      text: ''
    };
  }

  render() {
    var titles = ["Langs 1", "Langs 2", "Langs 3"];
    var data = [["C", "Java", "JavaScript", "PHP"], ["Python", "Ruby"], ["Swift", "Objective-C"]];
    return (
      <View style={{flex: 1}}>
        <View style={{height: 64}} />
        <DropdownMenu
          style={{flex: 1}}
          bgColor={'white'}
          tintColor={'#666666'}
          activityTintColor={'green'}
          // arrowImg={}
          // checkImage={}
          // optionTextStyle={{color: '#333333'}}
          // titleStyle={{color: '#333333'}}
          // maxHeight={300}
          handler={(selection, row) => this.setState({text: data[selection][row]})}
          titles={titles}
          data={data}
        >

          <View style={{flex: 1}}>
            <Text>
              {this.state.text} is the best language in the world
            </Text>
          </View>

        </DropdownMenu>
      </View>
    );
  }

}
```
