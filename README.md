
# Project 7: IoT Setup with ESP32 and Raspberry Pi 4 (Rust Version)

**Final Part of my IoT Lab Series using ESP32 and Raspberry Pi 4**

## Overview

This project is a Rust re-implementation of my initial IoT setup.  
It covers setting up the development environment, flashing programs to the ESP32, and running a simple application using Rust for embedded systems.  
The goal is to explore the capabilities of Rust in embedded development and compare it to the original C++ implementation.

## Objectives

- ✅ Set up Rust environment for ESP32 development
- ✅ Connect Raspberry Pi 4 and ESP32 for programming
- ✅ Build and flash Rust-based embedded applications
- ✅ Run "Hello World" application in Rust on ESP32
- ✅ Document the Rust setup and environment differences from C++

## Project Structure

esp32-lab7-iot-setup-rust/  
├── report.pdf # Lab report (required)  
├── raspberry-pi-setup/ # Raspberry Pi setup notes and configs  
├── esp32-hello-world-rust/  
│ ├── Cargo.toml  
│ ├── rust-toolchain.toml  
│ └── src/  
│ └── main.rs  
├── README.md  

## Setup Instructions

### 🦀 Rust Environment Setup

1. Install Rust toolchain:
curl https://sh.rustup.rs -sSf | sh

2. Add the Xtensa Rust target:
rustup target add xtensa-esp32-espidf

3. Install ESP-IDF:
Refer to the official Espressif Rust documentation:
https://esp-rs.github.io/book/installation/index.html

4. Set environment variables:
source export-esp.sh

### ⚙️ ESP32 Programming with Rust

1. Clone the repository and navigate to the Rust project directory:
cd esp32-hello-world-rust

2. Build the project:
cargo build --release

3. Flash to ESP32:
cargo espflash /dev/ttyUSB0 --release

4. Monitor output:
cargo run --release

## Notes

- Exclude target/ directories when zipping the project.
- Submit the required files and directories: esp32-hello-world-rust/*, report.pdf
- Document issues or learnings in report.pdf and README.md
- All external code must follow APACHE or BSD-like licenses.
- Reference any helpful resources properly in report.pdf (No StackOverflow, Reddit).

## What I Learned

- Setting up Rust for embedded development on ESP32
- Flashing and running Rust applications on embedded hardware
- Comparing Rust and C++ workflows in embedded systems
- Understanding benefits and trade-offs of Rust in low-level development

## Future Improvements

- Implement additional sensor readings in Rust
- Add display output integration
- Explore advanced concurrency features of Rust
- Build more complex IoT applications in Rust

## License
This project is for educational purposes.

Previous Project: [ESP32 Ultrasonic Range Finder](https://github.com/Inhle-C/Project-6-esp32-lab6-ultrasonic-sensor)  
(Part 6 of the series)

This is the final part of my IoT Lab Series 🚀
