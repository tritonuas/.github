# Global Github Settings

There are a lot of global settings and configurations that should be applied on
all repos that we have. These settings can be found here.

## Linting

The standards for linting for all files are defined in `.github/workflows/linting.yml`.
The specific linters used and any custom configurations are found below.

To add this workflow to a new project, simply copy `.github/workflows/linting.yml`
into the `.github/workflows/` directory of the project and choose the languages
to be used.

| _Language_                | _Linter_                                                                 |
| ------------------------- | ------------------------------------------------------------------------ |
| **CSS**                   | [stylelint](https://stylelint.io/)                                       |
| **Dockerfile**            | [dockerfilelint](https://github.com/replicatedhq/dockerfilelint.git)     |
| **Golang**                | [golangci-lint](https://github.com/golangci/golangci-lint)               |
| **JavaScript/Typescript** | [eslint](https://eslint.org/) [standard js](https://standardjs.com/)     |
| **JSON**                  | [jsonlint](https://github.com/zaach/jsonlint)                            |
| **Markdown**              | [markdownlint](https://github.com/igorshubovych/markdownlint-cli#readme) |
| **Python3**               | [pylint](https://www.pylint.org/) [black](https://github.com/psf/black)  |
| **Shell**                 | [Shellcheck](https://github.com/koalaman/shellcheck)                     |
| **YAML**                  | [YamlLint](https://github.com/adrienverge/yamllint)                      |

### Custom Configurations
