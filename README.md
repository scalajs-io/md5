MD5 API for Scala.js
================================
This is a Scala.js type-safe binding for [MD5](https://www.npmjs.com/package/md5)

A JavaScript function for hashing messages with MD5.

#### Build Dependencies

* [ScalaJs.io v0.3.x](https://github.com/ldaniels528/scalajs.io)
* [SBT v0.13.13](http://www.scala-sbt.org/download.html)

#### Build/publish the SDK locally

```bash
 $ sbt clean publish-local
```

#### Running the tests

Before running the tests the first time, you must ensure the npm packages are installed:

```bash
$ npm install
```

Then you can run the tests:

```bash
$ sbt test
```

#### Examples

Convert a string to MD5:

```scala
assert(MD5("Hello Wold") == "7e1c79bda939ad9f46a382a56df147e1")
```

Convert a buffer to MD5:

```scala
val buffer = Buffer.from("Hello Wold")
assert(MD5(buffer) == "7e1c79bda939ad9f46a382a56df147e1")
```

#### Artifacts and Resolvers

To add the Moment binding to your project, add the following to your build.sbt:  

```sbt
libraryDependencies += "io.scalajs.npm" %%% "md5" % "0.3.0.3"
```

Optionally, you may add the Sonatype Repository resolver:

```sbt   
resolvers += Resolver.sonatypeRepo("releases") 
```