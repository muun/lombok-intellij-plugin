1. Modify in `gradle.properties` and `build.gradle` the versions for IntelliJ and it's plugins

2. Run gradle wrapper with Java 14

```
JAVA_HOME=$(/usr/libexec/java_home -v 14) ./gradlew :buildPlugin
```

3. Upload it to AWS

```
aws-vault exec admin -- aws s3 cp build/distributions/lombok-plugin-0.36-${VERSION}.zip s3://muun-internal-assets/
```


