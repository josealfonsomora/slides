---
@title[Hello]

## Hello!

## Thanks for comming!

+++?image=template/img/bg/green.jpg&position=right&size=10% 100%
@title[About Me]

![me](template/img/me.jpg)
#### José Alfonso Mora
#### Android Engineer
##### Twitter: https://twitter.com/josealfonsomora
##### LinkedIn: https://www.linkedin.com/in/josealfonsomora/
+++?image=template/img/bg/green.jpg&position=right&size=50% 100%

@snap[west split-screen-byline]
![ding](template/img/ding_app.jpeg)
@snapend
@snap[midpoint split-screen-img]
![plynk](template/img/plynk_app.jpeg)
@snapend
@snap[east split-screen-text text-white]
![numbrs](template/img/numbrs_app.png)
@snapend

Note:

- Ding - Enero 2015
- Plynk - Octubre 2016
- Numbrs - Enero 2018
---
## Android App Bundle
![appbundle](template/img/app_bundle.jpg)
##### https://developer.android.com/guide/app-bundle/

Note:

Google IO / Mayo 2018

Necesitamos adelgazar nuestras APKS

+++
```
   // APK splitting
    splits {
        abi {
            // Enable APK splitting wrt architecture
            enable true
            
            // Reset the architectures for which you need to build the APKs for
            reset()
            
            // Include the architectures for which Gradle is building APKs
            include 'x86', 'x86_64', 'armeabi-v7a', 'arm64-v8a'
            
            // Set this to false if you don't want an APK that has native code for all architectures
            universalApk false
        }
    }
```
+++
![asappbundle](template/img/android_studio_app_bundle.png)
---
## Requisitos
+++
### Androi Studio 3.2
Note:

- Gradle 3
- AAPT2 (Android Asset Packaging Tool) is a build tool that Android Studio and Android Gradle Plugin use to compile and package your app's resources. AAPT2 parses, indexes, and compiles the resources into a binary format that is optimized for the Android platform.
+++
### App Signing
![signing](template/img/app_signing.png)
---
### Cómo funciona?
+++
### Bundletool
###### https://developer.android.com/studio/command-line/bundletool
###### https://github.com/google/bundletool

Note:

- Incluido en Android studio 3.2
- Open source
- Comand line tool
+++
### .aab
![aab](template/img/aab.png)
##### https://developer.android.com/guide/app-bundle/

Note:

- abb no se puede instalar
- no es lo mismo que un apk
+++
#### Google play firma nuestras apps
![signing steps](template/img/app_signing_steps.png)
+++
![whot it works](template/img/app_bundle_how_it_works.png)
+++
### Reducir tamaño app
![apk size](template/img/saved_size.png)
---
### Configuraciones
+++
```groovy
bundle {
    density{
        enableSplit = false
    }
    
    abi {
        enableSplit = false
    }
    
    language {
        enableSplit = false
    }
}
```
---
### Ejemplo real
+++
![peso cristal app](template/img/peso_cristal.png)
###### https://play.google.com/store/apps/details?id=com.josealfonsomora.pesoscristal
+++
![peso cristal size](template/img/peso_cristal_size.png)
+++
![peso cristal savings](template/img/peso_cristal_savings.png)
+++
### Bundle Explorer en Google Play Console
![live](https://media.giphy.com/media/A34x7CEKUkCyc/giphy.gif)
+++
![peso cristal comparacion](template/img/peso_cristal_comparacion.png)
---
### Otro ejemplo
+++
![sensei app](template/img/sensei_trade.png)
###### https://play.google.com/store/apps/details?id=com.txstockdata.senseitrade1
+++
![sensei app size](template/img/sensei_trade_size.png)
---
### App Bundle + Dynamic feature modules
![app bundle dynamic](template/img/app_bundle_dynamic_delivery.png)
https://developer.android.com/studio/projects/dynamic-delivery#dynamic_feature_modules

Note:

- Beta - Solo internal test track
- Solicitar access
+++
### New dynamic feature module
![dynamic feature module](template/img/dynamic_delivery.png)
+++
##### Android Studio -> New Module
![new module](template/img/new_module.png)
+++
###### Dynamic Feature Module
![new dynamic feature](template/img/new_dynamic_feature_module.png)
+++
###### Configure on demand
![on demand](template/img/dynamic_configure_on_demand.png)
+++
###### Configure on demand
![new module](template/img/dynamic_configure_on_demand.png)
+++
![module created](template/img/module_created.png)
+++
![manifest created](template/img/manifest_created.png)
+++
![dependency error](template/img/dependency_error.png)
+++
![api solution](template/img/api_solution.png)
---
### Como lo usamos?
https://github.com/googlesamples/android-dynamic-features
+++










