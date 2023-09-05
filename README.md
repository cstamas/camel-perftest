# Resolver changes test

apache Camel https://github.com/apache/camel  
Commit building 3d3a687e0ceb749791bb96d6aaf498454e064ff2

```diff
diff --git a/.mvn/extensions.xml b/.mvn/extensions.xml
index 594ee3553dc..8d37a146c16 100644
--- a/.mvn/extensions.xml
+++ b/.mvn/extensions.xml
@@ -5,4 +5,14 @@
         <artifactId>cq-alias-fastinstall-quickly-extension</artifactId>
         <version>4.4.2</version>
     </extension>
+    <extension>
+        <groupId>io.takari.maven</groupId>
+        <artifactId>maven-timeline</artifactId>
+        <version>1.8</version>
+    </extension>
+    <extension>
+        <groupId>io.takari.maven</groupId>
+        <artifactId>takari-smart-builder</artifactId>
+        <version>0.6.3</version>
+    </extension>
 </extensions>
```
Local MRM: Proximity primed (no internet access).

Command:
```
mvn -Dmaven.repo.local=local clean install -Dquickly -b smart -T4
```

## Maven 3.9.4 "baseline"

```
[cstamas@urnebes camel (main *%)]$ mvn -v
Apache Maven 3.9.4 (dfbb324ad4a7c8fb0bf182e6d91b0ae20e3d2dd9)
Maven home: /home/cstamas/.sdkman/candidates/maven/current
Java version: 17.0.8.1, vendor: Eclipse Adoptium, runtime: /home/cstamas/.sdkman/candidates/java/17.0.8.1-tem
Default locale: en_US, platform encoding: UTF-8
OS name: "linux", version: "6.4.13-200.fc38.x86_64", arch: "amd64", family: "unix"
[cstamas@urnebes camel (main *%)]$ 
```

Results:
* Primed local repository: [link](baseline-3.9.4-elr/timeline.html)
* Empty local repository: TBD

