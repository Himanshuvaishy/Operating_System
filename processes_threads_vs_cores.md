# 🧠 How Processes and Threads Utilize CPU Cores

## 🔧 What is a Process?

A **process** is an independent program in execution. It has its own:
- Memory space (code, data, stack, heap)
- System resources (file handles, registers)

🧠 Think of it like an **app running on your system** (e.g., Chrome, Spotify, VS Code).

## 🧵 What is a Thread?

A **thread** is a lightweight unit of a process.
- A process can have **one or more threads** (called multithreading).
- Threads **share the same memory** of the process but **have their own execution context** (stack, registers).

🧠 Think of a thread as a **sub-task** of a process.

---

## ⚙️ How CPU Cores Are Utilized

### 🔹 1. **Single-Core CPU**

- Can execute **only one thread** at a time.
- If you have multiple processes, they are scheduled using **time slicing** (very fast switching).

```text
Time  → |  Chrome |  VS Code |  Terminal |  Chrome |  VS Code | ...
Core  → |    1    |    1     |     1     |    1    |    1     | ...
