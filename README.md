# ansidrac

testing https://github.com/dell/redfish-ansible-module in nrec

## prerequirements

python>=3.8.6

## virtualenv

check python version >= 3.8: `python3 --version`

create virtualenv with python3: `virtualenv venv -p /usr/bin/python3`

enable venv: `source venv/bin/activate` or `. venv/bin/activate.fish`

then do `pip install -r requirements.txt`

## Install ansible-requirements

`ansible-galaxy collection install -r collections/requirements.yml`

## Compile your own python

```
mkdir ~/opt/python  # ca
wget https://www.python.org/ftp/python/3.10.5/Python-3.10.5.tgz
tar -xvf Python-3.10.5.tgz
cd Python-3.10.5/
./configure --prefix=$HOME/opt/python --enable-optimizations
make
make install
```

### Then back to project dir and create virtualenv

```
cd projectdir
~/opt/python/bin/python3.10 -m venv venv --upgrade-deps
```
