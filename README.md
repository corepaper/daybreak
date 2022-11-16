Rustbreak
=========

[![Crates Link](https://img.shields.io/crates/v/daybreak.svg)](https://crates.io/crates/daybreak)

**[Documentation][https://docs.rs/daybreak]**

This is a continuation of
[Rustbreak](https://github.com/TheNeikos/rustbreak) project, which was
archived. This is a Ruby `daybreak` inspired self-contained file
database. It is meant to be fast and simple to use. You add it to your
application and it should just work for you. The only thing you will
have to take care of is saving.

When to use it
--------------

This library started out because of a need to be able to quickly write
an application in rust that needed some persistence while still being
able to write arbitrary data to it.

In Ruby there is `daybreak` however for Rust there was no similar
crate, until now!

When not to use it
------------------

Rustbreak makes several trade-offs to be easy to use and extend, so
knowing of these drawbacks is important if you wish to use the
library:

- The Database needs to fit into memory (Rustbreak cannot do partial
  loads/saves, so if the Database exceeds your available memory you
  will run OOM)
- Not all backends support atomic saves, so if your program crashes
  while it is saving you might save incomplete data (Notably only
  PathBackend supports atomic saves)

Features
--------

- Simple To Use, Fast, Secure
- Threadsafe
- Serde compatible storage (ron, bincode, or yaml included)
