# Increasing Geospatial Awareness: Storing, Managing, Describing & Sharing Geospatial Data

**This Repository just covers the 'Enhancing Metadata with Geospatial Data' workshop portion**

**DLF Forum 2015**

## Abstract
This workshop is a joint effort to introduce working with geospatial data and geospatial metadata from a variety of contexts. As such, it will be a mix of talking and tinkering, with audience questions and interaction encouraged. We will start with an introduction to geospatial data types  and metadata standards as well as demonstrations of two data sharing services: the California Digital Library's Dash, which allows for geospatial metadata input and discovery for any data type, and Stanford University Libraries' EarthWorks, which focuses exclusively on geospatial datasets. Next will be a demonstration of how content-management systems like Omeka can be leveraged to assist in the submission of GIS data and the creation of geospatial metadata, as well as an introduction to GeoBlacklight geospatial data indexing software. Looking beyond platforms, there will be some hands-on training on how to manage metadata for the preservation and end-user discovery of several digital geospatial data types including vector and raster data, feature catalogs, georeferenced historic maps, and scholarly research data. Finally, there will be a walkthrough and discussion of how to use geographic information to improve discoverability of a wide range of non-geospatial digital library objects, as well as ensure metadata interoperability with geospatial dataset metadata.

## Agenda
_Total Time: 3 hrs w/ 15 min break (12:30 - 3:45)_

### **12:30 - 1:15:** Presentation: Geospatial data preservation and discovery
_Jack Reed (Stanford), Matthew McKinley (California Digital Library)_

1. Types and sources of geospatial data
2. Metadata standards
    - Geo-specific:
        - FGDC
        - ISO 19115/19139
        - ISO 19110
        - ISO 19115-1
        - GeoBlacklight
    - Non geo-specific but with geospatial component:
        - DataCite
        - DC
        - MODS
        - Will be covered in more detail in the _Enhancing descriptive metadata with geospatial properties_ portion
3. Discovery interfaces
    - DASH
    - Stanford Earthworks/GeoBlacklight/Solr

### **1:15 - 1:45:** Workshop: Omeka and GeoBlacklight
_Andrew Battista (NYU)_

1. GeoBlacklight@NYU
2. Acquiring data and metadata for research datasets using GeoBlacklight plug-in for Omeka
3. Quick demonstration of Omeka ingest form
4. Hands-on function: participants practice with input and output of sample GIS data items

### **1:45 - 2:30:** Workshop: Creating and managing geospatial metadata using the ISO Standards Series
_Kim Durante (Stanford)_

1. Creating XML metadata templates for geospatial data layers
2. Standardizing, enhancing, and transforming geospatial metadata using XSLT
3. Auto-generating metadata using Python


### **2:30 - 2:45:** BREAK


### **2:45 - 3:30:** Workshop: Enhancing descriptive metadata with geospatial properties
_Christina Harlow (UT Knoxville)_

1. Purposes for this portion/intro to scope shift
    - Getting items in previously discussed platforms discoverable in primary discovery interfaces/aggregated search options
2. Existing best practices for adding Geospatial attributes
    - For DC - Mountain West Digital Draft
    - For MODS - UTK / Columbia work
    - For RDF Modeled Data - DPLA/Europeana (+ their divergences)
3. Standards, Schema, & Vocabularies
    - [ISO3166](http://www.iso.org/iso/en/prods-services/iso3166ma/02iso-3166-code-lists/list-en1.html)
    - [DCMI Point, Box Datatypes](http://dublincore.org/documents/dcmi-box/)
    - [Geonames](http://www.geonames.org/)
    - [Getty Thesaurus of Geographic Names](http://www.getty.edu/research/tools/vocabularies/tgn/)
    - [LCNAF/LCSH](http://id.loc.gov/)
        - PCC Phase 3 project to possibly add more identifiers, coordinates?
        - Brings up question of Authorities
        - Issues with LoC handling of geographic descriptors
4. Tools for metadata munging for enhancing with geographic properties
    - [Geonames API](http://www.geonames.org/export/web-services.html)
    - [OpenRefine Recon Services](https://github.com/cmh2166/geonames-reconcile)
    - Catmandu Fix Processes, Python metadata scripts, other...?

### **3:30 - 3:45:** Questions for all previous sessions

