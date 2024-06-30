# First Come First Serve
##Description:
This C++ code implements the First-Come, First-Served (FCFS) scheduling algorithm. FCFS is a non-preemptive scheduling algorithm where the process that arrives first gets executed first. This code calculates and prints the waiting time, turnaround time, and average waiting and turnaround times for a set of processes.

Code Breakdown:
1.Include Statements and Namespace:

#include <iostream>: Includes the input-output stream library.
using namespace std;: Allows the use of standard library names without the std:: prefix.

2.Function Definitions:

findWaitingTime:

Parameters: int processes[], int n, int bt[], int wt[].
Purpose: Calculates the waiting time for each process.
Explanation:
The waiting time for the first process is set to 0.
For each subsequent process, the waiting time is calculated as the sum of the burst time of the previous process and the waiting time of the previous process.
findTurnAroundTime:

Parameters: int processes[], int n, int bt[], int wt[], int tat[].
Purpose: Calculates the turnaround time for each process.
Explanation:
The turnaround time for each process is the sum of its burst time and waiting time.
findavgTime:

Parameters: int processes[], int n, int bt[].
Purpose: Calculates and prints the average waiting time and turnaround time for the processes.
Explanation:
Calls findWaitingTime to calculate waiting times.
Calls findTurnAroundTime to calculate turnaround times.
Prints process details (Process ID, Burst Time, Waiting Time, Turnaround Time).
Calculates and prints the average waiting time and turnaround time.
3.Main Function:

Gets the number of processes from the user.
Initializes arrays for process IDs and burst times.
Prompts the user to input the process IDs and burst times.
Calls findavgTime to calculate and display the results.

Example Input and Output:

Enter the number of processes: 3
Enter the process ID for process 1: 1
Enter the process ID for process 2: 2
Enter the process ID for process 3: 3
Enter the burst time for process 1: 5
Enter the burst time for process 2: 9
Enter the burst time for process 3: 6
Processes  Burst time  Waiting time  Turn around time
 1         5          0             5
 2         9          5             14
 3         6          14            20
Average waiting time = 6.33333
Average turn around time = 13
