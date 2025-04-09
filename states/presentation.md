class: center, middle, inverse

# Estados

---
# Pasos para instalar Hilt

1. Agregar plugins al build.gradle.kts (Project :(projectName))

    `id("com.google.dagger.hilt.android") version "2.44" apply false`

2. Agregar plugins al build.gradle.kts (Module :app)

    `id("dagger.hilt.android.plugin")
    id("kotlin-kapt")`

3. Agregar dependencias al build.gradle.kts (Module :app)

    `implementation("androidx.hilt:hilt-navigation-compose:1.2.0")
    implementation("com.google.dagger:hilt-android:2.49")
    kapt("com.google.dagger:hilt-android-compiler:2.44")`

---
# Pasos para incluir Hilt al proyecto

1. Crear aplicación:

    Crear archivo en el root del proyecto (a la misma altura que la main activity):
   
    @HiltAndroidApp
    class LearningAndroidApplication: Application()

3. Referenciar aplicación creada en AndroidManifest.xml

    `<application
      android:name=".LearningAndroidApplication" ... />`

4. Definity la MainActivity como un entry point

   Annotar MainActivity.kt con @AndroidEntryPoint

---
# Pasos para incluir Hilt a las pantallas

1. Crear un View Model

   Agregar anotacion de Hilt, extender ViewModel y utilizar el @Inject:

   `@HiltViewModel
   class FriendsViewModel @Inject constructor() : ViewModel() {`

2. Utilizar hiltViewModel en la UI:

   `val viewModel = hiltViewModel<FriendsViewModel>()`
