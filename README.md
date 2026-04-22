# Problem 127 - 卡牌大师

**ACMOJ Problem ID**: 2514

## Table of Contents

- [Problem 127 - 卡牌大师](#problem-127-卡牌大师)
  - [Table of Contents](#table-of-contents)
  - [Introduction](#introduction)
    - [Background](#background)
  - [Assignment Description](#assignment-description)
    - [Grade Composition](#grade-composition)
  - [Assignment Requirements](#assignment-requirements)
    - [Input Format](#input-format)
    - [Output Format](#output-format)
    - [Samples](#samples)
    - [Data Constraints](#data-constraints)
  - [Per-Testcase Resource Limits](#per-testcase-resource-limits)
  - [Test Data](#test-data)
  - [Submission Requirements](#submission-requirements)
    - [OJ Git Repository Compilation Process](#oj-git-repository-compilation-process)
    - [Git Configuration Requirements](#git-configuration-requirements)
    - [Submission Guidelines](#submission-guidelines)
    - [Evaluation Notes](#evaluation-notes)
    - [Academic Integrity](#academic-integrity)

## Introduction

### Background

This problem tests algorithmic problem-solving skills.

## Assignment Description

### Grade Composition

| Grading Component | Percentage |
| :--: | :--: |
| Pass **2514. 卡牌大师** | 80% |
| Code Review | 20% |

Here are several points that need clarification:

- In the Code Review, we will **strictly examine your code style and repository organization structure, etc.**

- This assignment provides some sample data for testing, stored in the `/workspace/data/127/data_test/` directory. Note that these are not the test cases on the Online Judge. Passing all local test cases does not guarantee that you will pass the OJ tests.

- Besides the provided sample data, we also encourage you to design your own test data based on your program logic to assist debugging.

## Assignment Requirements

### Problem Description

卡牌大师有$n$张卡牌，这些卡牌对应的价值分别为$a_1,a_2,\cdots,a_n$。卡牌大师可以选择第$i$张卡牌点燃，点燃后获得的价值为$a_{i-1}\times a_i \times a_{i+1}$(如果只剩一张卡牌，那么点燃后获得的就是它的价值。如果这是第一张牌，那么点燃后获得的就是它和下一张卡牌的价值的乘积，如果是最后一张，那么点燃后获得的就是它和上一张卡牌的价值的乘积)，点燃后卡牌会消失，使得它左边的卡牌和右边的卡牌相邻。卡牌大师总有方法获得最大总价值。他想问你最大总价值是多少。

**TIPS:** 卡牌大师觉得这题有点难了，他决定告诉你他的窍门。他是用区间dp写这题的。

### Input Format

第一行一个正整数$n$，为卡牌数量。

第二行$n$个正整数$a_i$，中间用空格隔开，表示第$i$张卡牌的价值。

### Output Format

一个整数，表示最大值。

### Samples

#### Sample 1

**Input:**
```
5
3 5 6 2 5
```

**Output:**
```
305
```

### Data Constraints

$1\le a_i \le 10^4$

对于20%数据，$1\le n \le 10$

对于40%数据，$1\le n \le 100$

对于100%数据，$1\le n \le 1000$

## Resource Limits

- **Time Limit**: 1000 ms
- **Memory Limit**: 244 MiB

## Per-Testcase Resource Limits

- **Time Limit (per test case)**: 1000 ms
- **Memory Limit (per test case)**: 244 MiB
- **Disk Usage**: No disk usage is permitted.

## Test Data

The test data for this problem is located at `/workspace/data/127/data_test/`.

## Submission Requirements

### OJ Git Repository Compilation Process

For Git compilation, we will first clone the repository using a command similar to:
```bash
git clone <repo_url> . --depth 1 --recurse-submodules --shallow-submodules --no-local
```

Then we check if there is a `CMakeLists.txt` file. If it exists, we run (if not, a warning message will be displayed):
```bash
cmake .
```

Finally, we check if there is any of `GNUmakefile`/`makefile`/`Makefile` (if cmake was run previously, this will be the generated Makefile). If it exists, we run (if not, a warning message will be displayed):
```bash
make
```

After this process is complete, we will use the `code` file in the project root directory as the compilation result.

A `CMakeLists.txt` file is provided in the project. You can use or modify it as needed. The local environment has gcc-13 and g++-13 available.

### Git Configuration Requirements

**IMPORTANT**: You must create a `.gitignore` file in your project root directory to avoid OJ evaluation conflicts.

The `.gitignore` file should include at least the following entries:

```gitignore
CMakeFiles/
CMakeCache.txt
```

### Submission Guidelines

- The submitted code must be able to compile successfully through the above compilation process
- The compiled executable file name must be `code`
- The program needs to be able to read data from standard input and write results to standard output
- Please ensure the code runs correctly within the given time and space limits
- **You must use C++ or C language** to implement this assignment

### Evaluation Notes

- The evaluation system will test your program using the provided test data
- The program output must exactly match the expected output (including format)
- Exceeding time or memory limits will be judged as the corresponding error type
- Please pay attention to the overall time performance of your code and the time complexity of each part of your algorithm.

### Academic Integrity

If any violations are found during evaluation or code review (including but not limited to using unconventional methods to pass test cases), your final score may be significantly reduced or become **0 points**.
