Medway Local Elections 2023  
===========================  

### Description   
- web scraping of 2023 Medway Council local election results (with local caching)  
- data ETL  
- ward and candidate analysis    


### Languages, frameworks and libraries  
- Python  
	- requests  
	- Beautiful Soup  
	- pandas  
	- matplotlib  
- Jupyter Notebook    



### How to get boundary data  
*Download from National Archives - convert to GeoJSON*
1) Get the mapping files from the National Archives
[Mapping files]  
https://webarchive.nationalarchives.gov.uk/ukgwa/20221201172612/https://www.lgbce.org.uk/all-reviews/south-east/kent/medway 

2) Extract ZIP and convert shp file to GeoJSON
```
import geopandas
myshpfile = geopandas.read_file('data/Medway_final_proposals.shp')
myshpfile.to_file('Medway.geojson', driver='GeoJSON')
```
Source:
[StackOverflow] How to get lat and lon from a GeoPandas geodataframe polygon
https://gis.stackexchange.com/questions/412817/how-to-get-lat-and-lon-from-a-geopandas-geodataframe-polygon



*Alternative method for generating SVG file*  
1) Download Medway Boundary map from LGBC  
2) Import PDF into Inkscape  
3) Edit layers  


### How to convert (projected coordiante) shp file to GeoJSON

### Links  

Local Government Boundary Commission - Medway Boundary Map (April 2023)  
https://www.lgbce.org.uk/sites/default/files/2023-04/medway_order_map.pdf
- boundary map for 2023 Medway Local Elections  


Medway Elects  
https://www.medwayelects.co.uk/  
- Medway Election results and analysis


Mapping files
https://webarchive.nationalarchives.gov.uk/ukgwa/20221201172612/https://www.lgbce.org.uk/all-reviews/south-east/kent/medway