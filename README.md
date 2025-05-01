# **Bash Learning Scripts**

This repository contains a collection of basic Bash scripts designed to help you learn and practice shell scripting. Each script has a specific function and demonstrates different aspects of Bash scripting such as file manipulation, text processing, and working with command-line arguments.

---

## **Scripts Overview**

### 1. **countlines.sh**
   - **Purpose**: This script counts the number of lines in one or more text files, differentiating between files with zero, one, or multiple lines.
   - **Usage**: 
     ```bash
     ./countlines.sh file1.txt file2.txt
     ```
   - **Description**: The script loops through the provided files, counts the lines in each file, and prints a message indicating whether the file has 0, 1, or more lines.

   - **Example**:
     ```bash
     file1.txt: The file has 5 lines
     file2.txt: The file has 1 line
     ```

---

### 2. **peek.sh**
   - **Purpose**: This script prints the first three and last three lines of a file, or a specified number of lines from both ends, with "..." in the middle if the file is large.
   - **Usage**:
     ```bash
     ./peek.sh filename.txt 5
     ```
   - **Description**: This script displays the first and last `N` lines of a file. If the file contains more than `2*N` lines, it shows "..." in the middle to indicate that lines in between are omitted.

   - **Example**:
     ```bash
     Warning: The file contains more than 5 lines
     First 5 lines of the file
     ...
     Last 5 lines of the file
     ```
---

### 3. **fastascan.sh**
   - **Purpose**: This script scans a folder for FASTA/FA files and generates a report including file details such as symlink status, number of sequences, and total sequence length. It also detects whether sequences are nucleotide or amino acid-based.
   - **Usage**:
     ```bash
     ./fastascan.sh /path/to/folder 10
     ```
   - **Description**: The script recursively searches a directory (or the current directory if none is specified) for `.fasta` or `.fa` files. It reports the number of files found, the total unique FASTA IDs, and for each file, the number of sequences, total sequence length, and sequence type (amino acid or nucleotide). It also prints the first and last `N` lines of the file (if applicable).

   - **Example**:
     ```bash
     FOLDER: /path/to/folder
     Number of FASTA/FA files: 5
     Number of unique FASTA IDs: 15
     ------------------------------------------------------------
     FILENAME: file1.fasta
     - Symlink: No
     - Number of sequences: 10
     - Total Sequence Length: 1234
     - Type: Aminoacid Sequence
     ```


### 4. **fastascan.ai.sh**
   - **Purpose**: An improved version of fastascan.sh, utilizing AI enhancements for better accuracy and efficiency.
   - **Usage**:
     ```bash
     ./fastascan.ai.sh /path/to/folder 10
     ```
   - **Description**: This script is similar to fastascan.sh but includes optimizations and improvements powered by AI methods to improve file scanning and sequence classification.

---

## **Installation**

1. **Clone the Repository**:
   To get started, clone this repository to your local machine using Git:
   ```bash
   git clone https://github.com/your-username/bash-learning-scripts.git
