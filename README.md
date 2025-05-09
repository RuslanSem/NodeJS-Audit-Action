# NPM Audit Action

This GitHub Action runs `npm audit` to check for vulnerabilities in your Node.js project.

## Usage

Create a workflow file (e.g., `node.yml`) in your repository:

```yaml
name: NPM Audit

on:
  push:
    branches:
      - main
  pull_request:
    branches:
      - main

jobs:
  audit:
    runs-on: ubuntu-latest
    steps:
      - name: Run NPM Audit
        uses: RuslanSem/npm-audit-action@v1
        with:
          node-version: 'latest'
```

## Inputs

| Input         | Description                          | Default |
|---------------|--------------------------------------|---------|
| `node-version`| Specify the Node.js version to use.  | `latest`    |

## Outputs

This action does not produce any outputs.

## License

MIT License.
