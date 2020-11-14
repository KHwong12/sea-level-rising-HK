# Preparation of the elevation model

## Smoothed DTM

Source: Lands 5m DTM

1. In QGIS, Tool Libraries: Grid -> Filter -> Gaussian Filter
2. Choose circle, test sd and radius 
3. Export raster
4. aggregate to 10m resolution (optional)

Currently use sd = .5 and radius = 2


https://gis.stackexchange.com/questions/265854/qgis-raster-map-smoothing-pixels


## Hybrid DTM With spot height (test only)

1. 5m DTM to TIN
2. copy TIN
3. Add spot height data by `Edit TIN`
4. Convert TIN back to raster
5. Use `Raster Calculator` with `Con` statement to convert cells lower than 2m (i.e. sea) to 0 
