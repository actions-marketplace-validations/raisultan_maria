```yml
name: Code style check

on:
  pull_request:
    branches: [ master ]

jobs:
  suggest:
    runs-on: ubuntu-latest

    steps:
      - uses: actions/checkout@v2
      - uses: raisultan/maria@main
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```