<!DOCTYPE html>
<html>
  <head>
    <title>Ejemplo con CSS interno y geolocalización</title>
    <style>
      h1 {
        color: red;
      }
      p {
        color: blue;
      }
      body {
        background-color: powderblue;
      }
    </style>
    <script>
      function showPosition(position) {
        var lat = position.coords.latitude;
        var lon = position.coords.longitude;
        var location = "Latitud: " + lat + ", Longitud: " + lon;
        var locationElement = document.getElementById("location");
        locationElement.innerHTML = location;
      }

      function showError(error) {
        var locationElement = document.getElementById("location");
        locationElement.innerHTML = "No se pudo obtener la ubicación";
      }

      function getLocation() {
        if (navigator.geolocation) {
          navigator.geolocation.getCurrentPosition(showPosition, showError);
        } else {
          var locationElement = document.getElementById("location");
          locationElement.innerHTML = "Geolocalización no soportada por el navegador";
        }
      }
    </script>
  </head>
  <body onload="getLocation()">
    <h1>Título de la página</h1>
    <p>Este es un párrafo de ejemplo</p>
    <p>Ubicación: <span id="location"></span></p>
  </body>
</html>
