## Enhancing Descriptive Metadata with Geospatial Properties

**This Repository just covers the 'Enhancing Metadata with Geospatial Data' workshop portion: see the link to the full workshop schedule and documentation here: http://bit.ly/DLF15geowkshop**

## Mountain West Digital Library

Included in this repository is the MWDL Geospatial Discovery Final Report, which includes their geospatial metadata recommendations and examples, and a sample OpenRefine project that walks through their proposed OpenRefine Geospatial metadata enhancement process. [They walk through the process here, and the steps are also included below.](https://sites.google.com/site/mwdlgeospatial/home/openrefine)

1. Clean up your geospatial metadata column - split multiple values, remove trailing whitespaces, remove parentheses.
2. Create column GeoNames Search on the geospatial column by fetching URLs with this grel: 
```
"http://api.geonames.org/search?maxRows=1&username=YOURGEONAMESUSERNAME&country=US&style=short&isNameRequired=true&type=xml&q=\" + escape(value, \"url\")
```
3. Create a second column with that retrieved XML. You'll parse that column.
4. On that second Geonames XML return column, name it GeoName ID and apply the following GREL: 
```
value.parseHtml().select(\"geonameId\")[0].innerHtml()"
```
6. Create column Hierarchy at index 13 by fetching URLs based on column geonameId using this grel:
```
\"http://api.geonames.org/hierarchyJSON?username=smcintyre&geonameId=\" 
```
7. Create column Hierarchy extracted at index 14 based on column Hierarchy using expression 
```
grel:forEach(value.parseJson().geonames,foo,foo.toponymName).join(\", \")"
```
8. Create column lat, lng at index 12 based on column GeoNames Search using expression 
```
grel:value.parseHtml().select(\"lat\")[0].innerHtml() + \", \" + value.parseHtml().select(\"lng\")[0].innerHtml()"
```
9. Create column Combine cells at index 16 based on column Hierarchy extracted using expression 
```
grel:cells[\"lat, lng\"].value + \"; http://sws.geonames.org/\" + cells[\"geonameId\"].value + \"\\/; \" + value"
```
