Parallax Abstraction Layer
==========================

Language Agnostic API for P2 HAL Implementations

Introduction
------------

Wouldn't it be great if every (major/large) library for the Propeller 2 
implemented a similar API? Of course it would - then jumping from one language
to another would only be as hard as learning the new syntax rather than learning 
both a syntax and a new library API.

The Parallax Abstraction Layer aims to help make this happen by providing a
community-developed and language-agnostic API that hardware abstraction 
library (HAL) authors can use while implementing their designs.

There are two types of users for this repository: API designers and HAL 
authors. API designers will contribute their ideas to this repository and HAL
authors will take those ideas and turn them into executable code.

PAL Design & Architecture
-------------------

Designed with two layers in mind: HIL and HAL.

### Hardware Interface Layer

Low-level functions that interact directly with the hardware. These functions
provide little or no abstraction but are merely focused on giving high-level 
languages (anything other than assembly) access to the Propeller's special 
purpose registers.

### Hardware Abstraction Layer

Medium- and high-level functions that interact with either HIL or other HAL 
functions to accomplish high(er) level goals, such as "set the clock 
frequency" or "start a PWM signal."

### Object Hierarchy

Lines ending with `/` are categories. Those without are considered objects in
the API.

* `builtin/`
* `concurrency/`
* `filesystem/`
* `hmi/`
  * `input/`
  * `output/`
* `memory/`
* `motor/`
* `pins/`
* `sensor/`
  * `accelerometer/`
  * `analog/`
  * `distance/`
  * `gyroscope/`
  * `thermometer/`
* `bus/`
  * `can/`
  * `i2c/`
  * `spi/`
  * `uart/`

API Designers
-------------

Coming soon...

HAL Authors
-----------

Coming soon...
