# Network Communications Final Project

## System Requirements
- **Operating System:** Windows
- **Machine Code:** Python

## Files
- **App_server.py:** Server-side application handling SQL queries.
- **Client.py:** Client-side application interacting with various server functionalities.
- **DHCP.py:** Client module for Dynamic Host Configuration Protocol.
- **DNS.py:** Client module for Domain Name System.
- **mydatabase.db:** Database file.

## How to Run the Program
1. **Ensure that `mydatabase.db` is in the same directory as the `.py` files.**
   
2. **Run the Server:**
    - Open a terminal.
    - Navigate to the directory containing the Python files.
    - Execute:
        ```
        cd files_directory
        python App_server.py
        ```
3. **Run the Client:**
    - Open a new terminal.
    - Navigate to the directory containing the Python files.
    - Execute:
        ```
        cd files_directory
        python Client.py
        ```

## Program Overview

### 1. Client – DHCP
- **Functionality:**
    - Utilizes DHCP to dynamically obtain an IP address from a DHCP server on the network.

### 2. Client – DNS
- **Functionality:**
    - Sends domain name queries to a DNS server and resolves them, either from cache or by forwarding to a Google DNS server.

### 3. Client – App Server (TCP)
- **Functionality:**
    - Sends SQL queries to the server via TCP connection and receives responses.

### 4. Client – App Server (RUDP)
- **Functionality:**
    - Establishes a Reliable UDP (RUDP) connection with the server to send SQL queries and receive results.

## Program Workflow

1. **Client – DHCP:**
    - Sends DHCP discover packet.
    - Captures DHCP offer packet.
    - Requests offered IP address and updates client.

2. **Client – DNS:**
    - Sends domain name query to DNS server.
    - Receives resolved IP address from server, either from cache or Google DNS.
    
3. **Client – App Server (TCP):**
    - Sends SQL queries to server.
    - Receives and prints responses from the server.

4. **Client – App Server (RUDP):**
    - Establishes RUDP connection with server.
    - Sends SQL queries using RUDP.
    - Receives and validates responses using RUDP.

## Conclusion
This program demonstrates various network communication functionalities including DHCP, DNS, and client-server interactions over both TCP and RUDP protocols. Each component handles specific tasks such as IP address allocation, domain name resolution, and SQL query execution with appropriate communication protocols ensuring reliability and efficiency.
