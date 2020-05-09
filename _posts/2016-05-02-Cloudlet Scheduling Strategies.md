Cloudsim employs namely two strategies which are used to schedule the cloudlets. 
One of them is time-shared scheduler and second one is space-shared scheduler.

Time-shared scheduler: All available resources are shared between cloudlets for 
stipulated amount of time only. It uses round- robin scheduling algorithm. 
All space is allocated to one particular thread which is scheduled at that time. 
As the time frame for that cloudlet is over, all space resources 
are allocated to one cloudlet.

Space-shared scheduler: All available space is divided among the cloudlets. 
One cloudlet is running at one time but space is equally distributed among the 
various cloudlets.

We will use both of them:

1. Time-shared Scheduling:
    Change the code as written below (rest code is same from previous post). 
    Change the constructor of each virtual machine as the shown below.
```
    Vm vm1 = new Vm(vmid, brokerId, mips, pesNumber, ram, bw, size, vmm, new           
    CloudletSchedulerTimeShared());
```
   Then output will be:
   ![Output 1](/images/Cloudlet-Scheduling-1.png)


2. Space- shared scheduling:
    Change the constructor of each virtual machine as the shown below 
    for space shared scheduling algorithm.
```
    Vm vm1 = new Vm(vmid, brokerId, mips, pesNumber, ram, bw, size, vmm, new 
    CloudletSchedulerSpaceShared());
```

Then output will be:
![Output 2](/images/Cloudlet-Scheduling-2.png)

Comparison of the output:

Starting time and finish time of all the cloudlets is same in the case of time-shared scheduling as all cloudlets are given a impression that all are running at one point but time is divided among each providing resources are used by only one at one time. 

Whereas the starting and finish time of all 4 cloudlets is not same. Resources are divided among the cloudlets i.e. space, but not time. They are starting and finishing execution at different times.

Hope you like it!
