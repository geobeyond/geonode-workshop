## How to start with development

**Prerequisites**

Install [git](https://git-scm.com/) and the development dependencies for Ubuntu 14.04:

```bash
$ sudo apt-get install -y git libgdal-dev libevent-dev python-dev build-essential
# install git and gdal library for development
```

Install [pyenv](https://github.com/yyuu/pyenv) with the recommended way:

```bash
$ curl -L https://raw.githubusercontent.com/yyuu/pyenv-installer/master/bin/pyenv-installer | bash
```

Add these lines below to the *bashrc* of the *vagrant* user:

```bash
vi /home/vagrant/.bashrc
#
export PATH="/home/vagrant/.pyenv/bin:$PATH"
eval "$(pyenv init -)"
eval "$(pyenv virtualenv-init -)"
# export variable for pyenv
```

At the end run this command:

```bash
$ source .bashrc
```
