# Demo of xc

There is [IDE support for vscode and VIM](https://xcfile.dev/ide-support/). The [docs](https://xcfile.dev/task-syntax/) are quite good.

## Tasks

This repository is [xc](https://xcfile.dev) compliant.  The following tasks are available:

### demo_input

Try with no arg. Then try with arg

inputs: AN_ARG

```bash
echo $AN_ARG
```

### demo_env

Shows that you can't override MYVAR

environment: MYVAR=Default

```bash
echo $MYVAR
```

### demo_dir

Can't run until the directory exists!

directory: ./build

```bash
echo $PWD
```

### demo_inputs

Try with no args. Then try with just one arg.

inputs: VAR1, VAR2
environment: VAR2=default_var2

```bash
echo $VAR1 $VAR2
```

### demo_requirements

See that both run!

requires: demo_env

```bash
echo requirements met!
```

### demo_shebang

Lets see if python works

```bash
#!/usr/local/bin/python3
print("I'm a real python!")
```

### install

Install our poetry project

```bash
poetry install --with dev
```

### format

Format our poetry project

```bash
isort .
black .
```

### test

Lint and test

```bash
mypy .
flake8 .
pytest
```
