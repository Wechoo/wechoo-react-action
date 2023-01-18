# React Action

## creating a tag

```bash
git tag -a -m "Description of this release" v1
git push --follow-tags
```

## using action

```yml
name: React App

on:
  push:
    branches: [master]
  pull_request:
    branches: [master]

jobs:
  build:
    runs-on: ubuntu-latest
    
    steps:
    - uses: actions/checkout@v3

    - name: Build React app
      uses: wechoo/wechoo-react-action@v1
      with:
        example-input: 'Hello World'
```