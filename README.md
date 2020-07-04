# Global Github Settings

There are a lot of global settings and configurations that should be applied on
all repos that we have. These settings can be found here.

## Linting

We now use the github [super-linter](https://github.com/github/super-linter)
for all linting. The specific linters for each language are listed below.

| _Language_                | _Linter_                                                                 |
| ------------------------- | ------------------------------------------------------------------------ |
| **CSS**                   | [stylelint](https://stylelint.io/)                                       |
| **Dockerfile**            | [dockerfilelint](https://github.com/replicatedhq/dockerfilelint.git)     |
| **Golang**                | [golangci-lint](https://github.com/golangci/golangci-lint)               |
| **JavaScript/Typescript** | [eslint](https://eslint.org/) [standard js](https://standardjs.com/)     |
| **JSON**                  | [jsonlint](https://github.com/zaach/jsonlint)                            |
| **Markdown**              | [markdownlint](https://github.com/igorshubovych/markdownlint-cli#readme) |
| **Python3**               | [pylint](https://www.pylint.org/)                                        |
| **Shell**                 | [Shellcheck](https://github.com/koalaman/shellcheck)                     |
| **YAML**                  | [YamlLint](https://github.com/adrienverge/yamllint)                      |

To add this workflow to a new project, simply copy `.github/workflows/linting.yml`
into the root of the project.

### Custom Configurations
