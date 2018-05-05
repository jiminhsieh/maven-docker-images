# [Maven Docker images](https://hub.docker.com/r/jiminhsieh/maven/)

[![Build Status](https://travis-ci.org/jiminhsieh/maven-docker-images.svg?branch=master)](https://travis-ci.org/jiminhsieh/maven-docker-images)
[![](https://img.shields.io/docker/pulls/jiminhsieh/maven.svg)](https://hub.docker.com/r/jiminhsieh/maven/)
[![](https://img.shields.io/docker/stars/jiminhsieh/maven.svg)](https://hub.docker.com/r/jiminhsieh/maven/)


## Why another Gradle Docker images?

The reasons I make those Docker images:

* It will be great to use JVM that passed [TCK/JCK](https://en.wikipedia.org/wiki/Technology_Compatibility_Kit).
* [AdoptedOpenJDK's OpenJ9 was just passed TCK/JCK](https://blog.adoptopenjdk.net/2018/03/jck-certification-and-an-anniversary-of-sorts). We should give it a try.

## Which JVM do those images use?

* [Azul Zulu](https://www.azul.com/products/zulu-and-zulu-enterprise/)
* [Eclipse OpenJ9](https://www.eclipse.org/openj9/)

## Naming convention of those Docker tags
* {jvm}_{jvm.major}-{maven.major}.{maven.minor}
    * e.g. **zulu_8-3.3**
* {jvm}_{jvm.major}u{jvm.minor}-{maven.full.version}
    * e.g. **openj9_8u162-3.3.9**

All of available Docker image tags you can find [here](https://hub.docker.com/r/jiminhsieh/maven/tags/).

## The base images I used
* [azul/zulu-openjdk](https://hub.docker.com/r/azul/zulu-openjdk/)
* [adoptopenjdk/openjdk8-openj9](https://hub.docker.com/r/adoptopenjdk/openjdk8-openj9/)

## TODO

* If AdoptedOpenJDK releases HotSpot's version that passes TCK in the future, I will add that too.
