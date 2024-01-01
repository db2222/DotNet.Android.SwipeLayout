# DotNet.Android.SwipeLayout
This is a ```.NET 8``` compatible version of https://www.nuget.org/packages/Xamarin.AndroidSwipeLayout. \
\
The original source code can be found under https://github.com/xamarin/XamarinComponents/tree/main/Android/AndroidSwipeLayout. \
However, the project ```XamarinComponents``` is abandoned. There is no migrated alternative. \
The problem is that the component ```AndroidSwipeLayout``` is only compatible with Xamarin.Android (MonoAndroid) and not the newer .NET versions.

Furthermore, it uses the project https://github.com/daimajia/AndroidSwipeLayout as a Java binding library. \
This is as well very old and not maintained anymore. \
But it needs to be compatible with ```AndroidX``` to be usable with modern .NET versions. \
This is why this package uses the fork https://github.com/axzae/android-swipe-layout as the base. \
The ```.aar``` file can be found under https://mvnrepository.com/artifact/com.axzae/swipelayout/1.3.0.

The manual changes are:
- Replaced the NuGet packages to be compatible with ```AndroidX``` and still have support from Microsoft (see https://developer.android.com/jetpack/androidx/migrate/artifact-mappings as orientation).
- Removed code from ```Metadata.xml``` according to the warnings (osolete code).
- Switched the namespaces for ```RecyclerView``` in ```Extras.cs``` from ```Android.Support.V7``` to ```AndroidX```.

All used components are available via the ```MIT``` license.
