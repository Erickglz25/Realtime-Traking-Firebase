# Maps tracking Location + Firebase

## Revision general

* MapsActivity 

La aplicacion inicia de forma predeterminada en la clase MapsActivity
En el metodo onCreate() se generan las referencias de la base de datos (firebase) y se llama al metodo subirLatLongFirebase(). 
Dentro del metodo se solicitan los permisos de geolocalizacion necesarios, posteriormente se solicitan las coordenadas actuales del usuario y se suben a la base de datos dentro de la coleccion "usuario"

* La aplicaciÃn genera un nuevo punto cada vez que se llama al metodo subirLatLongFirebase(), que en este caso se ejecuta al iniciar la app, para un caso real este se debe actualizar cada determinado tiempo

onMapReady se realiza un peticion de la base de datos -> colecciÃ³n usuario, donde se almacenan las variables de localizacion.
Con el metodo addValueEventListener->onDataChange se crean listas temporales de marcadores que se actualizan cada vez que la base de datos sufre algun cambio.

* Los cambios a la base de datos hasta este commit deben ser hechos manualmente en firebase para comprobar el comportamiento.  

