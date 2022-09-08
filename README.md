arcw-action
===========

A GitHub Action for running `arcw`, inspired from https://github.com/ethereum/eipw-action.

## Usage

Here's an example workflow (so it would go in `.github/workflows/ci.yml` or similar):

```yaml
on:
  pull_request:

name: ci

jobs:
  check:
    name: Check
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3.0.2
      - uses: algorandfoundation/arcw-action@dist
        with:
          token: ${{ secrets.GITHUB_TOKEN }}
```

## Building & Deploying

```bash
npm install         # Grab dependencies.
npm run build       # Compile TypeScript and create bundle.
git add .
git commit
git push            # Make the new build available.
```
