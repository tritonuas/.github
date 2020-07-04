# Global Github Settings

There are a lot of global settings and configurations that should be applied on
all repos that we have. These settings can be found here.

## Linting

The standards for linting for all files are defined in `.github/workflows/linting.yml`.
The specific linters used and any custom configurations are found below.

To add this workflow to a new project, simply copy `.github/workflows/linting.yml`
into the root of the project.

| _Language_                | _Linter_                                                                        |
| ------------------------- | ------------------------------------------------------------------------------- |
| **CSS**                   | [stylelint](https://stylelint.io/)                                              |
| **Dockerfile**            | [dockerfilelint](https://github.com/replicatedhq/dockerfilelint.git)            |
| **Golang**                | [golangci-lint](https://github.com/golangci/golangci-lint)                      |
| **JavaScript/Typescript** | [eslint](https://eslint.org/) [standard js](https://standardjs.com/)            |
| **JSON**                  | [jsonlint](https://github.com/zaach/jsonlint)                                   |
| **Markdown**              | [markdownlint](https://github.com/igorshubovych/markdownlint-cli#readme)        |
| **Python3**               | [flake8](https://gitlab.com/pycqa/flake8) [black](https://github.com/psf/black) |
| **Shell**                 | [Shellcheck](https://github.com/koalaman/shellcheck)                            |
| **YAML**                  | [YamlLint](https://github.com/adrienverge/yamllint)                             |

### Custom Configurations

#### Python

```bash
flake8 --ignore=E203,E501,F401,W503
```

[**E203**](https://www.flake8rules.com/rules/E203.html): Whitespace before ':'

- This conflicts with black formatter see
  [this issue](https://github.com/psf/black/issues/315) for justification.

[**E501**](https://www.flake8rules.com/rules/E501.html): Line too long

- The pep8 limit is 79 characters, which can make writing code dumb sometimes

[**F401**](https://www.flake8rules.com/rules/F401.html): Module imported but
unused

- This should by upheld most of the time, but can be useful to have in place
  when creating modules and adding to the `__init__.py` file

[**W503**](https://www.flake8rules.com/rules/W503.html): Line break occurred
before a binary operator

- This is actually inherited from a [pycodestyle
  issue](https://github.com/PyCQA/pycodestyle/issues/513) and is still a
  descrepency with pep8. Black formats this to pep8 and causes an error
  documented [here](https://github.com/psf/black/issues/52)
