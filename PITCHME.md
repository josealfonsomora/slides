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
---
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

