# Stepper - Universal Stepper Motor Interface

[![crates.io](https://img.shields.io/crates/v/stepper.svg)](https://crates.io/crates/stepper)
[![Documentation](https://docs.rs/stepper/badge.svg)](https://docs.rs/stepper)
![CI Build](workflows/CI%20Build/badge.svg)

## About

**This library might not be suited for most projects these days. See _Status_
below.**

Stepper aims to provide an interface that abstracts over stepper motor drivers
and controllers, exposing high-level hardware features directly where available,
or providing software fallbacks where hardware support is lacking.

Right now, Stepper supports the following drivers:

- [A4988] ([crate][a4988-crate], [vendor documentation][a4988-doc])
- [DRV8825] ([crate][drv8825-crate], [vendor documentation][drv8825-doc])
- [STSPIN220] ([crate][stspin220-crate], [vendor documentation][stspin220-doc])

[A4988]: https://www.allegromicro.com/en/products/motor-drivers/brush-dc-motor-drivers/a4988
[a4988-crate]: https://crates.io/crates/a4988
[a4988-doc]: https://www.pololu.com/file/0J450/A4988.pdf
[DRV8825]: https://www.ti.com/product/DRV8825
[drv8825-crate]: https://crates.io/crates/drv8825
[drv8825-doc]: https://www.ti.com/lit/ds/symlink/drv8825.pdf
[STSPIN220]: https://www.st.com/en/motor-drivers/stspin220.html
[stspin220-crate]: https://crates.io/crates/stspin220
[stspin220-doc]: https://www.st.com/resource/en/datasheet/stspin220.pdf

Please refer to the [API Reference](https://docs.rs/stepper) or one of the
following guides to learn more:

- [How to Write a Driver](/documentation/how-to-write-a-driver.md)
- [Platform Support Guide](documentation/platform-support.md)

## Status

Stepper has only been passively maintained for many years now. While there have
been some contributions over those years, it seems to increasingly fall into
disrepair.

I recommend that you look at other options before using this library. There
might be better ones out there these days. If you still decide to use Stepper,
make sure to check the
[issue tracker](https://github.com/braun-embedded/stepper/issues) first.

Pull requests to fix any problems are still welcome.

## Usage

Stepper is a library written in Rust and designed for use in Rust projects. It
will run on any platform supported by Rust, including microcontrollers.

Add Stepper to your `Cargo.toml` like this:

```toml
[dependencies.stepper]
version = "0.5" # make sure this is the latest version
```

If you just need to use a specific stepper driver, you can also depend on the
crate for that specific driver. For example:

```toml
[dependencies.drv8825]
version = "0.5" # make sure this is the latest version
```

Please refer to the [API Reference] for more information.

## License

This project is open source software, licensed under the terms of the
[Zero Clause BSD License] (0BSD, for short). This basically means you can do
anything with the software, without any restrictions, but you can't hold the
authors liable for problems.

See [LICENSE.md] for full details.

[RampMaker]: https://crates.io/crates/ramp-maker
[API Reference]: https://docs.rs/stepper
[Zero Clause BSD License]: https://opensource.org/licenses/0BSD
[LICENSE.md]: LICENSE.md
[@hannobraun]: https://github.com/hannobraun
[@jessebraham]: https://github.com/jessebraham
