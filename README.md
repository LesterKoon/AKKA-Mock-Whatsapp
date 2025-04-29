# Mock WhatsApp Application Using Akka Actors

## Overview

This is a mock WhatsApp application built using Akka actors to simulate a distributed messaging system. The application includes various features such as:

- **Private Messaging**
- **Group Chats**
- **Community Conversations**
- **User Status Updates**

The system is organized into actors that handle core business logic, including message routing, private and group messaging, community chat management, user status updates, and session management.

## Components

The application is structured with the following key actors:

- **ServerActor**: Responsible for message routing across the system.
- **ChatManagerActor**: Manages direct/private messaging between users.
- **GroupChatManagerActor**: Handles group communication and management.
- **CommunityChatManagerActor**: Manages public community chat conversations.
- **StatusUpdateManagerActor**: Manages user status updates.
- **UserActor**: Manages user sessions, including login and authentication.


## Getting Started

### Prerequisites

- Java 11 or higher
- Maven 3.x

### Setup Instructions

1. **Clone the Repository**
   ```bash
   git clone https://github.com/LesterKoon/mock-whatsapp.git
   cd mock-whatsapp
   ```

2. **Build the Project**
   ```bash
   mvn clean install
   ```

3. **Start the Server**
   ```bash
   mvn exec:java -Dexec.mainClass="chat.main.ServerMain"
   ```

4. **Start Client(s)**
   For each user, open a new terminal window and run:
   ```bash
   mvn exec:java -Dexec.mainClass="chat.main.UserMain"
   ```

Each client represents a different user session.

