# BCCHC2
The shapefiles could be in different Coordinate Reference System (CRS). if you read your data using geopandas:

```
import geopandas as gpd

gdf = gpd.read_file ('data.shp')
```

Then write:

```
gdf.crs
```

It will show you the CRS of the shapefile. For example, EPSG:3857

If you want to be able to depict it using leaflet in javascript, you should write:

```
gdf_new = gdf.to_crs(epsg=4326)
```

That will take you to the CRS that you are looking for, EPSG:4326

[This page](https://kodu.ut.ee/~kmoch/geopython2020/L2/crs-projections.html) was helpful.

In this repository geo_under_new.js and geo_over_new.js are the javascript files containing the shapefiles for over 12 years old and under 12 years old.

**Note:** This ReadMe was intended for me to remember and understand in the future, not you.
