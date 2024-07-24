# Huffman Encoding/Decoding Project

## Overview

This project implements the Huffman encoding and decoding algorithm in C++. Huffman coding is a popular method used for lossless data compression, where the most frequent characters are represented with the shortest binary codes.

## Project Structure

- **code/** - Directory containing the source code. It have these files:
  - `Bin.bin` - The binary file containing the encoded data.
  - `Decompress.txt` - The decompressed output after decoding.
  - `Huffman.vcxproj` - Visual Studio project file.
  - `Huffman.vcxproj.filters.txt` - Filters for the Visual Studio project.
  - `Huffman.vcxproj.user` - User-specific project settings for Visual Studio.
  - `input.txt` - The input text file to be encoded.
  - `Source.cpp` - The main source code file containing the implementation of the Huffman algorithm.
  - `tree.txt` - A file containing the Huffman tree structure used in encoding.
  - `Use.txt` - A file explaining how to use the program.
- **Huffman.sln** - The Visual Studio solution file for the project.

## How to Use

1. **Building the Project:**
   - Open `Huffman.sln` in Visual Studio.
   - Build the solution to compile the project.

2. **Running the Project:**
   - Run the compiled executable. The program reads from `input.txt`, encodes the content, and outputs the encoded data to `Bin.bin`.
   - After encoding, you can run the decoder to read `Bin.bin` and generate the original text in `Decompress.txt`.

3. **Files Generated:**
   - `Bin.bin` - Contains the binary encoded output.
   - `Decompress.txt` - Contains the decoded text, which should match the original input.

## Code Explanation

The `Source.cpp` file implements the following:

- **Huffman Node Structure:**
  - Represents each character and its frequency in the input text.
  - Contains pointers to left and right children, representing the Huffman tree.

- **Huffman Class:**
  - Manages the Huffman tree and encoding/decoding processes.
  - Includes methods to calculate character frequencies, build the Huffman tree, generate codes, and encode/decode text.

- **Main Methods:**
  - `CalFreq()`: Calculates the frequency of each character.
  - `BuildTree()`: Builds the Huffman tree based on character frequencies.
  - `GenCode()`: Generates the binary code for each character.
  - `Encode()`: Encodes the input text using the generated codes.
  - `Decod()`: Decodes the binary data back to the original text.

## Notes

- Ensure that the `input.txt` file is present in the `code/` directory before running the program.
- The program is designed to work with ASCII characters.
- The  `txt` files uses the git lfs for manage larger text files support on github. It is downloaded by default on newer versions of git, but if you want to do it then run:
```bash
git lfs pull
```
- This will fetch all the *larger text* files in the repo.