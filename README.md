# RAFT Consensus Algorithm Implementation

## 📌 Overview
This repository contains an **implementation of the RAFT consensus algorithm** in **Go**. The implementation leverages a **custom-built remote library** to facilitate **Remote Procedure Calls (RPCs)** between RAFT peers, ensuring distributed consensus across multiple servers.

The RAFT consensus algorithm is designed to manage **replicated logs in distributed systems** and ensures **leader election, log replication, and fault tolerance**.

---

## 🚀 Features
- **RAFT Peer Management**: Handles the interaction between nodes in the RAFT cluster.
- **Leader Election**: Nodes vote to elect a leader in case of failures.
- **Log Replication**: Ensures consistency across nodes by synchronizing logs.
- **Heartbeat Mechanism**: Prevents leader re-elections by periodically sending heartbeats.
- **Remote Procedure Call (RPC) Handling**: Implements efficient inter-node communication.

---

## 📚 Reference Papers & Resources
This implementation is based on the following references:
- [Extended RAFT Paper - MIT](http://nil.csail.mit.edu/6.824/2020/papers/raft-extended.pdf)
- [RAFT Official Website](https://raft.github.io)
- [Distributed Systems Notes - University of Cambridge](https://www.cl.cam.ac.uk/teaching/2021/ConcDisSys/dist-sys-notes.pdf)
- Various **articles** and **YouTube tutorials**.

---

## 📂 Project Structure
```
├── remote/   # Contains the custom-built remote library for handling RPCs
├── raft/     # Contains the RAFT implementation
```

- **`remote/`**: Handles all **RPC interactions** between RAFT nodes.
- **`raft/`**: Contains the core **RAFT consensus algorithm** implementation.


```plaintext
.
├── Makefile
├── README.md
└── src
    ├── go.mod
    ├── raft
    │   ├── raft.go
    │   └── raft_test.go
    └── remote
        └── remote.go
```

---


## *You can use the boiler plate code and implement yourself*

## 🛠️ Implementing RAFT
### **Initial Setup**
- Copy your **remote library** code from **Lab 1** into `src/remote/`.
- The `raft` package includes a **base structure** aligned with the RAFT paper and **test suite requirements**.
- Your goal is to **complete the RAFT protocol implementation**, ensuring compliance with the **Canvas assignment specifications**.

### **Development Guidelines**
- You **can create additional files** in the `raft/` package as needed.
- Use **appropriate data structures, functions, and Go routines**.
- Ensure compatibility with the **existing test suite** (`raft_test.go`).
- Read the **test cases and controller logic** to understand the expected behavior.

---

## ✅ Testing Your RAFT Implementation
Once you are ready to test your implementation:

### **Using Go Test Commands**
```sh
go test ./raft
```

### **Using Makefile Rules**
The Makefile includes predefined **test execution rules**:
- **`make checkpoint`** – Runs checkpoint tests.
- **`make final`** – Runs final evaluation tests.
- **`make all`** – Runs all test cases.
- **`make checkpoint-race`**, **`make test-race`**, **`make all-race`** – Execute tests with Go's **race detector** to ensure thread safety.

> 🚀 **Pro Tip:** You are encouraged to create **your own additional tests** for further validation!

---

## 📄 Generating Documentation
To ensure **clear and readable package documentation**, we encourage writing detailed comments in the codebase.

### **Generate Documentation Using Makefile**
```sh
make docs
```
This command pipes `go doc` output into a **formatted text file** for easy navigation and manual grading.

---
🚀 **RAFT Consensus Algorithm Implementation - Ensuring Reliable Distributed Consensus!**

