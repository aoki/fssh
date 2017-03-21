# fssh

`fssh` is filterd ssh.
This command is very useful when to login with ssh by way of BASTION server.

## Installation

Copy `fssh` function into the your `.bashrc` or `.zshrc` or etc.
Or, copy the `fssh` file into functions directory.
After that, to set aliases like a below.

## Sample Aliases

For example, set arbitrary `BASTION` via environment variable and specify `GREP_WORD` at each environment(like a dev, stage and prod).

Add below aliases to the `.bashrc`, `.zshrc` and etc.
Here, `BASTION` indicate bastion server host.

```
alias ssd='BASTION=dev-bastion GREP_WORD=dev   fssh'
alias sss='BASTION=127.0.0.1 GREP_WORD=stage fssh'
alias ssp='BASTION=example.com GREP_WORD=prod  fssh'
```

Just type `ssd` when if you want login to one of dev environment hosts.
Similarly for `sss` and `ssp`.
