
# Task Snippets
## Build JAR with Manifest
```
tasks.withType<Jar>() {  
 duplicatesStrategy = DuplicatesStrategy.EXCLUDE  
 manifest {  
   attributes("Main-Class" to "MainKt")  
 }  
  
 from(configurations.runtimeClasspath.get().map { if (it.isDirectory) it else zipTree(it) })  
}
```

## Change working directory 
```
tasks.named<JavaExec>("run") {  
    workingDir = File("${projectDir.absolutePath}/run")  
}
```