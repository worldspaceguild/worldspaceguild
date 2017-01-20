<html lang="en-US" xmlns="http://www.w3.org/1999/xhtml">
   <head profile="http://gmpg.org/xfn/11">
      <meta http-equiv="Content-Type" content="text/html; charset=UTF-8" />
 
      <link rel="stylesheet" type="text/css" href="http://cdn.leafletjs.com/leaflet/v0.7.7/leaflet.css" />
      
      <script type='text/javascript' src='//ajax.googleapis.com/ajax/libs/jquery/2.0.3/jquery.min.js'></script>
      <script type='text/javascript' src='http://cdn.leafletjs.com/leaflet/v0.7.7/leaflet.js'></script>
   </head>
 
   <body>
      <h1>Leaflet Example</h1>
      
      <p>Here's a map of the countries I've either lived in or travelled through for a month or more.
      
      <div id="map" style="height: 440px; border: 1px solid #AAA;"></div>
 
      <script type='text/javascript' src='maps/markers.json'></script>
      <script type='text/javascript' src='maps/leaf-demo.js'></script>
      var map = L.map( 'map', {
    center: [20.0, 5.0],
    minZoom: 2,
    zoom: 2
});
L.tileLayer( 'http://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
    attribution: '&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a>',
    subdomains: ['a','b','c']
}).addTo( map );

6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
markers = [
   {
     "name": "Canada",
     "url": "https://en.wikipedia.org/wiki/Canada",
     "lat": 56.130366,
     "lng": -106.346771
   },
   {
     "name": "Anguilla",
     "url": "https://en.wikipedia.org/wiki/Anguilla",
     "lat": 18.220554,
     "lng": -63.068615
   },
...
   {
     "name": "Japan",
     "url": "https://en.wikipedia.org/wiki/Japan",
     "lat": 36.204824,
     "lng": 138.252924
   }
];
for ( var i=0; i < markers.length; ++i ) 
{
   L.marker( [markers[i].lat, markers[i].lng] )
      .bindPopup( '<a href="' + markers[i].url + '" target="_blank">' + markers[i].name + '</a>' )
      .addTo( map );
}
   </body>
</html>

