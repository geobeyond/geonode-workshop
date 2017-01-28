## How to start with development

**Prerequisites**

Install [git](https://git-scm.com/) and the development dependencies for Ubuntu 16.04:

```bash
$ sudo apt-get install -y git libgdal-dev libevent-dev python-dev build-essential
# install git and gdal library for development
```

Install [pyenv](https://github.com/yyuu/pyenv) with the recommended way:

```bash
$ curl -L https://raw.githubusercontent.com/yyuu/pyenv-installer/master/bin/pyenv-installer | bash
```

Add these lines below to the *bashrc* of the *ubuntu* user:

```bash
vi /home/ubuntu/.bashrc
#
export PATH="/home/ubuntu/.pyenv/bin:$PATH"
eval "$(pyenv init -)"
eval "$(pyenv virtualenv-init -)"
# export variable for pyenv
```

At the end run this command:

```bash
$ source .bashrc
```
