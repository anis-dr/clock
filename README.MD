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

```vbnet
USAGE:
    rust_clock [FLAGS] [OPTIONS] [datetime]

FLAGS:
    -h, --help       Prints help information
    -V, --version    Prints version information

OPTIONS:
    -a, --action <action>    Action to perform [default: get]
    -s, --std <std>          Time standard to use [default: rfc3339]

ARGS:
    <datetime>    When <action> is 'set', apply <datetime>. Otherwise, ignore.
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
