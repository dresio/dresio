# Hello

![](https://img.shields.io/badge/OS-Linux-informational?style=flat&logo=linux&logoColor=white&color=2bbc8a)
![](https://img.shields.io/badge/Code-C++-informational?style=flat&logo=C&logoColor=white&color=2bbc8a)
![](https://img.shields.io/badge/Code-Rust-informational?style=flat&logo=rust&logoColor=white&color=2bbc8a)
![](https://img.shields.io/badge/Code-Python-informational?style=flat&logo=python&logoColor=white&color=2bbc8a)
![](https://img.shields.io/badge/Code-Make-informational?style=flat&logo=cmake&logoColor=white&color=2bbc8a)
![](https://img.shields.io/badge/Shell-Bash-informational?style=flat&logo=gnu-bash&logoColor=white&color=2bbc8a)

## About me
I currently work developing autonomy software for underwater platforms, developing simulations, and working on getting further into AI and perception development, while also learning more low level processes to interface with hardware.
In my spare time I develop smaller robotic systems and other peripherals such as keyboards. This page is to focus and highlight the smaller hobby based projects I am developing.


# Projects

## [Blank](https://github.com/dresio/blank)
A cross-platform AI simulation framework built in C++20 using WebGPU for rendering/compute. Blank is designed for high-performance physics-based reinforcement learning and robotics simulation. It features an ECS architecture, Velocity Verlet physics integration with TOI collision detection, and GPU-accelerated compute shaders for massively parallel environments. Batched parallelization enables running thousands of physics environments simultaneously, achieving 100-500x speedups for RL training with near-linear scaling. Includes Python bindings for integration with ML/RL frameworks.

## [Stryder](https://github.com/dresio/stryder)
A research project for training a transformer-based neural network policy to control an 8-DOF point-foot bipedal robot using reinforcement learning. Built on top of the Blank simulation engine, Stryder implements a student-teacher distillation approach: a teacher policy learns with full privileged state observations, while a student policy learns from realistic sensor data only (IMU + proprioception). The C++ side models joints, servo dynamics, and IMU simulation with domain randomization for sim-to-real transfer. The Python side handles RL training with PPO and behavior cloning, targeting real-time deployment on hardware.

## [Nexus](https://github.com/dresio/nexus)
A decentralized, self-sovereign communication platform built entirely in Rust. Nexus uses Ed25519 keypairs derived deterministically from username + password via Argon2id, requiring no registration, email, or phone number. The same credentials always produce the same cryptographic identity across all clients. The Rust workspace includes a WebSocket server (Axum + SQLite), a Tauri desktop app, all sharing the same core crypto library. Supports simple self-hosting via Docker.

## [Veritas](https://github.com/dresio/veritas) *(Replaced with Stryder)*
This project trained extremely small neural networks to perform tasks on embedded platforms for robotic systems. The model served as a drop-in replacement for an IK solver trained on a specific IK chain. With an input layer size of 3, 2 hidden layers with a size of 3xjoints, and an output layer size of the number of joints, a 3 DOF leg had only 25 nodes and executed around 15x faster than traditional IK solvers. 
