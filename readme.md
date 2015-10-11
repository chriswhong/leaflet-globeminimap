# Leaflet.GlobeMiniMap

Leaflet.GlobeMiniMap is a simple minimap control that places a 3d Globe in the corner of your map, centered on the same location as the main map.  

## Using the GlobeMiniMap control

Leaflet.GlobeMiniMap requires d3.js & topojson.js.  You can load them from a CDN like this:

```
<script src="https://cdnjs.cloudflare.com/ajax/libs/d3/3.5.5/d3.min.js"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/topojson/1.6.19/topojson.min.js"></script>
```
The library is also looking for `/data/world.json`, so move it from /src to the correct location.

Add the globe minimap with one line of code:
    
```
    var miniMap = new L.Control.MiniMap(options).addTo(map);
```

You can pass in an options object to define colors for the water, land and marker on the globe minimap:

```
{     
  land:'#FFFF00',
  water:'#3333FF',
  marker:'#000000'
}
```
The minimap is reactive, it only changes when the main map's center point changes.  You can't interact with the mini map to move the main map.

##Attribution

The globe is build with d3, and is based on [World Tour](http://bl.ocks.org/mbostock/4183330) an excellent block by Mike Bostock.

The code for the plugin was modified from [Leaflet.MiniMap](https://github.com/Norkart/Leaflet-MiniMap) by Robert Nordon

The marker SVG on the minimap is from [fontawesome via wikimedia.org](https://upload.wikimedia.org/wikipedia/commons/9/93/Map_marker_font_awesome.svg)

##Issues

Please report issues on [github](https://github.com/chriswhong/leaflet-globe-minimap/issues).