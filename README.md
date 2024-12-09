
---

# Python Network Lab

This repository contains a series of Python scripts that demonstrate basic networking concepts using different modules such as `socket`, `requests`, and `scapy`. The lab includes examples of client-server communication, HTTP requests, and network packet manipulation, providing hands-on experience with these important networking tools in Python.

## Lab Components

1. **`client.py`**  
   A simple TCP client that connects to a server, sends a message, and receives a response.  
   - **Usage**: Connects to the TCP server (on localhost:12345), sends a message, and waits for an echo response.  
   - **Screenshot Suggestion**: Insert a screenshot showing the client code, highlighting the `socket` creation and the message exchange.

2. **`server.py`**  
   A TCP server that listens for incoming client connections, receives data, and sends an echo response.  
   - **Usage**: Listens on `localhost` at port `12345`. Accepts incoming client connections and echoes the received data back to the client.  
   - **Screenshot Suggestion**: Include a screenshot of the server code, especially the `socket.bind()` and `socket.listen()` methods.

3. **`request.py`**  
   A script that demonstrates making a GET request to a REST API and processes the response.  
   - **Usage**: Fetches data from a sample API, processes the response, and prints out the content.  
   - **Screenshot Suggestion**: Add a screenshot of the code performing the GET request using the `requests` library.

4. **`scap.py`**  
   A script that sends an ICMP packet (ping) to a target and displays the response, demonstrating network packet manipulation with `scapy`.  
   - **Usage**: Sends a ping (ICMP request) to `www.google.com` and prints the response time.  
   - **Screenshot Suggestion**: Show the code that constructs and sends the ICMP packet using `scapy`.

5. **`requirements.txt`**  
   A file containing the necessary Python libraries required to run the lab scripts. This includes `requests`, `scapy`, and others.  
   - **Screenshot Suggestion**: No screenshot necessary here, but you can highlight any important libraries in a section below.

---

## Prerequisites

To run the scripts, you'll need the following Python libraries:

- `requests` - For making HTTP requests.
- `scapy` - For network packet manipulation (ICMP, etc.).
  
Ensure that you have these libraries installed before running the scripts. The next section covers how to set up your environment.

---

## Setup Environment

1. **Clone this repository to your local machine**:
    ```bash
    git clone https://github.com/godcandidate/Python_Network_Lab/
    ```

2. **Navigate into the project directory**:
    ```bash
    cd Python_Network_Lab
    ```

3. **Create and activate a virtual environment** (optional but recommended):
    ```bash
    python3 -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

4. **Install the required dependencies**:
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

- **Screenshot Suggestion**: Add a screenshot of the server running in the terminal, showing messages such as "Server listening on localhost:12345".

### 2. Running the Client

In a separate terminal window, run the `client.py` script. This will connect to the server, send a message, and display the server's response.

```bash
python client.py
```

- **Screenshot Suggestion**: Insert a screenshot of the client code in action, showing the message exchange with the server.

### 3. HTTP Request Example

The `request.py` script demonstrates how to make a GET request to an API. It fetches data from a sample API and prints the response if successful.

```bash
python request.py
```

- **Screenshot Suggestion**: Include a screenshot of the output, displaying the fetched data from the API.

### 4. ICMP Ping Example

The `scap.py` script sends an ICMP ping to `www.google.com` and displays the response, allowing you to see basic packet manipulation.

```bash
python scap.py
```

- **Screenshot Suggestion**: Show a screenshot of the terminal output displaying the ICMP response time.

---

## Example Outputs

1. **Client-Server Communication Example**:  
   After running the `client.py` and `server.py` scripts, you should see the following output in the terminal:

   **Server Output**:
   ```bash
   Server listening on localhost:12345
   Connection received from ('127.0.0.1', 54321)
   Data received: Hello, Server!
   ```

   **Client Output**:
   ```bash
   Connected to the server.
   Received from server: Hello, Server!
   ```

2. **HTTP Request Example**:  
   When running `request.py`, you should see output similar to this:

   ```bash
   Fetching data from the API...
   Response: { "data": "Hello from the API!" }
   ```

3. **ICMP Ping Example**:  
   Running `scap.py` will display a response from the target, similar to:

   ```bash
   Sending ICMP ping to www.google.com...
   Response time: 32 ms
   ```

---

## Troubleshooting

- **Error: Missing Python Libraries**:  
   Ensure that you've installed the required libraries by running `pip install -r requirements.txt`.
   
- **Error: Permission Denied (on ICMP ping)**:  
   On some systems, sending ICMP packets might require elevated privileges. Try running the script as an administrator or using `sudo` on Unix-based systems.

---

## Contributions

Feel free to fork this repository and contribute to improving the scripts! If you find any bugs or would like to add new features, please create a pull request.

---

This README provides a comprehensive guide to setting up and using the Python Network Lab, along with suggestions for adding relevant screenshots of your code and outputs. If you'd like, I can help you create specific screenshots or refine any section further.
