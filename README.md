MD5 API for Scala.js
================================
[MD5](https://www.npmjs.com/package/md5) - js function for hashing messages with MD5

### Description

js function for hashing messages with MD5.

### Build Dependencies

* [SBT v0.13.13](http://www.scala-sbt.org/download.html)

### Build/publish the SDK locally

```bash
 $ sbt clean publish-local
```

### Running the tests

Before running the tests the first time, you must ensure the npm packages are installed:

```bash
$ npm install
```

Then you can run the tests:

```bash
$ sbt test
```

### Examples

Convert a string to MD5:

```scala
import io.scalajs.npm.md5._

MD5("Hello Wold") //=> 7e1c79bda939ad9f46a382a56df147e1
```

Convert a buffer to MD5:

```scala
import io.scalajs.nodejs.buffer.Buffer
import io.scalajs.npm.md5._

val buffer = Buffer.from("Hello Wold")
MD5(buffer) //=> 7e1c79bda939ad9f46a382a56df147e1
```

### Artifacts and Resolvers

To add the `MD5` binding to your project, add the following to your build.sbt:  

```sbt
libraryDependencies += "io.scalajs.npm" %%% "md5" % "0.4.0-pre3"
```

Optionally, you may add the Sonatype Repository resolver:

```sbt   
resolvers += Resolver.sonatypeRepo("releases") 
```