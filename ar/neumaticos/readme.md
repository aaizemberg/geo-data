* Fate

```javascript
var url = "https://www.fate.com.ar/puntos-de-venta";
var json = [ ... ];
console.log("title|lat|lng|sucursal|description");
for (let f of json) {
    console.log(f.title +"|"+ f.lat +"|"+ f.lng +"|"+ f.sucursal +"|"+ f.description);
}
```

* Michelin

```javascript
var url = "http://dealer-locator.michelin.com.ar/AR/es/search?rft=yes&all=1&query=Buenos+Aires%2C+Argentina&st_join=and&radius_index=1&radius=5000"
<div class="l_dealer-list">
<script>
var listDealers = [ ... ]
d3.select("body").append("div.titulos").text('lat|lng|name|id|street1|street2|zipcode|city|link');
d3.select("body").selectAll("div.data").data(listDealers).enter()
  .append("div")
  .text( function(d) {return d.lat + '|' + d.lng + '|' + d.name + '|' + d.id + '|' + d.street1 + '|' + d.street2 + '|' + d.zipcode + '|' + d.city + '|' + d.link;} );
```

* Bridgestone

```javascript
var url = "http://www.bridgestone.com.ar/pasajero/neumaticos/puntos-de-venta";
// <span id="ContenidoPrincipal_C001_lblJsonGeolocalizar" style="display: none">[{"geo_longitud ...
var data = [{"geo_longitud": ... }];
d3.select("body").append("div").text("rowid|longitud|latitud|nombreContacto|descripcionContacto|telefono1|telefono2|email|urlSitio");
d3.select("body").selectAll("div.rows").data(data).enter().append("div").attr("class","rows")
  .text( function(d,i) {return i + "|"  + d.geo_longitud + "|" + d.geo_latitud
     + "|" + d.nombreContacto + "|" + d.descripcionContacto + "|" + d.telefono1 + "|" + d.telefono2
     + "|" + d.email + "|" + d.urlSitio;} 
       );
```

* Pirelli

```javascript
var url = "https://www.pirelli.com/tyres/es-ar/__service__/dealer/dataDealers/data?pageId=17634";
var datos = {"status":true,"data":[ ... ]};
d3.select("body").append("div").text('address|city|details|email|fax|lat|lng|id|image|name|phone|region|url|zip');
d3.select("body").selectAll("div.rows").data(datos.data).enter().append("div").attr("class","rows")
  .text(function(d,i) { return i + '|' + d.address + '|' + d.city + '|' + d.details + '|' + d.email + '|' + d.fax + '|' + d.geo_localization.lat + '|' + d.geo_localization.lng + '|' + d.id + '|' + d.image + '|' + d.name + '|' + d.phone + '|' + d.region + '|' + d.url + '|' + d.zip; });
```

* Firestone

```javascript
var = "http://www.firestone.com.ar/pasajero/neumaticos/puntos-de-venta"
var data = var data = [{"geo_longitud":... ];
d3.select("body").append("div").text('descripcionContacto|email|geo_latitud|geo_longitud|horario|nombreContacto|telefono1|telefono2|urlSitio');
d3.select("body").selectAll("div.datos").data(data).enter().append("div").attr("class","datos")
  .text(function(d,i) { return i + '|' + d.descripcionContacto + '|' + d.email + '|' + d.geo_latitud + '|' +d.geo_longitud + '|' +d.horario + '|' + d.nombreContacto + '|' + d.telefono1 + '|' + d.telefono2 + '|' + d.urlSitio; });
 ```

* Goodyear

```javascript
var = "http://www.goodyear.com.ar/cfmx/web/ladealer/dealers.cfm?countryid=4"
// los datos estan en la 2da tabla, separados por <br />'s
```
