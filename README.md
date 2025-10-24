# Rust Simple Merkle Root Calculator

This repository presents a foundational implementation of a Merkle Tree Root calculator, written in **Rust**. Merkle Trees are essential cryptographic primitives used extensively in blockchain technologies (like verifying transaction sets, airdrop lists, and state proofs).

## Goal

* Demonstrate proficiency in Rust programming, focusing on secure byte manipulation and cryptographic hashing.
* Implement a core blockchain data structure (Merkle Tree) concept.
* Showcase a basic Rust project setup using `Cargo.toml` and external dependencies (`sha2` and `hex`).

## Program Functionality (`main.rs`)

The `calculate_merkle_root` function takes a vector of 32-byte hashes (leaves) and iteratively computes the tree's root hash.

* **Key Steps:**
    1.  Handles odd numbers of leaves by duplicating the last hash.
    2.  Hashes pairs of nodes to form the next level.
    3.  Follows a standard Merkle implementation by **lexicographically sorting** the paired hashes before combining and hashing them (ensuring canonical tree structure).

## Tech Stack

* **Language:** Rust (2021 Edition)
* **Build Tool:** Cargo
* **Dependencies:** `sha2` (for SHA-256 hashing) and `hex` (for output display).
* **Concepts:** Cryptographic Hashing, Data Structures, Merkle Trees.

## Running Locally

To compile and run this project, you must have the Rust toolchain (including Cargo) installed.

```bash
# Clone the repository
git clone [https://github.com/KZMKBL/rust-merkle-root-calculator.git](https://github.com/YOUR_GITHUB_USERNAME/rust-merkle-root-calculator.git)
cd rust-merkle-root-calculator

# Compile the project
cargo build

# Run the executable
cargo run

# Run the unit tests
cargo test
