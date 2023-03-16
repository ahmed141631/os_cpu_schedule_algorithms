# os_cpu_schedule_algorithms



# for round robin algorithms
Create an array rem_bt[] to keep track of remaining burst time of processes. This array is initially a copy of bt[] (burst times array)
Create another array wt[] to store waiting times of processes. Initialize this array as 0.
Initialize time : t = 0
Keep traversing all the processes while they are not done. Do following for i’th process if it is not done yet.
If rem_bt[i] > quantum
t = t + quantum
rem_bt[i] -= quantum;
Else // Last cycle for this process
t = t + rem_bt[i];
wt[i] = t – bt[i]
rem_bt[i] = 0; // This process is over



# for shortest job first


Sort all the processes according to the arrival time. 
Then select that process that has minimum arrival time and minimum Burst time. 
After completion of the process make a pool of processes that arrives afterward till the completion of the previous process and select that process among the pool which is having minimum Burst time. 
