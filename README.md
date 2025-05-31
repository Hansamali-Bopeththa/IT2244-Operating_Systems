# IT2244-Operating_Systems


:- The program starts with Process A (parent).

:- It prints its own process ID (getpid()) and its parent process ID (getppid()).

:- fork() is called the first time (f1 = fork()), creating Process B.

:- If f1 == 0, the child process (B) runs and prints its details.

:- The parent (A) continues execution.

:- fork() is called the second time (f2 = fork()), creating Process C.

:- If f2 == 0, the child process (C) runs and prints its details.

:- The result is three active processes: A (Parent), B (Child of A), and C (Child of A).

:- Each process has a unique process ID (PID), while its parent’s ID is retrieved using getppid().




![1](https://github.com/user-attachments/assets/cbea6bf6-6e44-4e44-9af8-ed61825886ed)
