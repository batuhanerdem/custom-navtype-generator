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
You can check [this](https://github.com/batuhanerdem/WeatherApp). project as as example.
