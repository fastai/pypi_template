# pypi template

> A minimal template for creating a pypi package

Use this template to more easily create a project project to submit to pypi and conda.

## How to use the template:

- [Click here](https://github.com/fastai/pypi_template/generate) to create a new repo (you need to be logged in to GitHub for this link to work), and follow the instructions to create a new repo from this template
- `git clone` your new repo
- Edit `settings.ini` and fill out all the requested information (you can ignore parts starting with `%`)
- Install [fastrelease](https://fastrelease.fast.ai/), [twine](https://twine.readthedocs.io/en/latest/), and [conda-build](https://docs.conda.io/projects/conda-build/en/latest/)
- Register at [pypi](https://pypi.org/account/register/) and [Anaconda](https://anaconda.org/)
- Create a file called `~/.pypirc` with your pypi login details, as follows:

```
[pypi]
username = your_pypi_username
password = your_pypi_password
```

- Write your Python library!
- Add any package requirements to the `requirements` line in `settings.ini`
- Run `make release` in the root of your repo. This will automatically:
  - Publish to pypi
  - Publish to Anaconda
  - Increment your version number
