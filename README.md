In this project, we will simulate and analyse Banker’s algorithm to avoid deadlock. Deadlock is a condition in the operating system, where processes wait for an event that will never occur. If a deadlock occurs in a system, the system will hang and cannot be operated. The solution to this problem is to avoid deadlock by closing the possibility that might cause deadlock.Here we use the Banker’s algorithm to avoid deadlock. The algorithm will try to lend resources to the process and analyse whether the state after lending resources is a safe state or unsafe state. If the state is a safe state, then the resource is allocated. Applications can simulate the requesting of resources by processes and prevent deadlock in the simulation using Banker's algorithm, which is to ensure that every situation after lending resources is in a safe state. Deadlock will not occur in a safe state.

**INTRODUCTION-**  Banker’s Algorithm is a deadlock avoidance algorithm. It is also used for deadlock detection. This algorithm tells that if any system can go into a deadlock or not by analyzing the currently allocated resources and the resources required by it in the future.
The Bankers Algorithm consists of the following two algorithms </br>
    1. Request-Resource Algorithm  </br>
    2. Safety Algorithm </br>

**Resource- Request Algorithm -**
Whenever a process makes a request of the resources then this algorithm checks if the resource can be allocated or not.
It includes three steps:
   1. The algorithm checks that if the request made is valid or not. A request is valid if the number of requested resources of each resource type is less than the Need(which was declared previously by the process). If it is a valid request then step 2 is executed else aborted.
   2. Here, the algorithm checks that if the number of requested instances of each resource is less than the available resources. If not then the process has to wait until sufficient resources are available else go to step 3.
   3. Now, the algorithm assumes that the resources have been allocated and modifies the data structure accordingly.
After the allocation of resources, the new state formed may or may not be a safe state. So, the safety algorithm is applied to check whether the resulting state is a safe state or not. </br>

**Safe state:** A safe state is a state in which all the processes can be executed in some arbitrary order with the available resources such that no deadlock occurs.</br>
    1. If it is a safe state, then the requested resources are allocated to the process in actual.</br>
    2. If the resulting state is an unsafe state then it rollbacks to the previous state and the process is asked to wait longer.</br>
**Safety Algorithm**</br>
The safety algorithm is applied to check whether a state is in a safe state or not.
This algorithm involves the following four steps:</br>
    1. Suppose currently all the processes are to be executed. Define two data structures as Work and Finish as vectors of length m(where m is the length of Available vector)and n(is the number of processes to be executed).</br>
    2. This algorithm will look for a process that has Need value less than or equal to the Work. So, in this step, we will find an index i such that If no such ‘i’ is present then go to step 4 else to step 3.</br>
    3. The process 'i' selected in the above step runs and finishes its execution. Also, the resources allocated to it gets free. The resources which get free are added to the Work and Finish(i) of the process is set as true. The following operations are performedAfter performing the 3rd step go to step 2.</br>
    4. If all the processes are executed in some sequence then it is said to be a safe state. Or, we can say that ifFinish[i]==true for all i,
then the system is said to be in a safe state</br>


**TOOLS & DATA SOURCES -**</br>
    IDE (Integrated Development Environment) - Visual Studio Code is a free source-code editor made by Microsoft for Windows, Linux and macOS. Features include support for debugging, syntax highlighting, intelligent code completion, snippets, code refactoring, and embedded Git. Users can change the theme, keyboard shortcuts, preferences, and install extensions that add additional functionality </br>
    Programming Language - HTML ,CSS ,JavaScript </br>
     Data Source - Wikipedia , W3school </br>
     Platform – Firefox </br>
contributors - 
- Shivam Sharma - 185004
- Vikrant Bhardwaj - 185007
- Hritwik Bhardwaj - 185009
