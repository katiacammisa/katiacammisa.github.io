class: center, middle, inverse

# Navegación

---
# Pasos para implementar la navegación

1. Agregar dependencia al build.gradle.kts (Module :app)

    implementation("androidx.navigation:navigation-compose:2.7.7")

2. Crear un NavHostController

    El navHostController va a controlar todas las operaciones de navegación (navigate, go back, etc)

3. Crear un archivo con las páginas que vamos a tener

    Declarar los nombres de las pantallas a crear y utilizarlas como rutas

4. Crear el NavHost

    Definir qué Composable se va a mostrar cuando se navegue a cada pantalla

5. Crear TopBar y BottomBar

   Crear barras de navegación estáticas en la aplicación
