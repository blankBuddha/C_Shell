# Operating Systems and Networks

## Assigment 1 - Final Submission

### S Murali Mukunda Bhat

### 2019115006

---

### Overview

>     A shell using the language C with a basic implementation of most commands available on any shell.

---

### Instructions

**To Run**

- Use the makefile to compile the code.
- This can be done by running `make all` in the directory.
- Then run the executable by running `./shell` in the directory.

### Code and Features

- The code is modular broken into various header files where each file has their each unique functions.
- The main file is `shell.c` which starts up the shell.
- `header.h` contains all the required header files to be included in the program.
- `global.h` stores all the required global variables and the funtions for initialising those variables.
- `prompt.h` diplays the prompt accepting username and system name.
- `input.h` takes the input for the shell and parses the input using the **';'** delimiter.
- `execute.h` contains the functions where the parsed input is taken and unnecessary spaces are removed. The required commands are also executed here by calling the required functions.
- `dirop.h` contains the implementation of both the directory operation builtin commands `pwd` and `cd`. Also contains `echo`.
- `peek.h` contains the full execution of the builtin `peek` command with handling of different flags.
- `pinfo.h` contains the implementation of the command `pinfo`.
- `history.h` contains the implementation of the `pastevents` and related commands.
- `backg.h` handles the execvp processes.
- `fbg.h` handles the `fg` and `bg` commands.
- `handlers.h` contains all the signal handlers.
- `pinfo.h` contains the implementation of the `pinfo` command.
- `makefile` contains the makefile for the shell.
- `pipes.h` handles the piping after being parsed by the semicolons and the command chaining symbols.
- `redirect.h` handles all the redirection.
- `ping.h` contains the inbuilt `ping` command.
- `history.txt` contains all the history commands.

---

### Assumptions

- For background processes, it is assumed that if `&` is present at the end of the line, then it is a background process.
- If the argument for the `pastevents` command is greater than the total commands present in the history, then all the history commands are printed.
- There must be no background processes with pipes.
- The output of background processes during redirection is added to the file.
- There cannot be two same redirection symbols in a command.

---
