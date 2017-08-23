# sbt-conflict-classes: List conflict classes in classpath  [![Build Status](https://secure.travis-ci.org/xuwei-k/sbt-conflict-classes.png?branch=master)](http://travis-ci.org/xuwei-k/sbt-conflict-classes)


## Usage

```scala
// project/plugins.sbt
addSbtPlugin("com.github.xuwei-k" % "sbt-conflict-classes" % "0.1.0")
```

```scala
// build.sbt

// Exclude from conflict detection(match with startsWith)(Optional)
conflictClassExcludes ++= Seq(
  "com/example/DuplicateClass.class",
  "com/example/dups/"
)
```

```
$ sbt compile:conflict-classes # show compile-time conflicts
$ sbt test:conflict-classes    # show test-time conflicts
$ sbt runtime:conflict-classes # show runtime conflicts
```
