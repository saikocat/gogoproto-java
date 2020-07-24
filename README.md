# Gogoproto Java Packaging
Generate Java package for the [Gogoproto](https://github.com/gogo/protobuf)
protobuf (importing `gogoproto/gogo.proto`). Gofast doesn't support Java yet.

# Usage
* [IN PROGRESS] Using Maven repository
* Using [Jitpack](https://jitpack.io) as resolver, and add `com.github.saikocat:gogoproto-java:1.0.0` as a dependency. [Full instructions](https://jitpack.io/#saikocat/gogoproto-java/1.0.0)

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
