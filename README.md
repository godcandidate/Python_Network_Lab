# Python Network Lab

This repository contains a series of Python scripts that demonstrate basic networking concepts using different modules such as `socket`, `requests`, and `scapy`. The lab includes examples of client-server communication, HTTP requests, and network packet manipulation.

## Lab Components

1. `client.py` - A simple TCP client that connects to a server, sends a message, and receives a response.
   
2. `server.py` - A TCP server that listens for incoming client connections, receives data, and sends an echo response.
   
3. `request.py` - A script that makes a GET request to a REST API and processes the response.
   
4. `scap.py` - A script that sends an ICMP packet (ping) to a target and displays the response.
   
5. `requirements.txt` - A file containing the necessary Python libraries required for the lab.

---

## Prerequisites
To run the scripts, you'll need the following Python libraries:

- requests (for making HTTP requests)
  
- scapy (for network packet manipulation)

### Setup Environment

1. Clone this repository to your local machine:
    ```bash
    git clone https://github.com/godcandidate/Python_Network_Lab/
    ```

2. Navigate into the project directory:
    ```bash
    cd Python_Network_Lab
    ```

3. Create and activate a virtual environment (optional but recommended):
    ```bash
    python3 -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

4. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

---

## Usage

### 1. Running the Server

To start the server, run the `server.py` script. This will make the server listen for incoming connections on `localhost` and port `12345`.

```bash
    python server.py
```

2. Running the Client
   
In a separate terminal, run the client.py script. This will connect to the server, send a message, and display the server's response.

```bash
    python client.py
```

3. HTTP Request Example
   
The request.py script demonstrates how to make a GET request to an API. It fetches data from a sample API and prints the response if successful.

```bash
    python request.py
```

4. ICMP Ping Example
The scap.py script sends an ICMP ping to www.google.com and displays the response, allowing you to see basic packet manipulation.

``` bash
    python scap.py
```

## Conclusion
This lab demonstrates basic networking concepts including TCP communication, HTTP requests, and ICMP packet manipulation. You can extend these examples to build more complex networked applications.
