## How to start with development

**Prerequisites**

Install [git](https://git-scm.com/) and the development dependencies for Ubuntu 14.04:

```bash
$ sudo add-apt-repository ppa:ubuntugis/ubuntugis-unstable
$ sudo apt-get update
$ sudo apt-get install -y git libgdal-dev libevent-dev python-dev build-essential
$ sudo apt-get install -y libgdal1h libgdal-dev python-gdal
# install git and gdal library for development
```

Install [pyenv](https://github.com/yyuu/pyenv) with the recommended way:

```bash
$ curl -L https://raw.githubusercontent.com/yyuu/pyenv-installer/master/bin/pyenv-installer | bash
```

Add these lines below to the *bashrc* of the *vagrant* user:

```bash
export PATH="/home/vagrant/.pyenv/bin:$PATH"
eval "$(pyenv init -)"
eval "$(pyenv virtualenv-init -)"
# export variable for pyenv
```

At the end run this command:

```bash
$ source .bashrc
```
