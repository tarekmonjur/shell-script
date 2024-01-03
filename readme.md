# Shell Script

#### Bash Documnet Commands:

```bash
$ man bash
$ info bash
$ info bash | wc -l
```

### Bash Shell Script File:

-   Fist two characters shoube be `#!` called `shebang` and also exceptable `#!/bin/bash`
-   Kernel system executed this file called execve().
-   Kernel checks for `#!` and passed the path to the orginal program as a comman line argument.
-   So, `./myscript.sh` with `#!/bin/bash` would have the kernel execute `/bin/bash ./myscript.sh`
-   Make scripts executable with `chmod u+x ./shebang.sh`

### Bash Startup:

-   `.bash_profile` is read when Bash is invoked as a login shell.(Basically when we login in system)
-   `.bashrc` is executed when a new shell is started. Basically its executed everytime a new shell is started.
-   Setting environment variable are typically done in `.bash_profile` not in `.bashrc`
-   If we extended an exported variable, like PATH, in `.bashrc`, it will grow with each nested shell invocation.
-   `PATH=$PATH:/usr/local/bin`, This would keep adding `/usr/local/bin` to the end of PATH within nested shell.
-   Aliases and funcitons should normally be defined in `.bashrc`

### Sourcing and Aliases Script:

-   `soruce example.sh` or `. example.sh` its "dot space" as a short way to source a script.
-   When we source a shell script, our current shell just interprets the commands inside the soruce script.
-   The shell executed the script in the shell own's process instead of in a new process.
-   The Alias command allows for short command. `alias ll=ls -la`
-   Unset an alias with the unalias command.

### Echo Command:

Build into bash and doesn't start a new process.

-   `-n` -> don't print a trailing newline.
-   `-e` -> enable backslash escaped characters like `\n` and `\t`
-   `-E` -> disable backslash escaped characters in case by they were enabled by default.
