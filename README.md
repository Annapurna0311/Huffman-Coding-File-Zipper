# Huffman-Coding-File-Zipper
#### Overview
This project uses Huffman Coding, a lossless compression algorithm, to compress and decompress text files.

#### Node Structure
A `Node` in the Huffman Tree contains:
- Character data
- Frequency of the character
- Huffman code
- Pointers to left and right child nodes

#### Huffman Class
The `Huffman` class includes:
- Constructor: Accepts input and output file names
- `compress()`: Compresses the input file
- `decompress()`: Decompresses the Huffman coded file
![image](https://github.com/user-attachments/assets/31e7fe05-2123-48e7-919b-0d601040c694)

#### Compression Steps (`compress()`)
1. **createMinHeap()**: Reads the input file, calculates character frequencies, and creates a Min Heap.
2. **createTree()**: Builds the Huffman tree using the Min Heap.
3. **createCodes()**: Traverses the Huffman tree to assign binary codes to characters.
4. **saveEncodedFile()**: Saves the encoded file with Huffman codes and the encoded input file.
![image](https://github.com/user-attachments/assets/1ddd9e96-2428-4881-9d72-9edceeac73f6)

#### Decompression Steps (`decompress()`)
1. **getTree()**: Reconstructs the Huffman tree from the encoded file.
2. **saveDecodedFile()**: Reads the encoded input file, converts Huffman codes back to characters, and saves the original file.
![image](https://github.com/user-attachments/assets/0696a17a-2dac-478c-aa92-22e2d9a75e4d)

# Result 
![image](https://github.com/user-attachments/assets/c162ba1c-e3f3-4d02-9973-6415dba3dda6)
![image](https://github.com/user-attachments/assets/f169ed91-5525-4e9d-a16e-1f03f2b4a70b)
![image](https://github.com/user-attachments/assets/6758008a-f37f-4aa3-93f0-6ddbb0c40163)

This project is just an implementation of Huffman coding, it is not as efficient as the compression algorithm used currently to compress files.
Example: inputFile.txt (2.2MB) is compressed to compressedFile.huf (1.1MB) file and decompressed back to ouputFile.txt (2.2MB).
