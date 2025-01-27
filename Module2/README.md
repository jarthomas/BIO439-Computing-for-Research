# Unix Command and Scripting Quick Reference Guide

## File Management
- **Copying Files**:
  - Use the `cp` command to copy files.
  - Syntax: `cp <source_file> <destination_file>`
  - Example: `cp file1.txt file2.txt`
  
- **Removing Files**:
  - Use the `rm` command to remove files.
  - Syntax: `rm <file_name>`
  - Example: `rm example.txt`
  
- **Moving Files**:
  - Use the `mv` command to move or rename files.
  - Syntax: `mv <source> <destination>`
  - Example: `mv file1.txt folder/`

## Directory Navigation
- **Display Current Directory**:
  - Use the `pwd` command to show the full path of your current working directory.
  - Example: `pwd`

- **List Contents of a Directory**:
  - Use the `ls` command to list files in the current directory.
  - Syntax: `ls` or `ls -l` for detailed output.
  - Example: `ls -l`

## Manual Pages and Help
- **View Manual Pages**:
  - Use the `man` command to get details about other commands.
  - Syntax: `man <command>`
  - Example: `man sort`
  
- **Exit Manual Pages**:
  - Press `q` to exit the manual page.

## Basic Bash Scripting
- **Assigning Command-Line Arguments**:
  - Assign the first command-line argument to a variable: `FIRST=$1`
  - Assign the second command-line argument to a variable: `SECOND=$2`

- **Printing Variables**:
  - Use the `echo` command to print the value of a variable.
  - Syntax: `echo $VARIABLE_NAME`
  - Example: `echo $FIRST`

- **Creating and Running a Script**:
  - Start the script with a shebang: `#!/bin/bash`
  - Save the file as `script.sh`.
  - Run the script: `bash script.sh <arguments>`

## Text Processing
- **Counting Characters in a FASTA File**:
  - Exclude header lines: `grep -v "^>" filename.fasta`
  - Remove newlines: `tr -d '\n'`
  - Count characters: `wc -c`
  - Full command:
    ```bash
    grep -v "^>" filename.fasta | tr -d '\n' | wc -c
    ```

## Common Errors and Debugging
- **Error: `No such file or directory`**:
  - Likely causes:
    - Running the script from the wrong directory.
    - Typo in the script or file name.
    - Missing executable permissions.

- **Error: `command not found`**:
  - Likely causes:
    - The command is not installed.
    - The command is not in the system `PATH`.
   
## Finding the Length (bp) of the Ebola Sequence
To find the length of the Ebola sequence from the NCBI database:
1. **Visit the NCBI Website**:
   - Go to [https://www.ncbi.nlm.nih.gov/](https://www.ncbi.nlm.nih.gov/).

2. **Search for Ebola**:
   - Use the search bar to find sequences related to "ebolavirus."
   - Locate the specific sequence of interest (e.g., project number PRJNA257197).

3. **Look for the Sequence Length**:
   - Once on the sequence page, look for details about the sequence length, usually displayed in base pairs (bp).

4. **Download and Count (Optional)**:
   - If you download the FASTA file, you can count the base pairs using Unix tools:
     ```bash
     grep -v "^>" ebola_sequence.fasta | tr -d '\n' | wc -c
     ```
