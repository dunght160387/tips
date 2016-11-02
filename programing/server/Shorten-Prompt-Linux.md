Shorten Prompt Linux
====================
The original PS1: ${debian_chroot:+($debian_chroot)}\[\033[01;32m\]\u@\h\[\033[01;34m\] \w \$\[\033[00m\]

The customized SP1:
    - short: 

```
PS1='[\u@\h]\$ $(eval "sps")$ '
sps() {
   echo "$PWD" | sed -r 's|/(..)[^/]*|/\1|g'
}
```

    - more detail: 

```
PS1='${debian_chroot:+($debian_chroot)}\[\033[01;32m\]\u@\h\[\033[01;34m\] $(eval "sps")[\W] \$\[\033[00m\] '
sps() {
   echo "$PWD" | sed -r 's|/(..)[^/]*|/\1|g'
}
```

Open ~/.bashrc or ~/.bash_profile and put customized code to and save and call `source ~/.bashrc` to get update.

More: if directly change for current terminal only, run `PS1=[\u@\h]\$`.
