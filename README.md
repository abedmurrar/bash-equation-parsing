# Birzeit University

# Department of Electrical & Computer Engineering

# ENCS313, Linux Laboratory

# Project#1: Shell Scripting - Validation and Solving Simple File Extractions

**Objective:** In this project, you will write a shell script to solve simple text parsing problem. The script
must pass into three stages as following:

### 1. Read instruction file:

The first line in the file contains the number of files to read. Then each line contains only
one file name.
**Example:**

```
4
Filea
Fileb
Filec
Filed
```

### 2. File parsing and computation:

1. In the second stage, the script should check if the input contains only valid file
    name (It has text and numbers but not special characters).
2. Open the file and do mathematical computation in each file. Each file can have
    one or more than one computation like

**Filea:**

```
 -4*5

(((2+4)*5)-3)

-3*4+(2+5)
```

**Fileb:**
```
4*5/3

(2+9)/5)-12)

-3*2+(14+5)
```

3. Valid equations contain **only** these characters: “ **(** “, ” **)** ”, “ **+ - / *** ” and “ **0 1 2 3 4 5 6 7 8 9** ”
    And save the computed results in new file name like oldfilename_computed. If
    there is an error in one file that can't compute, then it will print our error message
    indicating that this file has error and move on to next file:
**Filea_computed:**
```
-20
27
-5
```

### 4. **Final computation is to create** CSV file with the following fields:

|File name| Column1 | Column2 | Column3|
|----------|--------------|-----------|-----------|
|Filea| 20 | 27 | -2 |
|Fileb|...|||

Avg

Max

Min

Files with error

Files: failed to compute (in red)

Number of passed computation file: passed – files with errors.


### 5. Extra credit

a. for those who do the coloring in step 4. Like showing everything above average in green and below it in red.

b. Do - log to generate log file to show detail errors in each file

