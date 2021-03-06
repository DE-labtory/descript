# koa 
[![Build Status](https://travis-ci.org/DE-labtory/koa.svg?branch=master)](https://travis-ci.org/DE-labtory/koa)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0) [![Language](https://img.shields.io/badge/language-go-orange.svg)](https://golang.org) [![Coverage Status](https://coveralls.io/repos/github/DE-labtory/koa/badge.svg?branch=develop)](https://coveralls.io/github/DE-labtory/koa?branch=develop)

<img src="./image/koa-clip.gif" width="520px" height="320px">

The project is inspired by [the simplicity](https://blockstream.com/simplicity.pdf) and the [ivy-bitcoin](https://github.com/ivy-lang/ivy-bitcoin).

The koa project is to create a high-level language that has `more expressions` than the bitcoin script and 
is simpler and easy to analyze than soldity(ethereum).

<p align="center"><img src="./image/koa-concept.png" width="380px" height="300px"></p>

A more detailed explanation is given below.
- [Doc](https://github.com/DE-labtory/koa/blob/develop/docs/doc.md)

Also, koa project is published in [Mobisys 2019](https://www.sigmobile.org/mobisys/2019/)! You can see the paper and poster below.
###### **Title: "Demo: Light-Weight Programming Language for Blockchain"**
- [Paper](docs/MobiSys2019-demo-paper.pdf)
- [Poster](docs/MobiSys2019-demo-poster.pdf)

### Architecture

![koa architecture](image/koa-architecture.png)

- Lexer
- Parser
- Compiler
- VM

### Language Specification

#### Primitive Type
- Integer

  It is expressed in `int`. Integer size is 64 bytes.

- String

  It is expressed in `string`.

- Boolean

  It is expressed in `true` or `false`.

#### Operators
- Arithmetic

  We support `+, -, *, /, %` only for integer.

- Comparison

  We support `==, !=, >, <, >=, <=` for comparsion.

- Logical

  We support `&&, ||` for logical operation.

- Prefix

  We support `!, -` for prefix operator.

#### Condition
It is expressed in `if(){}` or `if(){}else{}`.

#### Etc
- `return`
- `\n` : All statements should end in `\n`.
- Assign : It is expressed in `=`.

#### Example Code
 ```go
contract {
  func Sig(sig string){
    string pubkey = "fvfidBGruUYC+mTw7CusaCOQbBuZBiYduFgH8hRW97KLmHn0xzB1FV++KI7syo8qXGo8Un24WP40IT78XjKO"
    
    if checkSig(pubkey, sig){
      return true
    }
    return false
  }
}
 ```

### Contribution
Contribution Guide
[CONTRIBUTION](CONTRIBUTING.md)

### License

Project source code files are made available under the Apache License, Version 2.0 (Apache-2.0), located in the [LICENSE](LICENSE).


### CLA Hub

To get started, <a href="https://www.clahub.com/agreements/DE-labtory/koa">sign the Contributor License Agreement</a>.
