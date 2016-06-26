## Setting up a virtualenv environment

Install your preferred *python* version:
```bash
$ cd ~/development
$ pyenv install 2.7.11
# install python
```

Create new virtual environment:
```bash
$ pyenv virtualenv 2.7.11 geonode
# create virtualenv container
```

Let's go into the virtual environment
```bash
$ pyenv activate geonode
# enter geonode virtualenv
```

Now we are into an isolated environment where we can create an instance of geonode for development
