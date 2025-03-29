# Time Dilation ⏱️

A minimal, scoped timing utility for Rust.

## Overview

`time-dilation` provides a simple `ScopedTimer` struct that starts measuring time when it's created and stops when it goes out of scope (is dropped).

It leverages the RAII (Resource Acquisition Is Initialization) pattern: the timer resource is acquired on creation, and measurement implicitly ends when the resource is released (on drop).

Optionally, when the `enable_summary` feature is activated, the timer will automatically print a human-readable, color-coded summary of the elapsed time to the console when it is dropped.

## Features

* **Scoped Timing:** Automatically measures the duration of a code block using RAII.
* **Simple API:** Easy to use with `ScopedTimer::new("description")`.
* **Optional Summary:** Enable the `enable_summary` feature to automatically print elapsed time on drop.
* **Human-Readable Output:** Formats durations appropriately (ns, µs, ms, s).
* **Color-Coded Grading:** The optional summary includes a simple opinionated color grade (Great/Good/Warning/Bad) based on the duration.
* **Manual Measurement:** Get the current elapsed time anytime using `.elapsed()`.

## Installation

Add this to your `Cargo.toml`:

```toml
[dependencies]
time-dilation = "0.1.10"
```
