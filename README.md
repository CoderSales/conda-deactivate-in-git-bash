# conda-deactivate-in-git-bash

## Setup

`conda` and `git bash`

## Use Automation instead of typing the command

Instead of running the following command in git bash :

``` bash
conda deactivate
```

Use :

## Automation

In `.bashrc` file :

``` .bashrc
alias deactivate_conda="./deactivate_conda.sh"
alias deactivate_conda_base="conda deactivate"
```

In `deactivate_conda.sh` :

``` deactivate_conda.sh
#!/bin/bash
# conda deactivate
```

conda deactivate commented out in script above for the following reason:

ChatGPT3.5 Recommendation/Fix:

``` text
In your deactivate_conda.sh script, you have the following line:
```

```bash

conda deactivate

This line is interpreted as a command to the conda tool,
and it's trying to find a command named
"deactivate"
within conda,
which doesn't exist.

This is causing the error message you're seeing.

To fix this issue,
you should remove the line
conda deactivate
from the deactivate_conda.sh script.

Since you're using the
alias deactivate_conda_base
to deactivate the base Conda environment,
you don't need to manually run

conda deactivate

in your script.
```

In `git bash` cli :

`Mod`ify the `deactivate_conda.sh` shell script to make a `.exe` executable file in the background:

``` bash
$ chmod +x deactivate_conda.sh
```

call the `deactivate_conda.sh` file in the current (`.`) directory :

ChatGPT3.5 recommendation: 

``` text
Just a quick note,
when you use the chmod +x command on a script,
you're making it executable,
which means you can run it directly without specifying the interpreter
(e.g., ./script.sh).

So, in your process, you could directly run
deactivate_conda.sh
without needing to add the
./
before it.
```


``` bash
$ ./deactivate_conda.sh
```

`source` the `.bashrc` file :

``` bash
$ source ~/.bashrc
```

run the `deactivate_conda_base` alias made above in the `.bashrc` file which runs the command `conda deactivate` automatically :

``` bash
deactivate_conda_base
```

## Revised / Summary process iteration 1:

1 :

``` bash
chmod +x deactivate_conda.sh
```

2 :

``` bash
deactivate_conda.sh
```

3 :

``` bash
source ~/.bashrc
```

4 :

``` bash
deactivate_conda_base
```

## Revised / Summary process iteration 2:

1 :

``` bash
source ~/.bashrc
```

2 :

``` bash
deactivate_conda_base
```

## References

[ChatGPT3.5](https://chat.openai.com/)
[Anaconda and Git Bash in Windows: Solving the 'conda: command not found' Issue](https://saturncloud.io/blog/anaconda-and-git-bash-in-windows-solving-the-conda-command-not-found-issue/)
