* This assignment done by 4 people and have 2 parts, scheduling and memory, my role in this assigment is implement a scheduling part.
* Scheduling is implement by combination of Muitilevel-queue and round-robin algorithm.

![image](https://github.com/MinhDuy27/OS-Simulation/assets/146503855/b352be5a-c04a-4f8b-bf82-bf1bc0f54620)
  
* I implement by create many queue with priority of each queue from hight to low, each process is knew before with 3 things (time coming, priority, burst time), so with each priority of process, it will be assigned in queue that have priority value same as it's
* Each time CPU Work. it will retreive from hight to low to take 1 process out to processing, if have many CPU, it will take many process to processing
* The processing algorithm is round robin with time-sliced is knew before, so after the process processing this time-slice, it will enqueue back to the queue have same priority value.
* Each queue have fixed amount of times for CPU to take process out for processing (Limit_SLot), if this queue reach the limit, CPU will move to next queue with lower priority value and dequeue process out to processing.
* When all queues are reach the limit, they will all set back to default by 0 (Limit_Slot = 0), then the process keep going in above way.
* THe way that set limit for each queue make sure that all process will be processed, so we will not be in the starving-stituation ( have process that always have to wait in queue and never be processed by CPU)
