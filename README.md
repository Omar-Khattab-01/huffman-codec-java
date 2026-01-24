# Huffman Code Compressor

A Java-based command-line utility that compresses and decompresses arbitrary files using Huffman coding, featuring a lightweight data-structures toolkit and ready-to-run sample workloads.

## Features
- Huffman encoding/decoding for text and binary files with end-of-file markers.
- Stream-based bit I/O for efficient packing/unpacking of compressed data.
- Command-line interface supporting single runs and batch scripts via test files.
- Sample corpus (text, images) and repeatable test script for quick verification.
- Clear byte-count reporting to compare compression ratios.

## Tech Stack
- **Backend:** Java (standard library), custom data-structures package for priority queues/trees.
- **Frontend:** CLI (no GUI layer).
- **Database:** None required.
- **Tools:** `javac`, standard JDK tooling; sample assets under `sample-data/`.

## Project Structure
- `src/main/java/Huffman.java` – Core encoder/decoder implementing Huffman trees and bit streams.
- `src/main/java/TestCompression.java` – CLI harness for encode/decode commands and batch runs.
- `src/main/java/net/datastructures/` – Minimal data-structure library (priority queues, trees) used by the codec.
- `sample-data/inputs/` – Ready-made text/image assets and `tests.txt` script for demonstrations.
- `sample-data/outputs/` – Generated artifacts from example runs (ignored by git; `.gitkeep` present).
- `docs/reference/` – Background material retained for internal context.
- `docs/screenshots/` – Placeholder folder for future UI/CLI screenshots.

## How to Run
Requirements: JDK 11+.

```bash
# Compile everything
mkdir -p build
javac -d build $(find src/main/java -name "*.java")

# Encode a file
java -cp build TestCompression E sample-data/inputs/genes.txt sample-data/outputs/genes.huf

# Decode a file
java -cp build TestCompression D sample-data/outputs/genes.huf sample-data/outputs/genesRecover.txt

# Run the bundled batch script
java -cp build TestCompression T sample-data/inputs/tests.txt
```
Running `java -cp build TestCompression` with no arguments executes a quick demo using `sample-data/inputs/ACTGhandout.txt` and writes outputs into `sample-data/outputs/`.

## What This Project Demonstrates
- Implementing Huffman coding with custom priority-queue and tree structures.
- Stream-oriented file handling and bit-level buffering in Java.
- Designing a small, testable CLI workflow with batch automation.
- Organizing sample data and documentation for reproducible results.

## Future Improvements
- Package as a reusable library (Jar) with versioned releases.
- Add JUnit tests and CI workflow for automated verification.
- Include compression benchmarks and ratio reporting across datasets.
- Provide screenshots or asciicasts in `docs/screenshots/` demonstrating CLI usage.

## Author
Omar Khattab
