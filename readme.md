Negahban
========

🧐 A simple file watcher, based on `notify`, designed to be fast, easy-to-use and async friendly

[![MIT License](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/aarmn/negahban/blob/main/LICENSE)
[![Crates.io](https://img.shields.io/crates/v/negahban.svg)](https://crates.io/crates/negahban)
[![docs.rs](https://docs.rs/negahban/badge.svg)](https://docs.rs/negahban/)
<!-- [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT) -->
<!-- [![codecov](https://codecov.io/gh/aarmn/negahban/branch/main/graph/badge.svg?token=5DURCC65LH)](https://codecov.io/gh/aarmn/negahban) -->
<!-- [![Build Status](https://github.com/aarmn/negahban/actions/workflows/rust.yml/badge.svg)](https://github.com/aarmn/negahban/actions) -->
<!-- ![Rust Version](https://img.shields.io/badge/rust-1.67.0-orange.svg) -->

Overview 📊
--------

`negahban` is a Rust library based on `notify` that allows you to watch a directory for changes.

This library is designed to be:

*   Simple, Sane defaults ✅
*   Blazing Fast 🚀
*   Async friendly 🔀
*   Cross-platform 🌐

Features ✨
--------

*   Supports multiple event types such as file creation, deletion, and modification.
*   Provides `HookType`, `WatchMode`, and `RecurseMode` configuration options.
*   Can ignore specific files and directories.
*   Easy to use and async friendly.

Usage 🔨
-----

Add this to your `Cargo.toml`:

```toml
[dependencies]
negahban = "0.2.1"
```

A minimal example that monitors the current directory and logs events to the console:

```rust
use negahban::Negahban;
fn main() {
    Negahban {
        hook: Box::new(|event, _| println!("{:?}", event)),
        ..Negahban::default()
    }.run();
}
```

Examples 👨‍💻
--------

See the [`examples/`](https://github.com/aarmn/negahban/tree/main/examples) directory for more examples.

License ⚖
-------

This project is licensed under the MIT License - see the [LICENSE](https://github.com/aarmn/negahban/blob/main/LICENSE) file for details.