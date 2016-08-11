# react-mapbox-gl

Forked from https://github.com/alex3165/react-mapbox-gl

Changed import statements of 'mapbox-gl' to enable server side rendering.

The samples in the example folder might not be working with these changes. The library works though.
If using webpack remember the necessary configuration:

    https://github.com/mapbox/mapbox-gl-js#using-mapbox-gl-js-with-webpack

![London cycle example gif](london-cycle-example.gif "London cycle example gif")

Based on [mapbox-gl-js](https://www.mapbox.com/mapbox-gl-js/api/) this library aim to bring the api to a React friendly way with some additional extra behavior.
The library include the following elements :

- ReactMapboxGl
- Layer
- Feature
  - Layer type properties `symbol` display a mapbox symbol.
  - Layer type properties `line` display a lineString.
  - Layer type properties `fill` display a polygon.
  - Layer type properties `circle` display a mapbox circle.
- ZoomControl
- Popup

## Breaking change

`zoom` property is now an array it is required to test for a reference equality in `componentWillReceiveProps` of the map component in order to properly update the zoom when the reference changed.

## How to start

```
npm install tf-react-mapbox-gl --save
```

Import the component :

```
// ES6
import ReactMapboxGl, { Layer, Feature } from "tf-react-mapbox-gl";

// ES5
var ReactMapboxGl = require("tf-react-mapbox-gl");
var Layer = ReactMapboxGl.Layer;
var Feature = ReactMapboxGl.Feature;
```

## Examples

- See the example to display a big amount of markers : [London cycle example](example/london-cycle.js)
- See the example to display all the availables shapes : [All shapes example](example/all-shapes.js) 

### Run the examples

- Clone the repository
- Install the dependencies: `npm install`
- Run the example : `npm run example`
  - Default port: `8080`

> Change the example by replacing the example component in `example/main.js` file.


## [API](docs/API.md)
