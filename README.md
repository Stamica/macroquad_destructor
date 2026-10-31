# macroquad_destructor

[![Github Actions](https://github.com/not-fl3/macroquad/workflows/CI/badge.svg)](https://github.com/not-fl3/macroquad/actions?query=workflow%3A)
[![Docs](https://docs.rs/macroquad/badge.svg?version=0.4.5)](https://docs.rs/macroquad/0.4.5/macroquad/index.html)
[![Crates.io version](https://img.shields.io/crates/v/macroquad.svg)](https://crates.io/crates/macroquad)
[![Discord chat](https://img.shields.io/discord/710177966440579103.svg?label=discord%20chat)](https://discord.gg/WfEp6ut)

`macroquad` is a simple and easy to use game library for Rust programming language, heavily inspired by [raylib](https://github.com/raysan5/raylib).

This is a fork of [macroquad](https://github.com/not-fl3/macroquad) v0.4.16 aimed at adding a method to display the UI at will instead of at the end of a frame. This is done with using [egui_macroquad](https://github.com/optozorax/egui-macroquad) in mind and egui-related crates. 

This fork is _destructored, meaning it is aimed at the [_destructor project](https://git.aliens-lyon.fr/ahennet/blettes_destructor) which is currently private. 

Changes on this fork are as follow:
- added a bool in `Context` struct defined in `lib.rs`: `ui_flushed`
- added function `draw_ui()` which flushes the UI and renders it. Flags `ui_flushed`.
- added a `ui_flushed` condition inside of `end_frame()` in `lib.rs` to not dump the flushed ui.
