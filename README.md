<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8">
    <title>Mi ubicación GPS</title>
    <style>
      body {background-color: powderblue;}
      h1 {color: red;}
      p {color: blue;}
    </style>
  </head>
  <body>
    <h1>Qué es el GPS</h1>
    <p> El Sistema de Posicionamiento Global (GPS</p>
    <h1 id="location">Cargando ubicación...</h1>
    <script>
      if (navigator.geolocation) {
        navigator.geolocation.getCurrentPosition(function(position) {
          var latitude = position.coords.latitude;
          var longitude = position.coords.longitude;
          document.getElementById("location").innerHTML =
            "Latitud: " + latitude + "<br>Longitud: " + longitude;
        });
      } else {
        document.getElementById("location").innerHTML =
          "Lo siento, tu navegador no soporta la ubicación GPS.";
      }
    </script>
  </body>
</html>
![image](https://user-images.githubusercontent.com/57737682/219979157-9894e309-1e0a-4683-9c29-8263ef0aaf70.png)
