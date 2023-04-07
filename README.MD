Rust Clock Utility
==================

A simple command-line utility to get and set the system time. The program is written in Rust and uses the `chrono`, `clap`, `byteorder`, and platform-specific libraries to interact with the system time.

Features
--------

* Get the current system time
* Set the system time
* Check the system time against NTP servers

Usage
-----

```bash
# clock --help
Usage: clock [OPTIONS] [ACTION] [DATETIME]

Arguments:
  [ACTION]    Action to perform [default: get] [possible values: get, set, check]
  [DATETIME]  When <action> is 'set', apply <datetime>. Otherwise, ignore.

Options:
  -s, --std <STD>  Time standard to use [default: rfc3339] [possible values: rfc2822, rfc3339, timestamp]
  -h, --help       Print help
  -V, --version    Print version
```

Dependencies
------------

* `chrono` for date and time manipulation
* `clap` for command-line argument parsing
* `byteorder` for byte order manipulation
* Platform-specific libraries (`libc` for Unix, `kernel32` and `winapi` for Windows) for system time interaction

Example
-------

Get the current time in RFC3339 format:

bash

```bash
clock
```

Set the system time using an RFC3339 formatted date-time string:

```bash
rust -a set -s rfc3339 "2023-04-03T10:30:00Z"
```

Disclaimer
----------

This package is for educational purposes only and is the result of following the Rust in Action book by Tim McNamara. It is not intended for production use or as a complete, robust solution for managing system time. Users should exercise caution and understand the implications of modifying system time before using this code. The author of this package and the creators of the Rust in Action book shall not be held responsible for any unintended consequences or damages resulting from the use of this package.
