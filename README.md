# Distributed File System in Go
A lightweight, peer-to-peer distributed file system implemented in Go. This project demonstrates the core principles of distributed storage, including file replication, peer discovery, and secure data transfer.

## Features
Peer-to-Peer Architecture: Nodes communicate directly, eliminating the need for a central server.
File Replication: Ensures data redundancy by replicating files across multiple peers.
Secure Communication: Utilizes cryptographic techniques to secure data transmission between nodes.
Modular Design: Components like storage, networking, and cryptography are modular, facilitating easy maintenance and extension.
Command-Line Interface: Simple CLI for interacting with the file system.

## Getting Started
Prerequisites
Go 1.16 or higher installed on your system.

## Installation
Clone the repository:

```
git clone https://github.com/anthdm/distributedfilesystemgo.git
cd distributedfilesystemgo
```

Build the project:
```
go build -o dfs
```

This will generate an executable named dfs.

## Usage
Start a node by running:

```
./dfs -port=8000 -peers=localhost:8001,localhost:8002
```
- port: Specifies the port on which the node will listen.
- peers: Comma-separated list of peer addresses to connect with.


Once the node is running, you can interact with it using the CLI:

## Store a file:

```
./dfs store /path/to/local/file.txt
```

Retrieve a file:

```
./dfs retrieve file.txt /path/to/save/file.txt
```

##  Project Structure
main.go: Entry point of the application.

server.go: Handles networking and peer communication.

store.go: Manages file storage and retrieval.

crypto.go: Implements cryptographic functions for secure communication.

store_test.go & crypto_test.go: Unit tests for storage and cryptography modules.

