# Installing Java and Maven

There are many tutorials out there on how to install Java and Maven, but we’re going to add another one since they are required for following these tutorials.

## Installing Java

Maven requires Java to be installed so we’ll do that one first.

Note: At the time of this writing, the latest stable release of Java is 1.8.0_60.

### Windows

Check if you already have Java installed by opening up command prompt and running `java -version`. You should see something like this:

```console
C:\Users\username>java -version

java version "1.8.0_45"
Java(TM) SE Runtime Environment (build 1.8.0_45-b14)
Java HotSpot(TM) 64-Bit Server VM (build 25.45-b02, mixed mode)
```

As long as you have Java 1.7 or higher, you’ll be fine.

### OS X

Check if you already have Java installed by opening up a terminal window and running `java -version`. You should see something like this:

```bash
$ java -version

java version "1.8.0_05"
Java(TM) SE Runtime Environment (build 1.8.0_05-b13)
Java HotSpot(TM) 64-Bit Server VM (build 25.5-b02, mixed mode)
```

As long as you have Java 1.7 or higher, you’ll be fine.

If you don’t have Java installed, install Java with [Homebrew](http://brew.sh/). If you haven’t already, install Homebrew and run the following commands:

```bash
brew tap caskroom/cask
brew install brew-cask
brew cask install java
```

Because Java is installed for all users, you will need administrator access to complete the install.

(It’s a massive download (over 200MB) so it will take awhile.)

## Installing Maven

### Short Maven Overview

If you’ve used [NPM](https://www.npmjs.com/) or [Ant+Ivy](http://ant.apache.org/ivy/) or [Gradle](https://gradle.org/) or [NuGet](https://www.nuget.org/) or [Composer](https://getcomposer.org/) then know that Maven is similar to those tools. If you aren’t familiar with any of them then: Welcome to the world of dependency management!

Dependencies are libraries that your project *depends on* to run. For example, the FreeMarker library is a dependency of any webapp that wants to use FreeMarker to render a web page. If I am working on a FreeMarker website with another developer (or even a group of developers), it’s important that we all use the same version of FreeMarker. Without a tool to manage dependencies, we would have to manually keep all our libraries in sync (which is tedious and error-prone.)

Maven ensures developers working on a project together are using the same libraries with the same versions. It handles downloading dependencies and putting them in a consistent location where your Java compiler can find them. It is also used to bundle JAR and WAR files, and can be used to version your own projects.

By default Maven looks for a `pom.xml` file in the root of your project and runs commands based on what is in that file. You can tell Maven to run just about anything. The `pom.xml` file can also be split up into smaller files since xml files tend to become quite verbose.

### Windows

### OS X