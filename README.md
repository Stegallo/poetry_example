# poetry_example
Example of use of poetry form lib management

# run in a fresh 3.11 docker container
```
docker build -t $(basename $(pwd)) .
docker run -it -v $(pwd):/project -w /project $(basename $(pwd)) /bin/bash
```

only at first execution to create the project
```
pip install poetry # is using the container this is redundant

poetry new poetry-example
```

```
cd poetry-example
poetry add pendulum
poetry add black

# if adding to a dependency group
poetry add pytest --group test

# this activate a virtual environment
poetry shell
pip freeze
exit

# reinstall libs (or install from a lock file)
poetry install
poetry install --with test
```
