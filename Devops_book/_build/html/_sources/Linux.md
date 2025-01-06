# Intro to Linux

Linux is an Open-Source Unix based Operating-System based family on the linux kernal, and the OS Kernal was first published on 17th September 1991 by <b>Linus Torvalds</b>. Typically, Linux is packaged as Linux distribution, which contains te supporting libraries, system software and Linux kernal, several of which are offered by GNU Project. Several Linux distributions use the term "Linux" in the title, but the Free Software Foundation uses the "GNU/Linux" title to focus on the necessity of GNU software, causing a few controversies. Famous Linux distribution are RPM, Debian etc.

## History of Linux 

- Early computers are enormous, with each having its own unique operating system, making operation difficult and software incompatible. They were expensive and inaccessible to the general public.

- So to overcome this issue, Bell labs developed Unix in 1969, a simpler and more efficient operating system using C launguage instead of assembly language. Unix was modular, with a recyclable 'Kernal' and it source code was open.

- Initially, Unix was adopted by large organizations like governament bodies, universities, and financial institutions, which used mainframes and minicomputers.

- During the 1980s, companies like IBM and HP created their own Unix versions, leading to fragmentation. Then in 1983, Richard Stallman developed GNU project with the goal to make it freely available Unix like operating system by creating General Public License. GNU stands for <b> GNU's Not Unix </b>. The GNU General Public License (GPL) ensured that software remained free to use, modify, and distribute. By late 1980's many components of GNU were ready, but the kernal (core of the operating system) was incomplete.

- In 1991 Linus Torvalds, a Finnish student, created the Linux kernel as a free Unix alternative for personal use. Initially named "Freax," it became "Linux." He used the GNU C compiler and initially restricted commercial use. In 1992, Torvalds released the Linux kernel under the GNU General Public License, integrating GNU tools and making it free and open-source.

- Today Linux is simply -> Linux kernal + GNU Utilities. Linux is the kernel, one of the essential major components of the system. The system as a whole is basically the GNU system, with Linux added. When you're talking about this combination, please call it “GNU/Linux.”

## Architecture of Linux :

- Linux is majorly consists of 4 layers. Those are :

  **Hardware Layer** : This layer consists of hardware components of the system which are CPU, RAM, ROM, Mother Board etc.

  **Kernal** : On top of hardware components linux kernal is located. This Linux Kernal is the intermediatary between User and Hardware. It actually manages the system resources such as CPU, Memory and I/O devices.

  **Shell** : This is the Command Line Interface for the User to interact with OS.

  **Applications** : On top of all these layers, many applications are situated. File system are also situated here.

- Linux distributions we have today are combination of Linux Kernal + GNU Utilities + Some Customized applications created by some organization for their specific use cases.

## Core Linux Principles

- **Everything is a File** 

  1) In Linux, almost everything (devices, directories, processes, etc.) is treated as a file.

  2) This unifying abstraction simplifies interactions with hardware and software components.

  3) **Ex** :

     - `/dev` contains device files for hardware like disks and terminals.

     - `/proc` provides process and system information as files.

- **Small, Simple and Modular Programs** 

  1) Linux utilities and commands are designed to do one task and do it well.

  2) Programs are kept small and focused, promoting modularity and composability.

  3) <b> Ex </b> : Instead of a monolithic tool, Linux offers separate utilities like grep, awk, sed, and cat for text processing. Monolithic simply implies only single code base used for all the tasks. Non- Monolothic means seperate files are there for respective tasks which is actually linux.

- **Text is the Universal Interface**

  1) Text-based communication is preferred for input, output, and configuration.

  2) Files, logs, and settings are typically stored as plain text, making them easy to read, edit, and process.

  3) <b> Ex </b> : Configuration files like /etc/passwd are simple text files.

- **Open Source Collaboration** 

  1) Linux is developed under the principles of open-source software.

  2) The source code is freely available, encouraging transparency, collaboration, and community contributions.

  3) Ensures security through peer review and rapid bug fixing.

- **Security and User Permissions**

  1) Security is a core principle, with strict access control mechanisms.

  2) Files and resources are assigned ownership and permissions (read, write, execute) for three categories: owner, group, and others.

  3) Principle of least privilege ensures that users and processes have only the permissions they need.

- **Interoperability and Composability**

  1) Linux tools are designed to work together, allowing users to combine them to perform complex tasks.

  2) The output of one program can be used as the input for another via <b>pipes (|)</b>.

  3) <b>Ex</b> : cat file.txt | grep "search" | sort | uniq

- **Flexibility and Customization**

  1) Linux is highly customizable, from the kernel to the user interface.

  2) Users can build and modify their systems to suit specific needs, choosing components like window managers, shells, and tools.

- **Portability**

  1) Linux is designed to run on a wide range of hardware architectures, from embedded systems to supercomputers.

  2) Code written for Linux is highly portable across different platforms.

- **Community Over Corporation**

  1) Linux prioritizes the needs of its community of users and developers over corporate interests.

  2) Development is driven by collaboration and meritocracy.


## Advantages of Linux 

- OpenSource

- Community Support 

- Heavily Customizable

- Most Servers Runs on Linux

- DevOps most of the tools implements on Linux only

- Automation

- Secure

## Different Linux Distributions 

- **Popular Desktop Linux Os**

  1) Ubuntu Linux

  2) Linux Mint

  3) Arch Linux

  4) Fedora

  5) Debian

  6) OpenSuse

- **Popular Server Linux OS**

  1) Red Hat Enterprise Linux

  2) Ubuntu Server

  3) CentOS

  4) SUSE Enterprise Linux

- Today IT Industry, there are only two types of popular linux distros are used. Those are RPM(Red Hat Package Manager) and Debian. The key differences are :

  **RPM** : It uses RPM package format (.rpm files) and its package management tools are `dnf`,`yum` and `rpm`. It is basically derived from Red Hat Enterprise Linux (RHEL). Some of RPM distros are RHEL and Centos, Fedora, OpenSUSE

  **Debian** : It uses debian package format (.deb files) and its package management tools are `apt`, `apt-get` and `dpkg`. It is basically derived from Debian. Some of debian distros are Ubuntu Server, Debian, Linux Mint, Kali Linux.



