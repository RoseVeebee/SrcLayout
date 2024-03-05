# SrcLayout
Requirements:
* Python
* pip
* Pipenv

Usage:
1. Activate pipenv shell
2. `pipenv update`
3. Run `./main.py` > calls function in mypkg

Structure:
* src layout = pkg(s) to dev in `./src/`
* .venv using Pipenv
* .gitignore: Official Github template for Python.
    * Changed `.venv` to `.venv/*` + `!.venv/.gitkeep`. With default behavior, this forces Pipenv to use `./.venv/` to house venv, instead of default venv location on user's system.
    * Commented out `dist\` in .gitignore to allow `mypkg(...).whl` to be included for demo purposes.
* ^ `./dist/` holds `mypkg(...).whl`. Can be installed to show how src layout forces dev to use installed version of pkg: changing code in `./src/mypkg/` won't impact installed mypkg version.
+ setup.py for mypkg

What is set up:
* Pipfile with -e dev pkg + --dev pytest pkg.
    > Run `pipenv update` after Git pulls to ensure stable venv state.
* Extremely basic setup.py. Recent sources indicate setup.py is outdated: research Poetry (+ Pipenv?) soon.
