# IT2244-Operating_Systems

Message Queue

Key Concepts
Message Queue: A mechanism that allows processes to communicate by sending and receiving messages.

msgget(): Creates (or accesses) a message queue.

msgsnd(): Sends a message to the queue.

msgrcv(): Retrieves a message from the queue.

msgctl(): Deletes the message queue when it's no longer needed.

1: Sender
Generate a unique key using ftok(). This key identifies the message queue.

Create (or access) a message queue using msgget(). If it doesn’t exist, it will be created.

Prompt the user to input a message (fgets()).

Send the message using msgsnd().

Display the message that was sent.

![Q01](https://github.com/user-attachments/assets/98383afc-5d85-4adf-a8ba-6f939f78618f)


2: Receiver
Generate the same unique key (ftok()), so it refers to the same message queue.

Access the existing message queue (msgget()).

Retrieve the message using msgrcv(), filtering by message type (mesg_type).

Print the received message.

Destroy the message queue using msgctl() to free system resources.

![Q02](https://github.com/user-attachments/assets/d6bd0de6-0c8a-401d-990b-998457f04ef9)
