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
   </body>
</html>

