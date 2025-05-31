# IT2244-Operating_Systems


01.

The program begins by printing "Hello world".

Then, it calls fork(), which creates a new child process.

getpid() retrieves the process ID (PID) of the running process.

The program prints the process ID and the return value of fork(), which:

Is 0 in the child process.

Is the child's PID in the parent process.


![01](https://github.com/user-attachments/assets/079b4366-ed19-4b40-bc27-dbc7a30e6a49)


02.

The program calls fork(), which creates a child process.

It checks the return value of fork():

If f == 0, it means this is the child process.

Otherwise, it’s the parent process.


![02](https://github.com/user-attachments/assets/50845337-e643-4807-837d-7acaf8dc5294)


03.

 The program starts with Process A (parent) and prints its own PID and parent PID.

It then creates Process B using fork(). The child process prints its parent’s PID.

The parent process further creates Process C using another fork(), making three processes in total.

The output will show information about the relationships between the parent (A) and its two children (B and C).


![c](https://github.com/user-attachments/assets/a8281c77-9827-45dc-86e7-1697cb5054de)
