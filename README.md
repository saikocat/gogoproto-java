[![](https://jitpack.io/v/saikocat/gogoproto-java.svg)](https://jitpack.io/#saikocat/gogoproto-java)

# Gogoproto Java Packaging
Generate Java package for the [Gogoproto](https://github.com/gogo/protobuf)
protobuf (importing `gogoproto/gogo.proto`). Gofast doesn't support Java yet.

# Usage
* Directly link to [Sonatype](https://ossindex.sonatype.org/component/pkg:maven/com.github.saikocat/gogoproto-java@1.0.1)
  and [Maven](https://repo1.maven.org/maven2/com/github/saikocat/gogoproto-java/)
    * Maven:
```
<dependency>
  <groupId>com.github.saikocat</groupId>
  <artifactId>gogoproto-java</artifactId>
  <version>1.0.1</version>
</dependency>
```
    * Gradle:
```
implementation group: 'com.github.saikocat', name: 'gogoproto-java', version: '1.0.1'
```
* Using [Jitpack](https://jitpack.io) as resolver, and add `com.github.saikocat:gogoproto-java:1.0.1-jitpack` as a dependency. [Full instructions](https://jitpack.io/#saikocat/gogoproto-java/1.0.1-jitpack)

# Reason for yet another gogoproto-java
* As of the time of writing, there are 4 projects on Maven Central. 1 has extra
  bundles of non-protobuf related jars, 1 required appending additional repo url
  , 2 is using outdated protobuf runtime dependency. Can't find the scm to make
  a PR.
* Outdated protobuf runtime dependency (<3.8.0) causes compilation error so we
  bumped up the dependency for protobuf runtime.
```
error: cannot find symbol
      UnusedPrivateParameter unused) {
      ^
  symbol:   class UnusedPrivateParameter
  location: class MyType
```
* Work on using Jitpack and Maven Central without appending additional repo url.
