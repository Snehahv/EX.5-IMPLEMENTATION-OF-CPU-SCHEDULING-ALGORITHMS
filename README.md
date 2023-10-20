# EX.5-IMPLEMENTATION-OF-CPU-SCHEDULING-ALGORITHMS

## AIM:
To implement First-Come-First-Serve (FCFS) Scheduling

## ALGORITHM:
1.Start with a queue (or a list) to represent the ready queue of processes.
2.Initialize a timer or clock to 0.
3.Read the number of processes (n) and create a data structure to store process information,
including arrival time (AT) and burst time (BT) for each process.
4.Read the arrival time and burst time for each process and store them in the data structure.
5.Sort the processes in the ready queue based on their arrival times in ascending order. This step
ensures that processes are executed in the order they arrive.
6.Initialize the waiting time (WT) and turnaround time (TAT) for the first process to 0.
7.For each process in the ready queue (in the order of arrival): a. Calculate the start time (ST) as the
maximum of the current time and the arrival time of the process. b. Calculate the finish time (FT) as
the start time plus the burst time of the process. c. Calculate the waiting time (WT) for the process
as the start time minus the arrival time. d. Calculate the turnaround time (TAT) for the process as
the finish time minus the arrival time. e. Update the current time to the finish time.
8.Calculate the average waiting time (AWT) and average turnaround time (ATAT) for all processes by
summing up the individual waiting times and turnaround times and dividing by the total number of
processes.
9.Display the waiting time, turnaround time, and other relevant information for each process.
10.Display the average waiting time and average turnaround time for all processes.
11.End
## PROGRAM:
```
PROGRAM:
#include<stdio.h>
int main()
{
int c=0,i,n,bt[10],at[10],wt[10],ft[10];
int st[10],tat[10];
float awt=0,atat=0,rr[10];
printf("Enter the number of process : ");
scanf("%d",&n);
for(i=1;i<=n;i++)
{
printf("Enter the arrival time and burst time for the process %d",i);
scanf("%d %d",&at[i],&bt[i]);
}
for(i=1;i<=n;i++)
{
st[i]=c;
c=c+bt[i];
wt[i]=st[i]-at[i];
ft[i]=st[i]+bt[i];
tat[i]=wt[i]+bt[i];
rr[i]=tat[i]/bt[i];
}
for(i=1;i<=n;i++)
{
awt=awt+wt[i];
atat=atat+tat[i];
}
awt=awt/n;
atat=atat/n;
printf("\n\t\t CPU SCHEDULING\n\t\t ***************");
printf("\n\t\t FIRST COME FIRST SERVE\n\t\t **********************");
printf("\n--------------------------------------------------------------\n");
printf("proc\t at\t bt\t st\t ft\t wt\t tat\t rr\t\n");
printf("--------------------------------------------------------------");
for(i=1;i<=n;i++)
{
printf("\n %d\t %d\t %d\t %d\t %d\t %d\t %d\t%5.2f",i,at[i],bt[i],st[i],ft[i],wt[i],tat[i],r
}
printf("\n--------------------------------------------------------------");
printf("\n Average waiting time is %5.2f\n average tat is%5.2f",awt,atat); }
```

OUTPUT:


RESULT: First-Come-First-Serve Scheduling is implemented successfully.


AIM: To implement Shortest Job First (SJF) Preemptive Scheduling

ALGORITHM:


PROGRAM:


OUTPUT:


RESULT: Shortest Job First (SJF) preemptive scheduling is implemented successfully.


AIM: To implement Shortest Job First (SJF) Non-Preemptive Scheduling

ALGORITHM:


PROGRAM:


OUTPUT:


RESULT: Shortest Job First (SJF) Non-preemptive scheduling is implemented successfully.

AIM: To implement Round Robin (RR) Scheduling

ALGORITHM:


PROGRAM:


OUTPUT:


RESULT: Round Robin (RR) Scheduling is implemented successfully.


AIM: To implement Priority Preemptive Scheduling

ALGORITHM:


PROGRAM:


OUTPUT:


RESULT: Priority Preemptive scheduling is implemented successfully.


AIM: To implement Priority Non-Preemptive Scheduling

ALGORITHM:


PROGRAM:


OUTPUT:


RESULT: Priority Non-preemptive scheduling is implemented successfully.

