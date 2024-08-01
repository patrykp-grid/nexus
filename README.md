### After installing nexus repository manager, I started it with the following command:


```bash
./nexus run
```

![nexus](images/nexus.png)

### Next I accessed user interface on http://localhost:8081:

![UI](images/nexus-ui.png)

### I logged in with the default credentials:

![login](images/nexus-login.png)

### Setting up a proxy repository

![proxy](images/nexus-proxy.png)

#### Maven proxy repository

![maven](images/nexus-maven.png)

updating .m2/settings.xml

![settings](images/settings.png)

#### Gradle configuration

build.gradle

```gradle
repositories {
    maven {
        url 'http://localhost:8081/repository/maven-public/'
    }
}
```

and added publish plugin

```gradle
apply plugin: 'maven-publish'
```


### Uploading maven artifact 

```bash
mvn deploy
```

![upload-mvn](images/upload-mvn.png)

### Uploading artifact using gradle

```bash
./gradlew publish
```








