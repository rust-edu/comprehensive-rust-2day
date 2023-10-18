# Comprehensive Rust 🦀

This repository is a fork of the source code for
Comprehensive Rust 🦀, a multi-day Rust course developed by
the Android team. The course covers all aspects of Rust,
from basic syntax to generics and error handling. This
experimental fork is intended to be taught in just two
days. As such, it omits some material and zooms over other.

Read the course at **https://rust-edu.github.io/comprehensive-rust-2day/**.

## Course Format and Target Audience

The three-day version of this course is used internally at
Google when teaching Rust to experienced software
engineers. They typically have a background in C++ or Java.

The course is taught in a classroom setting and we hope it
will be useful for others who want to teach Rust to their
team. The course will be less useful for self-study since
you miss out on the discussions happening in the
classroom. You don't see the questions and answers and you
don't see the compiler errors we trigger when going through
the code samples. We hope to improve on this via [speaker
notes](https://github.com/google/comprehensive-rust/issues/53)
and by [publishing
videos](https://github.com/google/comprehensive-rust/issues/52).

## Building

The course is built using a few tools:

- [mdbook](https://github.com/rust-lang/mdBook)
- [mdbook-svgbob](https://github.com/boozook/mdbook-svgbob)
- [mdbook-i18n-helpers](https://github.com/google/mdbook-i18n-helpers)
- [mdbook-exerciser](mdbook-exerciser/)
- [mdbook-course](mdbook-course/)

First clone the repository:

```shell
git clone https://github.com/google/comprehensive-rust/
cd comprehensive-rust
```

Then install these tools with:

```shell
cargo install mdbook
cargo install mdbook-svgbob
cargo install mdbook-i18n-helpers
cargo install --path mdbook-exerciser
cargo install --path mdbook-course
```

Run

```shell
mdbook test
```

to test all included Rust snippets. Run

```shell
mdbook serve
```

to start a web server with the course. You'll find the content on
<http://localhost:3000>. You can use `mdbook build` to create a static version
of the course in the `book/` directory. Note that you have to separately build
and zip exercises and add them to `book/html`. To build any of the translated
versions of the course, run `MDBOOK_BOOK__LANGUAGE=xx mdbook build -d book/xx`
where `xx` is the ISO 639 language code (e.g. `da` for the Danish translation).
[TRANSLATIONS.md](TRANSLATIONS.md) contains further instructions.

> **Note** On Windows, you need to enable symlinks
> (`git config --global core.symlinks true`) and Developer Mode.

## Contact

For questions or comments on this forked course, please
contact [Bart Massey](bart@rust-edu.org) or start a
[discussion on
GitHub](https://github.com/rust-edu/comprehensive-rust-2day).
We would love to hear from you.
