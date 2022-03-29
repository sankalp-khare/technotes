# Managing Python Project Dependencies

I've got pyenv for version selection, but within whatever python version's running, I've most recently used pipenv to manage dependencies and it seems nice.

## Pipenv
pipenv is a wrapper around virtualenv / venv something (not sure which) and I read about it in [the hitchiker's guide to python](https://docs.python-guide.org/dev/virtualenvs/).


### Get pipenv

```bash
pip install --user pipenv
```
### Initialize virtual env + install requirements
Enter project dir, and if it contains a `requirements.txt` you just go

```bash
pipenv install -r requirements.txt
```
and it does the setup of the packages listed in the requirements in a virtualenv.
(this wasn't actually mentioned on the page where I read about pipenv, but I figured I'd give it a try, since it seemed like something `pipenv` should support).

### Use the virtual env
In the project dir, execute

```bash
pipenv shell
```
And it spawns a new shell with the virtual env activated.

### Compatibility with starship prompt

I use [starship prompt](https://starship.rs) and the virtual env setup done by this is detected by it so that's great.
