# Errors For Scala Cats Instances #

# ScalaDoc #

[The Scaladoc for errors4s-core may be viewed here][javadoc].

[javadoc]: https://www.javadoc.io/doc/org.errors4s/errors4s-core-cats_3/1.0.0.0/index.html "Scaladoc"

# Overview #

This project provides [cats][cats] typeclass instances for [errors4s-core][errors4s-core] types.

[cats]: https://github.com/typelevel/cats "Cats"
[errors4s-core]: https://github.com/errors4s/errors4s-core "Errors4s Core"

## Using ##

Add this to your `libraryDependencies` in your `build.sbt`.

```scala
    "org.errors4s" %% "errors4s-core-cats" % "1.0.0.0"
```

```scala
import cats._
import cats.syntax.all._
import org.errors4s.core._
import org.errors4s.core.cats.instances._

val nes: NonEmptyString = NonEmptyString("A nonempty string")
// nes: NonEmptyString = A nonempty string

nes.show
// res0: String = A nonempty string

nes === nes
// res1: Boolean = true

nes < nes
// res2: Boolean = false
```

# Version Support Matrix #

This project uses [Package Versioning Policy (PVP)][pvp]. This is to allow long term support (see [this discussion][errors4s-core-pvp]). This table lists the currently supported, upcoming, and recently end of life versions.

If you need support for a version combination which is not listed here, please open an issue and we will endeavor to add support for it if possible.

|Version|Errors4s Core|Cats Version|Scala 2.11|Scala 2.12|Scala 2.13|Scala 3.0|
|-------|:-----------:|:----------:|:--------:|:--------:|:--------:|:-------:|
|1.0.x.x|1.0.x.x      |2.x.x       |No        |Yes       |Yes       |Yes      |

[pvp]: https://pvp.haskell.org/ "PVP"
[errors4s-core-pvp]: https://github.com/errors4s/errors4s-core#versioning "Errors4s Core: Versioning"
[semver]: https://semver.org/ "Semver"
