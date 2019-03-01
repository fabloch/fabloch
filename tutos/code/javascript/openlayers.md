# OpenLayers

[OpenLayers](https://openlayers.org/)

## Tips and tricks

### Mes points ne sont pas visibles sur la carte

See default [ol.style](http://openlayers.org/en/latest/apidoc/ol.style.html) of ol.layer.Vector

Stroke needs some shape of feature such as circle, polygon, etc,. simple ol.geom.point doesn't have a shape. that's why nothing appears when you set style only with stroke

If you change your style like below, it will work as you expect:
```
var style = new ol.style.Style({
  image: new ol.style.Circle({ // add this
    stroke: new ol.style.Stroke({
      color: 'red'
    }),
    radius: 5
  }),
});
```

- [Moveend sample](https://openlayers.org/en/latest/examples/moveend.html)
- [Update a feature's coordinates/geometry](https://gis.stackexchange.com/questions/189462/update-a-features-coordinates-geometry)
- [Detecting map changes](Detecting map changes using Openlayers)
- [how to get the current zoom in openlayers](https://stackoverflow.com/questions/39017806/how-to-get-the-current-zoom-in-openlayers)
- [Add feature manually to a vector layer](https://gis.stackexchange.com/questions/153092/add-feature-manually-to-a-vector-layer-in-ol3)
- [Clear features in a vector layer](https://gis.stackexchange.com/questions/251770/how-can-i-clear-a-vector-layer-features-in-openlayers-4)
- [Rotate marker Image](https://openlayers.org/en/latest/apidoc/module-ol_style_Icon.html)

[How to add marker to user defined image](https://gis.stackexchange.com/questions/176510/how-to-add-marker-to-user-defined-image-in-openlayers-3)
[how to add markers with OpenLayers 3](https://stackoverflow.com/questions/24315801/how-to-add-markers-with-openlayers-3)

[How to get the current viewport of the map](https://stackoverflow.com/questions/8988453/how-to-get-the-current-viewport-of-the-map-out-of-openlayers-as-geometry-boundi)

https://openlayers.org/workshop/en/vectortile/map.html
