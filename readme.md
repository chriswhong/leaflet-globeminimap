# Leaflet.GlobeMiniMap

Leaflet.GlobeMiniMap is a simple minimap control that places a 3d Globe in the corner of your map, centered on the same location as the main map.  

![cursor_and_3d_minimap_and_minimap_ _bash_ _80x24_and_index_html_ _globe-minimap](https://cloud.githubusercontent.com/assets/1833820/10415088/cb1d45fe-6fb8-11e5-9903-2c2ec16fbabd.png)

[Try the example out out now on github pages](http://chriswhong.github.io/leaflet-globeminimap/example/)

## Using the GlobeMiniMap control

Leaflet.GlobeMiniMap requires d3.js & topojson.js.  You can load them from a CDN like this:

```
<script src="https://cdnjs.cloudflare.com/ajax/libs/d3/3.5.5/d3.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/topojson/1.6.19/topojson.min.js"></script>
```
The library is also looking for `/data/world.json` in order to load the world topojson file. You can use the option `topojsonSrc` to define another source.

Add the globe minimap with one line of code:
    
```
    var miniMap = new L.Control.GlobeMiniMap(options).addTo(map);
```

You can pass in an options object to define colors for the water, land and marker on the globe minimap:

```
{     
  land:'#FFFF00',
  water:'#3333FF',
  marker:'#000000',
  topojsonSrc: 'path/to/world.json'
}
```
The minimap is reactive, it only changes when the main map's center point changes.  You can't interact with the mini map to move the main map.

##Attribution

I saw this static 3d minimap and thought it would be a great plugin for leaflet.  [Static 3d Minimap](http://earthview.withgoogle.com/marshall-islands-6155)

The globe is built with d3, and is based on [World Tour](http://bl.ocks.org/mbostock/4183330) an excellent block by Mike Bostock.

The code for the plugin was modified from [Leaflet.MiniMap](https://github.com/Norkart/Leaflet-MiniMap) by Robert Nordon

The marker SVG on the minimap is from [fontawesome via wikimedia.org](https://upload.wikimedia.org/wikipedia/commons/9/93/Map_marker_font_awesome.svg)

##Issues

Please report issues on [github](https://github.com/chriswhong/leaflet-globe-minimap/issues).
I am a noob at this plugin business, and am not sure if the /dist and build stuff is working properly, so advice and Pull Requests are welcome!  
