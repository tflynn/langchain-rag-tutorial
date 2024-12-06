Ubuntu 24.04 and Python 3.12 and later versions of both

The installed system version of Python 3 is now protected. It can no longer be updated using 'pip3'.

The full solution is described below.

* Install python3-pip3 and python3-venv using system packages.

```sudo apt install python3-pip```

* Create a local python3 venv to be the target of non-qualified 'pip3 install' commands. Activate. This works nicely in your shell startup file.

```
# You can name the location and the venv any way you want.
# Adjust as appropriate.
mkdir -p $HOME/.venvs
if [[ ! -d $HOME/.venvs/standard ]]; then
  cd $HOME/.venvs
  python3 -m venv standard
fi
source $HOME/.venvs/standard/bin/activate
```

