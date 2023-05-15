# Comparison-between-Process-And-Threads-
INTRODUCTION:
We will show the comparison by implementing sorting algorithm i.e. Merge Sort .We will compare the performance of this sorting algorithm with respect to time, number of inputs and speed . The time taken at each step is recorded and displayed. At the end, the 4 sub arrays combine into one array and displayed. After executing, the program also shows the time complexity taken for a particular algorithm and IPC method.
PROGRAMMING PLATFORM USED:
•	The programming platform used is C Language
•	The operating system that we worked on is Ubuntu.
MODULES USED:
•	Bubble sort
•	Insertion sort
•	Merge sort
•	Quick sort
•	Heap sort
PROBLEM FACED:
When the processes break e.g., when the array breaks into 4 parts to be assigned to each core the process makes a copy of the array only, so when the processes end itself the copy of array is also deleted, although the array is sorted but it vanishes.
SOLUTION:
solve this problem, we used to inter process communication so that that the sorted array could be send to the master process so that the array is merged from there. Due to this problem, we Also used comments in the C++ program to use it for debugging.  
IMPLEMENTATION:-
POSIX THREADS:
The array was divided into 4 parts, and 4 threads were created alongside with each thread taking each part of the array. Threads sort each part of the array individually and finally combine them together to display the final sorted array.
PROCESSES:
It was implemented using 2 fork calls and then child and parent processes were executed through different if else conditions to make them work accordingly.
SHARED MEMORY:
We have to use shared memory for implementing Processes so that the sorting done on different sub arrays in different processes should reflect in parent process also.
