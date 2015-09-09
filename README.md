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
