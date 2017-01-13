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
* Bridgestone
* Pirelli
* Firestone
* Goodyear
