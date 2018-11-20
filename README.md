# React-Native SVGWheel Menu

This is a react-native component for IOS and Android that uses React Native SVG where you send the configuration as a prop and the Menu is rendered.

## Getting Started
```bat
npm install react-native-svgwheel-menu --save
```
## Demo
![alt text](https://i.postimg.cc/MGZ1z844/s1.png)
![alt text](https://i.postimg.cc/c4qYr32f/s2.png)

```javascript
import GeneratePathCanvas from "react-native-svgwheel-menu";

const userPurchases = [
    {
        id: '1.1',
        parent: '0.0',
        itemName: 'Sales',
        price: 1,
        color: ''
    },
    {
        id: '1.2',
        parent: '0.0',
        itemName: 'Allocation',
        price: 1,
        color: ''
    },
    {
        id: '1.3',
        parent: '0.0',
        itemName: 'Margins',
        price: 1,
        color: ''
    },
    {
        id: '1.4',
        parent: '0.0',
        itemName: 'Inventory',
        price: 1,
        color: ''
    },
    {
        id: '2.1',
        parent: '1.1',
        itemName: 'Daily Sales',
        price: 1,
        color: ''
    }
];
class App extends Component {
    render() {
    return (
            <GeneratePathCanvas 
                depth= {2}
                homeTitle= 'Home'
                userPurchases= {userPurchases} 
                pieColorArray= {pieColorArray}
                clickEvent= {this.parentHandleFunction}
             />
        );
    }
}
```

## Props
| Prop          | Required      | Description  |
| ------------- |:-------------:| ------------:|
| depth        | true          | A Number to define Levels of your Menu  |
| homeTitle     | true      |   A String to define the title at Level 1 |
| userPurchases     | true      |   An array of values to differentiate between parent and child levels |
| pieColorArray   | true | An array of colors in hex code |
| clickEvent | true      |   A function callback that handles child data and its name clicked at last level |

## Stuff used to make this:

 * [react-native-svg](https://github.com/react-native-community/react-native-svg) for making the svg

