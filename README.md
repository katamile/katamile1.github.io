<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8">
    <title>Mi ubicación GPS</title>
  </head>
  <body>
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
![image](https://user-images.githubusercontent.com/57737682/219978937-89377dc2-d111-4d8c-a3e1-771711cb9a86.png)
