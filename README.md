This library designed to simplify the creation of custom navigation types for Jetpack Compose's navigation component. With this library, you can easily generate custom NavType classes that allow you to pass complex data types between composables in a type-safe manner using Compose Navigation.

# Step 1. Add the JitPack repository to your build file
Add it in your root build.gradle at the end of repositories:

	dependencyResolutionManagement {
		repositoriesMode.set(RepositoriesMode.FAIL_ON_PROJECT_REPOS)
		repositories {
			mavenCentral()
			maven { url 'https://jitpack.io' }
		}
	}

# Step 2. Add the dependency
 
	dependencies {
	        implementation 'com.github.batuhanerdem:custom-navtype-generator:v1.0.0'
	}

# Example Usage:

```kotlin
composable<Screens.ForecastScreen>(
            typeMap = mapOf(
                typeOf<List<DayUi>>() to serializeAnyType<List<DayUi>>()
            )
        )
```
You can check [this](https://github.com/batuhanerdem/WeatherApp) project as an example.
