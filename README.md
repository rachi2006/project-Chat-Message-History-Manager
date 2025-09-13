# project-Chat-Message-History-Manager
🔹 Overview

* This C++ program is a Chat Message History Manager.
It simulates a mini chat system where you can:

* Send messages.

* Receive messages (copies last sent message into inbox).

* View inbox or sent history.

* Undo and redo sent messages.

It uses queues for the inbox (FIFO order) and stacks for sent/undone messages (LIFO order).
Timestamps are automatically added to every message using <chrono> and <ctime>.
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
🔹 Features

* Send Message

* Stores the message in sentMessages stack.

* Shows timestamp when sent.

* Receive Message

* Simulates receiving the last sent message by moving it to inbox.

* Show Inbox

* Displays all received messages in order (FIFO).

* Show Sent Messages

* Displays all sent messages in reverse order (latest first).

* Undo Last Sent Message

* Removes the last sent message and moves it to an undo stack.

* Redo Last Undone Message

* Restores the last undone message back into the sent list.

* Timestamps

* Every message is saved with the exact date & time it was created.

* Menu System

* Simple text-based menu with emojis for clarity.
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
🔹 How to Run

* Save the code as chat_manager.cpp.

* Open a terminal/command prompt.

* Compile the program:

* g++ chat_manager.cpp -o chat_manager
               or
  * you can also run in online compiler.

Run the program:

./chat_manager

🔹 Example Output

User Interaction (Sample Run):

======== 💬 Chat Message History Manager ========
1️⃣  Send Message.
2️⃣  Receive Message.
3️⃣  Show Inbox.
4️⃣  Show Sent Messages.
5️⃣  Undo Last Sent.
6️⃣  Redo Last Undone.
7️⃣  Exit.
👉 Enter choice: 1
✍️ Enter message to send: Hello World!
📤 Message sent: "Hello World!" at Sat Sep 13 17:20:45 2025

👉 Enter choice: 4
--- 📤 Sent Messages ---
🕒 Sat Sep 13 17:20:45 2025 | ✉️ Hello World!

👉 Enter choice: 2
📥 Message received: "Hello World!" at Sat Sep 13 17:20:50 2025

👉 Enter choice: 3
-------- 📥 Inbox Messages --------
🕒 Sat Sep 13 17:20:50 2025 | 💬 Hello World!

👉 Enter choice: 5
↩️ Undo: "Hello World!" removed from sent messages.

👉 Enter choice: 6
🔁 Redo: "Hello World!" re-sent.

👉 Enter choice: 7
👋 Exiting...
