# Ejemplo de Swipe Reveal Layout en Kotlin

## Configuración del Proyecto

### 1. Configuración del archivo `build.gradle.kts` a nivel de proyecto
Agrega la siguiente tarea para limpiar el proyecto:

```kotlin
tasks.register("clean", Delete::class.java) {
    delete(rootProject.layout.buildDirectory)
}
```

En `build.graddle.kts` nivel project Module:app
```kotlin
dependencies {
    ...
    implementation("com.github.chthai64:SwipeRevealLayout:1.4.0")
}
```

En `gradle.properities`   
agregar asi
```kotlin
android.useAndroidX=true
android.enableJetifier=true
```

En `gradle-wrapper.properities`  
cambiar esto por la version (mas info de la version que uso en el archivo gradle)
```kotlin
distributionUrl=https\://services.gradle.org/distributions/gradle-8.7-bin.zip
```

En `settings.graddle.kts`  
Agregar en:
```kotlin
pluginManagement {
    ...
    repositories {
        ...
        maven { url = uri("https://jitpack.io") }
    }
}


dependencyResolutionManagement {
    ...
    repositories {
        ...
        maven { url = uri("https://jitpack.io") }
    }
}
```
