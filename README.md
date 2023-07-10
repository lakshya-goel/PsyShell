
# PsyShell

This is a basic Linux/UNIX shell made using C.

It implements three internal commands: **echo, pwd, cd**\
and five external commands: **cat, mkdir, rm, ls** and **date**

Standard C libraries, including Linux system calls such as
fork(),exec() family system calls and wait() family of system calls have been utilized.
Basic error handling and two options (or flags) per command have also been implemented.

| Command | Option 1 | Option 2 |
|---------|----------|----------|
| pwd     | -P       | -L       |
| cd      | -P       | -L       |
| ls      | -a       | -l       |
| cat     | -b       | -n       |
| date    | -u       | -r       |
| rm      | -i       | -d       |
| mkdir   | -v       | -p       |

## Modes
The shell has two modes of executing the implemented commands.
- using pthread_create()/system()
- using fork()/execl()

The thread based execution would be performed if the command is followed by the characters, “&t”. The rest of the functionalities remain the same. 


## Deployment

To deploy this project execute

```bash
  makefile
```

