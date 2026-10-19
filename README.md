# Preregistration Tutorial

This repository holds the training materials on preregistration for advanced learners, published at https://lmu-osc.github.io/preregistration-tutorial/.

The site is built with Quarto using the [`lmu-osc/tutorial-template`](https://github.com/lmu-osc/tutorial-template) extension. To render it locally, run `quarto preview` in the project root.

## Check `CITATION.cff` Format

Repo templates come with a GitHub Action that will check that the `CITATION.cff` file is correctly formatted every time the file is pushed to GitHub (and it will check on any branch to which it is pushed.)

You can also run this check locally with the code below which 1) installs the `cffconvert` checker package, and runs the check (inside of a Docker container). You may need to install Docker and Python 3 if they are not already on your computer.


```{bash}
python3 -m pip install --user cffconvert
docker run --rm -v "${PWD}:/app" citationcff/cffconvert --validate
```
