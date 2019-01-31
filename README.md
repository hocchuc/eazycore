# EazyCore
Code base for Android
[![Release](https://jitpack.io/v/harrylefit/eazycore.svg)](https://jitpack.io/#harrylefit/eazycore/2.1)
[![Codacy Badge](https://api.codacy.com/project/badge/Grade/6619cd5f41d44885bf516647877bd83b)](https://www.codacy.com/app/harryle-fit/eazycore?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=harrylefit/eazycore&amp;utm_campaign=Badge_Grade)
[![codebeat badge](https://codebeat.co/badges/f86c6d81-3314-49b3-9e22-8215a3c387f4)](https://codebeat.co/projects/github-com-harrylefit-eazycore)
[![Dependency Status](https://www.versioneye.com/user/projects/5899fd201e07ae0046f5912a/badge.svg?style=flat-square)](https://www.versioneye.com/user/projects/5899fd201e07ae0046f5912a)

Using :
- [ButterKnife](https://github.com/JakeWharton/butterknife)
- [Parceler](https://github.com/johncarl81/parceler)
- [FragmentArgs](https://github.com/sockeqwe/fragmentargs)
- [NoListAdapter](https://github.com/TellH/NoListAdapter)
- [Timber](https://github.com/JakeWharton/timber)
- [Rebound](https://github.com/facebook/rebound)

Dependencies: 
  - **Architect**
    - [EazyMvp](https://github.com/harrylefit/eazymvp)
  - **Utils**
    - [EazyLoader](https://github.com/harrylefit/eazyloader)
    - [EazySocial](https://github.com/harrylefit/eazysocial)
    - [TopSnackBar](https://github.com/cuongloveit/topsnackbar)

##Structure

There are base classes . They're separated into 3 main parts (activity, fragment, adapter)
- **Activity :**
  - **BaseActivity :** it contains basic functions to manage the life-cycle of the activity.
  - **BaseMainActivity:** it inherits from `BaseActivity` and manage toolbar, fragments.

- **Fragment :**
  - **BaseFragment :** it's same as `BaseActivity`. It manages the life-cycle of the fragment.
  - **BaseMainFragment :** it inherits from `BaseFragment` and provide the functions to handle toolbar quickly.
  - **BaseMainWithDataFragment :** it inherits from `BaseMainFragment` and provide the functions to push data into `Recyclerview` quickly.

- **Adapter :**
  - **BaseViewBinder :** it's provide the functions to implement `Adapter` into `Recyclerview` quickly.

- **Dialog :**
  - **BaseDialog :** it's provide the basic functions to implement `Dialog` quickly.
  - **BaseAnimationDialog :** it inherits from `BaseDialog` and provide the functions to support animation.
  - **BaseDataDialog :** it inherits from `BaseAnimationDialog` and provide the functions to load data into it.

##Setup
This library is not yet released in Maven Central, until then you can add as a library module or use JitPack.io

In build.gradle (top-level)

Add remote maven url in

```groovy
repositories {
    maven {
        url "https://jitpack.io"
    }
}
```
Add classpath in

```groovy
dependencies {
    classpath 'com.neenbedankt.gradle.plugins:android-apt:1.8'    
}
```

Download
--------

```groovy
	implementation 'com.github.harrylefit:eazycore:2.1'
```

#Licence

Apache License, Version 2.0


    Copyright (C) 2017, Harry Le

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

         http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
