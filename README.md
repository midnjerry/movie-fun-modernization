# Movie Fun!

Smoke Tests require server running on port 8080 by default.

## Build WAR ignoring Smoke Tests

```
$ mvn clean package -DskipTests -Dmaven.test.skip=true
```

## Run Smoke Tests against specific URL

```
$ MOVIE_FUN_URL=http://moviefun.example.com mvn test
```

## Convering from Maven to Gradle

1.) Create a Gradle Wrapper which creates `./gradle` and `gradle.bat`

(Gradle must be installed on machine)
```
gradle wrapper --gradle-version ${version} --distribution-type all
```

2.) Create `build.gradle` automatically pulling dependencies from `pom.xml`
```
./gradlew init
```

3.) Update .gitignore to ignore `.gradle/` folder

4.) Delete `pom.xml` and `.idea` folder.  Reopen in IntelliJ.