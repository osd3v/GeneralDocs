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



