## NavigationView

##### android.support.design.widget.NavigationView

Representa el menu de navegación standar para aplicaciones. El contenido del menu puede ser llenado con un **Menu resource file**

Generalmente el NavigationView esta contenido en DrawerLayout

```java
<android.support.v4.widget.DrawerLayout xmlns="http://schemas.android.com/apk/res/andorid"
	xmlns:app="http://schemas.android.com/apk/res-auto"
    android:id="@+id/drawer_layout"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:fitsSystemWindows="true">
    <!-- Contenido del layout -->
    <android.support.design.widget.NavigationView
    android:id="@+id/navigation"
    android:layout_width="wrap_content"
    android:layout_height="match_parent"
    android:layout_gravity="start"
    app:menu="@menu/my_navigation_items"
    />
</android.support.v4.widget.DrawerLayout>
```

## Layouts

Un layout define la estructura de un UI en la aplicación, como en un activity. Todos los elementos en el layout son contruidos utilizando una herencia de objetos View  y ViewGroup. Un view usualmente dibuja un objeto con el que un usuario puede interactuar. Por otro lado, un ViewGroup es un contenedor invisible que define la estructura de layout para objetos View y ViewGroup.

Los objetos View son usualmente llamados widgets y pueden ser un o varias subclasses, como un Button or TextView. Los objectos ViewGroup son llamados Layouts y pueden ser uno o varios types que proveen diferentes estructuras de layouts, como LinearLayout or ConstraintLayout.   

Declarar elementos UI:

* Declarar elementos UI con XML, android provee un extenso vocabulario XML que corresponde a las clases y subclases de View, como los widgets y layouts.

* Instanciar elementos layout en runtime, mediante programación se puede crear objetos View y ViewGroup (y manipular sus propiedades).

  Declarar el UI en XML permite separar la presentación de la lógica de programación que controla el comportamiento. Utilizar archivos XML tambi´ne facilida 

### Escribir XML

### LinearLayout

LinearLayout es un viewgroup que alinea los items es una dirección simple, vertical o horizontal. (**android:orientation**)

