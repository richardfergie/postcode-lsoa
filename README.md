# English Postcodes and LSOA
Spatial join between English postcodes and English LSOA

Might be useful for someone

Postcode data from the OS code point open dataset
LSOA data from the census

## Processing
1. Open LSOA shp file in qgis
2. Export shp file using the WGS84 projection
3. Dump postcode data into CSV from database (I am unsure what processing is done before inserting into database - conversion to WGS84 at a minimum)
4. Load both data sets into saga-gis
5. Perform spatial join
6. Dump to CSV

NB that the postcode location is given as a point when actually a postcode is a region (is this true? Perhaps a postcode is a collection of houses?). This makes it dead easy to say which LSOA a postcode is in because we never have to worry about a postcode that spans two or more LSOAs. But it does mean that things are not 100% accurate.
