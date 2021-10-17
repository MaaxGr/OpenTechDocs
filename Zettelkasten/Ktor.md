# Base Dependencies
https://ktor.io/docs/gradle.html

```
implementation("io.ktor:ktor-server-core:1.6.4") 
implementation("io.ktor:ktor-server-netty:1.6.4") implementation("ch.qos.logback:logback-classic:1.2.5")
```

# Basic Structure
````
embeddedServer(Netty, port = 8080) {  

}.start(true)
```