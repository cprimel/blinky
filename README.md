# Blinky

[![Generic badge](https://img.shields.io/badge/Status-Completed-green)](https://shields.io/)

It's an LED! It blinks! That's it!

## Table of Contents
* [Setup](#setup)
* [References](#references)

## Setup

Things you need before getting started:
* Raspberry Pi 3
* a mircoSD card
* a breadboard
* a CP2102 USB TTL adapter
* 2x male-female jumper cables
* 1x resistor (any)
* 1x LED

For detailed instructions, check out the original [assignment from the 2015 course website](https://cs140e.sergio.bz/assignments/0-blinky/).

I have updated the provided code for ```phase4``` to successfully cross-compile the project for the RPi3. In short, the instructions linked above use the sysroot manager
[```xargo```](https://github.com/japaric/xargo) which has been in maintenance mode since 2017.
It was succeeded by [```cargo-xbuild```](https://github.com/rust-osdev/cargo-xbuild), a fork of
```xargo```, whose features have been incorporated into Cargo as
[the ```build-std``` feature](https://doc.rust-lang.org/nightly/cargo/reference/unstable.html#build-std). Mostly, just flip out one for the other and the compiler errors will lead you to the rest of it! You will also have to make some minor changes 
to the provided code for the current build of Rust. Check out my changes to ```makefile```, ```panic_handler``` in ```lang_items.rs```,
and feature flags in ```lib.rs```.

## References

1. CS140e, [An Experimental Course on Operating Systems](https://cs140e.sergio.bz/). Sergio Benitez (instructor), Dawson Engler (instructor) and Jennifer Lin (teaching assistant).