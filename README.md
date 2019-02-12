# Maps tracking Location + Firebase

## Revision general

* MapsActivity

> Actualizacion **La funcion getLastLocation se sustituye por el metodo requestLocationUpdates** 

La aplicacion inicia de forma predeterminada en la clase MapsActivity
En el metodo onCreate() se generan las referencias de la base de datos (firebase) y se llama al metodo subirLatLongFirebase(). 
Dentro del metodo se solicitan los permisos de geolocalizacion necesarios, posteriormente se solicitan las coordenadas actuales del usuario y se suben a la base de datos dentro de la coleccion "usuario"

* El metodo locationManger.requestLocationUpdates es el encargado de actualizar las coordenadas cada X segundos, genera y sube un nuevo punto a firebase

onMapReady se realiza un peticion de la base de datos -> colección usuario, donde se almacenan las variables de localizacion.
Con el metodo addValueEventListener->onDataChange se crean listas temporales de marcadores que se actualizan cada vez que la base de datos sufre algun cambio.


