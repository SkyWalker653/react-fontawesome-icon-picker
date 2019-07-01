# react-fontawesome-icon-picker
React Font Awesome Icon Picker is a basic icon picker for react application. This plugin is in initial stage and have some performace issues.

## Installation
React Font Awesome Icon Picker is still not available in NPM website so you have to install it directly from this git repository using below command.

```
npm install https://github.com/SkyWalker653/react-fontawesome-icon-picker.git --save
```

## Usage

```javascript
import React from 'react';
import ReactIconPicker from "react-fontawesome-icon-picker";

class MyComponent extends React.Component {

    constructor(props) {
      super(props);

      this.state = {
        selectedIcon: {
          prefix: 'fas',
          iconName: 'coffee'
        }
      };
    }
    
    iconPickHandler = (icon) => {
      this.setState({
        selectedIcon: icon
      })
    }
    
    render() {
        return (
            <div>
              <ReactIconPicker pickIcon={this.iconPickHandler} /> <br/>
              Icon: <FontAwesomeIcon icon={[this.state.selectedIcon.prefix, this.state.selectedIcon.iconName]} /> <br/>
              Icon Name: {this.state.selectedIcon.prefix + ' fa-' + this.state.selectedIcon.iconName} <br/>
              Icon HTML code: {'<i class="' + this.state.selectedIcon.prefix + ' fa-' + this.state.selectedIcon.iconName + '"></i>'}
            </div>
        )
    }
}

```
