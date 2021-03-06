Building upon https://github.com/klokantech/osm2vectortiles-ios, now an iOS app
can be built to have local vector data, styles, glyphs and sprites.

## Features

* 100% local data (notice in the animation that WiFi is turned off at the beginning of the demo)
* Vector data built using http://OSM2VectorTiles.org
* Styling of the countries is from https://github.com/klokantech/mapbox-gl-js-offline-example

## Build

* In Terminal, run `pod install`
* Then open the Workspace `OSM2VectorTiles.xcworkspace`

## Architecture

* All assets are local and are accessed by Mapbox GL by the `asset://` URI.

```
"sources": {
    "countries": {
        "type": "vector",
        "tiles": [
            "asset://geography-class.osm2vectortiles/{z}/{x}/{y}.pbf"
        ]
    }
},
"sprite": "asset://sprites/bright-v8",
"glyphs": "asset://glyphs/{fontstack}/{range}.pbf",
```


![geography-class](geography-class.gif)

* (QuickTime has a bug when screen recording; as it still shows WiFi service is on, when it indeed is off)
