GSI Vector Tile Experiment
===
Geospatial Information Authority of Japan (GSI, http://www.gsi.go.jp/ ) provides a vector tile service for its authoritative geospatial data, with nationwide coverage updated intermittently, available in GeoJSON format. The aim of the experiment is to design the best way to provide the result of the basic survey conducted according to Survey Act by GSI, in a way users can make use of the latest web map technologies.

Making the data from GSI more accessible to developers is central to the mission of the Information Access Division of GSI. We don't want you to have to struggle with handling GML data, installing PostGIS, or download the whole bunch of data to start playing with our data.

Vector tiles make real-time rendering possible by sending the underlying geometry and attributes directly to the client, whether that's browser or a native mobile app. We believe that vector tiles will enable yet-to-be-invented types of applications. Use our data to experiment with ideas.

Please note: this service is in experimental phase and is subject to change!

# Getting Started
This service is available for all developers to use.

## Using the serice
The template URL for our vector tiles service is as below:
```
http://cyberjapandata.gsi.go.jp/xyz/{layer}/{z}/{x}/{y}.geojson
```
This url scheme is slippy map tilenames (XYZ).

Here's a sample tile in GeoJSON:
http://cyberjapandata.gsi.go.jp/xyz/experimental_fgd/18/233094/102736.geojson

Please note that the charset of all our GeoJSON data is UTF-8.

Also please note that our GeoJSON vector tile data does not have the concept of layers; One raw FeatureCollection is enclosed in on GeoJSON tile.

# Spatial coverage
Spatial coverage of this experiment is the whole area of Japan. However, several layers provided in early stage still covers limited area called 'experiment area'.

The experiment area is shown in https://github.com/handygeospatial/vector-tile-experiment-area/blob/gh-pages/area.geojson .

# Layers
Data are organized into several layers comprising the elements typically used for base map rendering. This is one view of GSI data for easier consumption, with interleaving serveral Feature Classes into one layer.

## experimental_rdcl: road centerline
Road centerline.

- **zoom level:** 16
- **coverage:** whole Japan area
- [example]( http://cyberjapandata.gsi.go.jp/xyz/experimental_rdcl/16/58242/25798.geojson)
- [default style]( http://cyberjapandata.gsi.go.jp/xyz/experimental_rdcl/style.js)

Please note [the specification for the default style](https://github.com/gsi-cyberjapan/style-dot-js-spec).

### properties
- rID
- lfSpanFr
- lfSpanTo
- tmpFlg
- orgGILvl
- ftCode
- admCode
- devDate
- type
- rdCtg
- state
- lvOrder
- name
- comName
- admOfcRd
- rnkWidth
- Width
- sectID
- tollSect
- medSect
- motorway
- repLtdLvl
- rtCode

## experimental_railcl: railroad centerline
Railroad centerline.

- **zoom level:** 16
- **coverage:** whole Japan area
- [example](http://cyberjapandata.gsi.go.jp/xyz/experimental_railcl/16/58242/25798.geojson)
- [default style](http://cyberjapandata.gsi.go.jp/xyz/experimental_railcl/style.js)

### properties
TODO

## experimental_rvrcl: river centerline

- **zoom level:** 16
- **coverage:** whole Japan area
- [example](http://cyberjapandata.gsi.go.jp/xyz/experimental_rvrcl/16/58242/25798.geojson)
- [default style](http://cyberjapandata.gsi.go.jp/xyz/experimental_rvrcl/style.js)

### properties
TODO

## experimental_anno: annotation

- **zoom level:** 15
- **coverage:** whole Japan area
- [example](http://cyberjapandata.gsi.go.jp/xyz/experimental_anno/15/29106/12903.geojson)
- [default style](http://cyberjapandata.gsi.go.jp/xyz/experimental_anno/style.js)

### properties
TODO

## experimental_fgd: 1:2500 data

- **zoom level:** 18
- **coverage:** [experiment area](https://github.com/handygeospatial/vector-tile-experiment-area/blob/gh-pages/area.geojson)
- [example](http://cyberjapandata.gsi.go.jp/xyz/experimental_fgd/18/233094/102736.geojson)

The default style of this layer is not yet separated from the [example site](http://gsi-cyberjapan.github.io/experimental_fgd/).

### properties
TODO

## experimental_dem5a: 5m DEM

- **zoom level:** 18
- **coverage:** [experiment area](https://github.com/handygeospatial/vector-tile-experiment-area/blob/gh-pages/area.geojson)
- [example](http://cyberjapandata.gsi.go.jp/xyz/experimental_dem5a/18/233094/102736.geojson)

Please see the [demo site](http://gsi-cyberjapan.github.io/experimental_dem/).

### properties

## experimental_dem10b: 10m DEM

- **zoom level:** 18
- **coverage:** [experiment area](https://github.com/handygeospatial/vector-tile-experiment-area/blob/gh-pages/area.geojson)
- [example](http://cyberjapandata.gsi.go.jp/xyz/experimental_dem10b/18/233094/102736.geojson)

Please see the [demo site](http://gsi-cyberjapan.github.io/experimental_dem/).

### properties
TODO

## experimental_cp: control points

- **zoom level:** 7-12
- **coverage:** whole Japan area
- [example](http://cyberjapandata.gsi.go.jp/xyz/cp/12/3638/1612.geojson)
- [default style](http://cyberjapandata.gsi.go.jp/xyz/cp/style.js)

### properties
TODO

## experimental_pp: principal points
Point data for aerial photographs.

- **zoom level:** 14
- **coverage:** whole Japan area
- [example](http://cyberjapandata.gsi.go.jp/xyz/pp/14/14552/6452.geojson)
- [default style](http://cyberjapandata.gsi.go.jp/xyz/pp/style.js)

### properties
TODO

## experimental_zk25000: 1:25000 map grid

- **zoom level:** 8
- **coverage:** whole Japan area
- [example](http://cyberjapandata.gsi.go.jp/xyz/zk25000/8/224/101.geojson)
- [default style](http://cyberjapandata.gsi.go.jp/xyz/zk25000/style.js)

### properties
TODO

# How it works
TODO

# How to display vector tiles
TODO

Currently we use TileLayer.GeoJSON and TileLayer.Canvas of Leaflet 0.7.3.

## TileLayer.GeoJSON
As in [GSI Maps]( http://maps.gsi.go.jp/?ll=35.707179,139.959544&z=17&base=ort&ls=experimental_railcl%7Cexperimental_anno&cd=f4&vs=c1j0l0u0&d=l) ([GitHub repo.](https://github.com/gsi-cyberjapan/gsimaps/))

## TileLayer.Canvas
As in an [example]( http://gsi-cyberjapan.github.io/vector-tile-experiment/canvas.html) ([GitHub repo.](https://github.com/gsi-cyberjapan/vector-tile-experiment/))

# ChangeLog
- 2014-08-01 Experiment started
- 2015-08-05 First release of README_en.md
