## Usage

Install the package

```
npm i -S react-animated-burgers
```

or

```
yarn add react-animated-burgers
```

Import the desired component, for example

```
import { HamburgerArrow } from 'react-animated-burgers'
```

Pass in isActive boolean prop

```
<HamburgerArrow isActive={this.state.isActive} />
```

Pass in toggleButton function prop

```
<HamburgerArrow isActive={this.state.isActive} toggleButton={this.toggleButton} />
```

Pass in buttonColor & barColor string to change the color of the button & bars

```
<HamburgerArrow isActive={this.state.isActive} toggleButton={this.toggleButton} buttonColor="#FFBC67" barColor="white" />
```

Pass in buttonStyle prop for style overrides

```
<HamburgerArrow buttonStyle={{ backgroundColor: "#FFBC67" }} isActive={this.state.isActive} toggleButton={this.toggleButton} />
```

If you prefer using classes pass in className

```
<HamburgerArrow className="my-styles" isActive={this.state.isActive} toggleButton={this.toggleButton} />
```

Complete example app component

```
import React, { Component } from 'react'
import { HamburgerArrow } from 'react-animated-burgers'

class App extends Component {
  state = {
    isActive: false
  }

  toggleButton = () => {
    this.setState({
      isActive: !this.state.isActive
    })
  }

  render() {
    return (
        <HamburgerArrow isActive={this.state.isActive} toggleButton={this.toggleButton} buttonColor="#FFBC67" barColor="white" />
    )
  }
}

export default App
```

## Acknowledgments

- Based on Tasty CSS-animated Hamburgers https://jonsuh.com/hamburgers by Jonathan Suh
