# GRPC and Distributed Systems

## Project Overview

This project involves designing and implementing a simple distributed file system (DFS) using gRPC and Protocol Buffers. The project is divided into two parts: developing file transfer protocols and incorporating a Weakly Consistent Synchronization system to manage cache consistency between multiple clients and a single server.

## Technologies Used

- **Programming Languages:** C++14
- **Libraries and APIs:** gRPC, Protocol Buffers
- **Tools:** Docker, Gradescope, Visual Studio Code

## Project Structure

### 1. RPC Protocol Service

Implemented the foundational RPC protocol service, enabling basic file operations using gRPC and Protocol Buffers.

- **dfs-service.proto**: Defines the structure of the RPC service, including service methods and message types for requests and responses.
- **Client-Side Implementation**: Handles communication setup, error checking, and streaming of file data for operations like fetch, store, delete, list files, and get file status.
- **Server-Side Implementation**: Listens for incoming RPC calls from clients and performs requested file operations, managing file reads, writes, and metadata retrieval.

### 2. Distributed File System (DFS)

Extended the RPC-based file system to include client-side caching and exclusive file write operations with lock mechanisms.

- **Client-Side Implementation**: Includes file caching, handling server notifications, and acquiring write locks for file operations.
- **Server-Side Implementation**: Manages file locks, sends asynchronous notifications to clients, and ensures caching consistency.

## Key Features

### RPC Protocol Service

- **Service Methods**: Fetch, Store, Delete, ListFiles, and GetFileStatus.
- **Message Types**: Define data structures for requests and responses, ensuring structured and type-safe communication.

### Distributed File System

- **File Caching**: Implements local file caching to reduce read operations from the server.
- **Asynchronous Notifications**: Handles asynchronous callbacks from the server, processing notifications about file changes.
- **Write Lock Acquisition**: Ensures only one client can write to a file at any given time, maintaining consistency.

## Usage
- **RPC Protocol Service**: Handles client requests and performs file operations on the server.
- **Distributed File System**: Enhances file system with caching and synchronization across multiple clients.

## Original Repository
- The original project repository is private since this project was built as part of a class, but I am happy to share it for interview purposes. You can find the original project [GIOS-PR4](https://github.com/NischalKhatri/omscs-gios-pr4). Please reach out to me via email if you would like to access the full repository.
