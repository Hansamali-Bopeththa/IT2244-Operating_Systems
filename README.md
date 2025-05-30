# IT2244-Operating_Systems

1. Basic Sleep and Exit
This program starts, prints a message, sleeps for 3 seconds, and then exits using exit(0).

Since there is no fork(), it runs as a single process.

![Q01](https://github.com/user-attachments/assets/c448132b-ce0f-4432-a566-7a334dc79f5e)


2. Parent-Child Process with Waiting
The parent creates a child process using fork().

The child sleeps for 2 seconds and then exits.

The parent waits for the child to finish (wait(&status)).

After the child exits, the parent prints the child's exit status using WEXITSTATUS(status).

![Q2](https://github.com/user-attachments/assets/a2f0acba-a223-4767-89c3-ada53197e2b4)


3. Parent Creating Two Children
The parent creates two child processes.

First child sleeps for 1 second, Second child sleeps for 3 seconds.

The parent waits for both children using waitpid().

Once both children exit, the parent prints that both have finished.

![Q3](https://github.com/user-attachments/assets/63931b59-63d7-4f38-8fd5-9758c9e634bd)


4. Tracking Which Child Finishes First
The first child sleeps 2 seconds, then exits with status 2.

The second child sleeps 1 second, then exits with status 1.

The parent waits twice, checking which child finishes first.

It prints PID and exit status of both children.

![Q4](https://github.com/user-attachments/assets/370d093a-81a1-4759-a056-5e74d01f103d)


5. Parent, Child, and Grandchild Process
The parent creates a child, and the child creates a grandchild.

Grandchild sleeps 2 seconds, exits with status 2.

Child waits for grandchild to finish, prints the exit status, and exits with status 55.

Parent waits for the child, prints the child's exit status, and exits.

![Q5](https://github.com/user-attachments/assets/7fa14afc-b5b9-4fab-9f64-27efeebf816b)

