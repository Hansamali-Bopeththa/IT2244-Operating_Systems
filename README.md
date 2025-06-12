# IT2244-Operating_Systems

Practical 01: Using Pipes for Communication


This practical demonstrates interprocess communication using pipes.


The first program writes three messages (msg1, msg2, msg3) to a pipe.


The parent process sends data through the pipe, and the child process reads and displays them.




Practical 02: Parent-Child Communication via Fork()


The parent process takes user input (name, registration number, and age).


It creates a child process using fork(), which then prints the received input.


The wait() function ensures the child process finishes before the parent completes.




Practical 03: Using Pipes for IPC (Interprocess Communication)


Instead of using shared memory, this program uses a pipe to transfer user input from the parent process to the child process.


The parent takes input (name, regno, age), sends it to the child, and the child reads and displays the information.




Practical 04: Shape Area Calculation Using Pipes


The parent process collects user input (shape selection and dimensions).


It sends the data to the child process, which performs area calculations based on shape type.


The result is then sent back to the parent process through another pipe, which prints the final output.


Each of these practicals showcases process communication techniques using pipes and fork() in C programming.
