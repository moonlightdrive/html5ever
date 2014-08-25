# html5ever

Very much a work in progress!

[![Build Status](https://travis-ci.org/kmcallister/html5ever.svg?branch=master)](https://travis-ci.org/kmcallister/html5ever)

html5ever is an HTML5 parser developed as part of the [Servo](https://github.com/servo/servo) project.

## Features / goals

* Provides a simple static parse tree, or works with your choice of DOM representation
* Suitable for use by a real web browser
* High-performance "unhosted" native code (no garbage collector, etc) with a C API usable from any language
* Written in the memory-safe [Rust](http://www.rust-lang.org/) programming language for speed and security
* UTF-8 parsing pipeline, with such workarounds as are needed to support UCS-2 `document.write`
* Concise, highly readable code which is cross-referenced with the WHATWG HTML syntax spec

For more details see the [design](https://github.com/kmcallister/html5ever/wiki/Design) page on the project wiki.

## Building it

The library itself builds using [Cargo](http://crates.io/), so you just run `cargo build` in the top directory.

Run `cargo doc` to build documentation under `target/doc/`.

To build examples, tests, and benchmarks, do something like

```
mkdir build
cd build
../configure
make examples check bench
```

This will invoke Cargo if necessary.
