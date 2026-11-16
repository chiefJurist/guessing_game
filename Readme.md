# Guessing Game

A small command-line number guessing game written in Rust, built while following Chapter 2 of *The Rust Programming Language* book. The program picks a random secret number between 1 and 100, asks you to guess it, and tells you whether your guess is too small, too big, or correct, repeating until you win.

## What it demonstrates

This project introduces core Rust basics: reading user input with `std::io`, generating random numbers with the external `rand` crate, comparing values with `std::cmp::Ordering` and the `cmp` method, branching with `match`, converting text into a `u32` with `parse`, and looping until the player guesses correctly.

## Requirements and setup

You need Rust and Cargo installed (get them from https://rustup.rs). Create the project with `cargo new guessing_game`, then add the `rand` crate by running `cargo add rand` inside the project folder, and replace the contents of `src/main.rs` with your game code.

## How to run

From the project folder, run `cargo run`. Cargo will download dependencies, compile the program, and start the game. Type a number and press Enter to guess, and the game will respond with "Too small!", "Too big!", or "You win!".

## Notes

The random number generator is local to the current thread and seeded by the operating system, so you get a different secret number on every run. Guesses are stored as `u32`, so negative numbers or non-numeric input are not valid guesses.