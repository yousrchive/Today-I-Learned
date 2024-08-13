# In case with python conflict

I've faced with many cases with errors saying that `PYTHON3 does EXIST BUT PIP does not`. In the case, the path where library is installed might makes the conflict.

**Following materials is how I solved the issue.**

```
rm -rf .venv
```

```
python3 -m venv .venv
```

`DELETE` the existing .venv, replacing with newly installed.

```
source .venv/bin/activate
```

```
python -m ensurepip --upgrade
```

It is how you can install pip on virtual environment.

If you are MAC USERS, use `HOMEBREW` for reinstalling Python and pip.

```
Brew reinstall python
```

```
pip install package_name
```

In my case, pipx and pip3 couldn't make it possible to install seaborn library. But the code made it to have seaborn with me now.