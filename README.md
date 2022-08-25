# Building an API test automation framework with Python

## Purpose
Code for building an API framework with Python. Once

## Setup

Ensure you have
[pipenv already installed](https://automationhacks.io/2020/07/12/how-to-manage-your-python-virtualenvs-with-pipenv/):

```zsh
# Activate virtualenv
pipenv shell
# Install all dependencies in your virtualenv
pipenv install
```

## Application under test

This automated test suite covers features of `people-api`, Please refer the Github repo
[here](https://github.com/automationhacks/people-api).

Note: These tests expect the `people-api` and `covid-tracker` API to be up. You would find
instructions in the `people-api` repo

## How to run

```zsh
# Setup report portal on docker
# Update rp_uuid in pytest.ini with project token
docker-compose -f docker-compose.yml -p reportportal up -d

# Launch pipenv
pipenv shell

# Install all packages
pipenv install

# Run tests via pytest (single threaded)
python -m pytest

# Run tests in parallel
python -m pytest -n auto

# Report results to report portal
python -m pytest -n auto ./tests --reportportal
```

## Discuss?

Feel free to use the
in this repo to ✍🏼 your thoughts or even use the disqus comments section on the blogs.

Happy learning!
