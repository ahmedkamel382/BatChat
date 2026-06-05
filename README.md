# BatChat 🦇

BatChat is a comprehensive, Java-based desktop messaging application designed for seamless communication. Built with a rich graphical user interface using JavaFX, the application allows users to create accounts, engage in private one-on-one conversations, manage multi-user group chats, and share multimedia attachments. All system data—including user credentials, chat histories, and file metadata—is persistently and securely managed through a MySQL relational database.

## ✨ Features

* **Secure User Authentication:** Comprehensive registration and login system with duplicate-user validation and credential verification.
* **Private Messaging (1-on-1):** Start dedicated, persistent text chains with any registered user. Chat histories are dynamically loaded upon opening a conversation.
* **Dynamic Group Chats:** Create custom chat rooms and seamlessly add multiple registered users. Group messages are routed to all participants tied to the room.
* **Multimedia Integration:** Native support for sending and receiving image attachments (`.png`, `.jpg`, `.jpeg`, `.gif`). Images are rendered directly within the chat UI alongside text messages.
* **Robust Data Persistence:** Completely database-driven architecture using MySQL to reliably store user profiles, message timestamps, relationship mappings, and attachment metadata.

## 🛠️ Technology Stack

* **Frontend GUI:** [JavaFX](https://openjfx.io/) – Manages the responsive desktop interface, layout rendering, and interactive UI components.
* **Backend Logic:** Java (JDK 8+) – Implements Object-Oriented principles to manage application state, I/O file operations, and stream processing.
* **Database:** MySQL – Relational database handling complex queries and data relationships.
* **Database Connectivity:** JDBC (`mysql-connector-j`) – Bridges the Java application to the MySQL server for real-time data transactions.

## 🗄️ Database Architecture Highlights
The application relies on a normalized relational database schema to maintain data integrity, including:
* `User`: Stores system credentials and profile information.
* `Message`: Logs message content, sender IDs, and precise timestamps.
* `PrivateChat` / `GroupChat`: Maps relationship data for 1-on-1 and multi-user environments.
* `Attachment`: Tracks metadata (file path, size, type) for uploaded local files.

## 🚀 Getting Started

### Prerequisites
* Java Development Kit (JDK 8 or higher)
* JavaFX SDK (if not bundled with your JDK)
* MySQL Server installed and running locally

### Installation & Setup

1.  **Clone the Repository:**
    ```bash
    git clone [https://github.com/yourusername/batchat.git](https://github.com/yourusername/batchat.git)
    cd batchat
    ```

2.  **Database Configuration:**
    * Create a new MySQL database named `batchat`.
    * Ensure your local MySQL server is running on `localhost:3306`.
    * *(Optional)* If your local MySQL credentials differ from the default, update the `URL`, `USER`, and `PASSWORD` constants inside `src/DatabaseManager.java`.

3.  **Compile and Run:**
    * Open the project in your preferred IDE (e.g., IntelliJ IDEA, Eclipse).
    * Ensure the `mysql-connector-j` dependency is added to your project structure/build path.
    * Build the project and run the `App.java` main class to launch the BatChat client.

## 💻 Usage
1.  **Create an Account:** Launch the app and register a new profile with a unique username.
2.  **Start Chatting:** Navigate the dashboard to initiate a "New Chat" with an existing user or create a "Group Chat" room.
3.  **Share Media:** Use the 📎 (attachment) button inside any chat room to upload and send images directly to your contacts.