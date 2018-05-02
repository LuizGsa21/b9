<figure class="image">
  <img src="{{"/docs/assets/images/logoREADME.png" width="100%"/>
</figure>

# Welcome to base9!

[![Build Status](https://api.travis-ci.org/b9org/b9.svg?branch=master)](https://travis-ci.org/b9org/b9)
[![Coverage Status](https://coveralls.io/repos/github/b9org/b9/badge.svg?branch=master)](https://coveralls.io/github/b9org/b9?branch=master)

Base9 is an educational language runtime and programming language! We’re using it to show people how to use [Eclipse OMR] to build their own language runtime with a Just in Time (JIT) Compiler! The base9 front-end language is a simple subset of JavaScript. For more information, visit the [base9 website].

[Eclipse OMR]: https://github.com/eclipse/omr
[base9 website]: https://www.base9.xyz

## Build your own Language Runtime

If you'd like to build your own language runtime, visit our guide on [Building a Language Runtime]!

[Building A Language Runtime]: https://www.base9.xyz/build-a-runtime

## Getting started

This page contains some basic instructions to get you started. For more detailed instructions, go to:

* [Ubuntu set-up page](./docs/setup/ubuntu.md).
* [OSX set-up page](./docs/setup/osx.md).

### 1. Requirements

To get started with base9 using the Ninja build system, you'll need the following:

* `git`
* `build-essential`
* `nodejs` **(Minimum version 4.5.0)**
* `npm`
* `esprima`
* `cmake` **(Minimum version 3.2.0)**
* `ninja`

### 2. Clone the repository and get the submodules

```sh
git clone --recursive https://github.com/b9org/b9.git
```

### 3. Install Esprima

```sh
cd b9 \
&& npm install esprima
```

### 4. Build base9

```sh
mkdir build \
&& cd build \
&& cmake -GNinja -DCMAKE_BUILD_TYPE=Debug .. \
&& ninja
```

### 5. Run Hello World!

In the `build` directory, run:

```sh
./b9run/b9run ./test/hello.b9mod
```

### 6. Test base9

You can run the full base9 test suite with:

```sh
ninja test
```
