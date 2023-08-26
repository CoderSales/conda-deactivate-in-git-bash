# conda-deactivate-in-git-bash

## Setup

`conda` and `git bash`

## Use Automation instead of typing the command

``` bash
conda deactivate
```

## Automation

``` .bashrc
alias deactivate_conda="./deactivate_conda.sh"
alias deactivate_conda_base="conda deactivate"
```

``` deactivate_conda.sh
#!/bin/bash
conda deactivate
```

``` bash
$ chmod +x deactivate_conda.sh
```

``` bash
$ ./deactivate_conda.sh
```

``` bash
$ source ~/.bashrc
```

``` bash
deactivate_conda_base
```

## References

[ChatGPT3.5](https://chat.openai.com/)
[Anaconda and Git Bash in Windows: Solving the 'conda: command not found' Issue](https://saturncloud.io/blog/anaconda-and-git-bash-in-windows-solving-the-conda-command-not-found-issue/)
