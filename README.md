# Huffman Code Compressor

I worked on this Java coursework project to understand how Huffman coding turns symbol frequencies into variable-length bit codes. The program compresses a file and reconstructs it through a matching decoding process.

## What it does

- Build a frequency table and Huffman tree from file contents.
- Encode and decode files, including an end-of-file marker.
- Read and write individual bits through buffered byte streams.
- Support individual encode/decode operations and batches from a test file.
- Include sample inputs for inspecting the compression workflow.

## Project context and attribution

This is an academic implementation built on course material. The Huffman source credits **Lucia Moura (2021)**. The bundled `net.datastructures` library credits **Michael T. Goodrich, Roberto Tamassia, and Michael H. Goldwasser**, from *Data Structures and Algorithms in Java*, Sixth Edition.

The bundled data-structures files retain their original GPL notices. Course and library credits are preserved in the source headers, alongside the repository's [LICENSE](LICENSE) file.
