This assignment demonstrates two approaches for merging multiple already sorted lists:

K-Way Merge using a Min Heap
Pairwise Merging

The program is implemented in C and compares both approaches based on heap size, number of comparisons, time complexity, and space requirements.

📋 Problem Statement

A financial system receives three already sorted transaction lists:

L1 = 10, 30, 50, 70
L2 = 20, 40, 60, 80
L3 = 15, 35, 55, 75

The tasks are:

Represent the sorted lists using suitable data structures.
Implement K-way merge using a Min Heap.
Display important heap states during execution.
Implement pairwise merging.
Count the major operations/comparisons.
Compare both approaches.
Determine which approach is more suitable when the number of sorted files increases.
🎯 Objectives
Understand K-way merging.
Learn how a Min Heap can be used for efficient merging.
Implement merging of sorted arrays in C.
Compare Min Heap and pairwise merging approaches.
Analyze time and space complexity.
Understand the scalability of both methods.
🛠️ Technologies Used
Programming Language: C
Data Structure: Min Heap
Compiler: GCC / Code::Blocks / Dev-C++ / Visual Studio Code
Operating System: Windows / Linux / macOS
📂 Input Data

The program uses three sorted lists:

L1 = 10 30 50 70
L2 = 20 40 60 80
L3 = 15 35 55 75
🔹 Approach 1: K-Way Merge Using Min Heap

The first element from each sorted list is inserted into a Min Heap.

Initial elements:

10 20 15

The smallest element is repeatedly removed from the heap.

After removing an element, the next element from the same list is inserted into the heap.

Example:

Initial Heap
10 20 15

Remove 10
Insert 30

Heap
15 20 30

This process continues until all elements are merged.

Final Output
10 15 20 30 35 40 50 55 60 70 75 80
🔹 Approach 2: Pairwise Merging

In pairwise merging, two lists are merged at a time.

Step 1

Merge L1 and L2:

10 30 50 70
20 40 60 80

Result:

10 20 30 40 50 60 70 80
Step 2

Merge the result with L3:

10 20 30 40 50 60 70 80
15 35 55 75

Final result:

10 15 20 30 35 40 50 55 60 70 75 80
📊 Complexity Comparison
Feature	K-Way Min Heap	Pairwise Merge
Time Complexity	O(N log K)	O(NK)
Space Complexity	O(K + N)	O(N)
Heap	Required	Not required
Heap Size	K	No heap
Scalability	Better for many lists	Less efficient for many lists
Implementation	Slightly more complex	Simple

Where:

N = total number of elements
K = number of sorted lists

For this assignment:

N = 12
K = 3
📁 Project Structure
K-Way-Merge/
│
├── k_way_merge.c
└── README.md
▶️ How to Run
Using GCC

Compile the program:

gcc k_way_merge.c -o k_way_merge

Run:

./k_way_merge
On Windows
gcc k_way_merge.c -o k_way_merge.exe
k_way_merge.exe
💻 Sample Output
====================================
        K-WAY MERGE PROGRAM
====================================

Input Lists:

L1: 10 30 50 70
L2: 20 40 60 80
L3: 15 35 55 75

====================================
      K-WAY MERGE USING MIN HEAP
====================================

Initial heap:
10 20 15

Selected minimum = 10
Heap after operation:
15 20 30

...

Final K-way merged list:
10 15 20 30 35 40 50 55 60 70 75 80

====================================
       PAIRWISE MERGING
====================================

After merging L1 and L2:
10 20 30 40 50 60 70 80

After merging with L3:
10 15 20 30 35 40 50 55 60 70 75 80
📚 Concepts Demonstrated
Arrays
Structures in C
Min Heap
Heapify
K-way merge
Pairwise merge
Sorting and merging
Time complexity
Space complexity
Algorithm comparison
