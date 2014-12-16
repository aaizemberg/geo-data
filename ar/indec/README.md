Estaba viendo [esta página](http://www.indec.gov.ar/gis/) que es una aplicación GIS desarrollada por el INDEC hecha con [Leaftlet](http://leafletjs.com/) y servicios WMS del IGN y vi que los datos vectoriales los tomaba de varios archivos en formato .js, así que hice una pequeña conversión y quedaron disponibles en formato GeoJSON. 

GitHub los muestra directamente sobre un mapa cuando hacemos una previsualización (https://help.github.com/articles/mapping-geojson-files-on-github/)

Para tener un archivo completo de *Localidades*, tenes que unir estos tres:
 1. [capitales](https://github.com/aaizemberg/geo-data/blob/master/ar/indec/capitales.geojson) (de provincias)
 2. [cabeceras](https://github.com/aaizemberg/geo-data/blob/master/ar/indec/cabeceras.geojson) (de departamentos)
 3. [localidades](https://github.com/aaizemberg/geo-data/blob/master/ar/indec/localidades.geojson) (resto de las localidades)
