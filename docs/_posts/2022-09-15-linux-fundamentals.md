---
id: linux-fundamentals
title: Linux Fundamentals
description: Basic fundamentals and commands
---


Earlier every operating system was designed for a particular hardware for performing a particular task, OS of one system can't be used for another operating system. Then UNIX was invented by Bell Laboratories, and it could be used on any hardware component, just needed a Kernel which was different.

Linux was developed by `Linus Torvalds` as an alternative of UNIX which could be free and easily available for everyone.


## Benefits of Linux

1. Its open source, anyone can download it free from Internet, make changes in the source code according to need, which is also freely available.
2. It is portable for any hardware platform.
3. It was made to keep running.
4. It is the most secure OS and versatile at the same time.

## Architecture of Linux

There are basically four layers in the architecture of the Linux Operating System-

            Hardware
               ^
            Kernel
               ^
             Shell
               ^
          Application layer

1. Application Layer- It is the layer where the user interacts with the various applications or software.
2. Shell- This the layer which acts as an interface between the Application and the Kernel, it is a part of CLI Linux System.
3. Kernel- It is the layer most closest to the hardware, it is specially designed for a particular hardware. It has various functions like to Allocate resources to the processes, allocate memory to particular processes, establishing a connection with external hardware etc.
4. Hardware- It is the innermost layer of this architecture.


## File Permissions in Linux

In Linux there are three types of users for a file:
* Owner of the file
* Users in the group
* Others - who might access the file

We have many files in our system, we can decide who can read the file, execute the file or modify the contents of this file. 
These are particularly known as modes. This makes it very secure.

The commands to change the owner or the modes of a file using `chown` and `chmod` respectively.


## References

* [Intro-Linux](https://linux.die.net/Intro-Linux/index.html)
* [Linux Commands Handbook](https://www.freecodecamp.org/news/the-linux-commands-handbook)
* [Linux Kernel Source Code](https://github.com/torvalds/linux)
