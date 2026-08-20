

#  Safe Malware Attack Simulation

A beginner-friendly cybersecurity project demonstrating how malware can affect files and system permissions, without actually damaging the operating system.

##  About the Project

For this project, I created a controlled malware simulation using Kali Linux running inside VirtualBox.

The goal was not to create real destructive malware, but to understand some of the basic techniques malware can use to affect files and restrict access to them.

To keep the experiment safe, I created a dedicated test directory containing fake files. The simulation only interacted with these files, meaning my actual Kali Linux system and its important files were not targeted. 

##  What I Wanted to Learn

Through this project, I wanted to gain practical experience with:

* Linux file and directory management
* Bash scripting
* File permissions
* The `chmod` command
* Using loops in Bash
* Understanding basic malware behavior
* Creating a controlled cybersecurity testing environment
* Safely documenting the results of a simulated attack

##  Lab Environment

| Component          | Used                           |
| ------------------ | ------------------------------ |
| Operating System   | Kali Linux                     |
| Virtualisation     | VirtualBox                     |
| Scripting Language | Bash                           |
| Text Editor        | Nano                           |
| Test Environment   | Isolated `test_root` directory |

The project was performed inside a virtual machine, with a separate test folder created specifically for the simulation. 

##  How the Simulation Works

The project follows a simple attack simulation:

1. A `test_root` directory is created.
2. Fake files are placed inside the directory.
3. A Bash script called `virus.sh` is created.
4. The script checks the files before the simulation.
5. The files are renamed with a `.broken` extension.
6. File permissions are changed using `chmod 000`.
7. The results are checked after the simulation.

The `.broken` extension represents files that have become unusable, while `chmod 000` simulates a situation where access to files has been completely restricted. 

##  Key Linux Concepts

### `mkdir`

Used to create the isolated test directory.

```bash
mkdir test_root
```

### `touch`

Used to create empty fake files that represent system files.

```bash
touch example.txt
```

### `chmod`

Used to modify file permissions.

In this simulation:

```bash
chmod 000 *
```

removes read, write and execute permissions from the files in the test environment. 

### Bash `for` Loop

The script uses a loop to process multiple files and rename them, allowing the simulation to demonstrate how an automated attack could affect several files.

##  Results

Before the simulation, the files appear normally without the `.broken` extension.

After the script runs, the files are renamed with `.broken`, and their permissions are removed.

This provides visible evidence that the simulation successfully changed the files without affecting the actual operating system. 

##  Safety

**This project is intentionally designed as a controlled simulation.**

The script was created to operate inside a dedicated test directory containing fake files. It was not designed to target real system files or damage the host operating system.

This was an important part of the project because cybersecurity experiments involving destructive behavior should be performed in isolated and controlled environments. 

##  What I Learned

This project helped me connect Linux fundamentals with cybersecurity concepts.

Before this project, commands such as `chmod`, Bash loops and file manipulation could seem like simple Linux commands. Building the simulation helped me understand how these same concepts can become relevant when analysing malicious behavior.

Most importantly, I learned that cybersecurity practicals should be performed safely and deliberately, especially when simulating destructive activity.


##  References

* Linux Documentation Project — `chmod` documentation
* Kali Linux Documentation
* *Counter Hack Reloaded* — Skoudis & Liston

##  Author

**Lulamela Maxakatho**

Diploma in Information Technology | Cybersecurity

This project was completed as part of my cybersecurity studies and is part of my growing practical cybersecurity portfolio.

