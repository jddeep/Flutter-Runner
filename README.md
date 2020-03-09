# Github Action for Flutter Testing

This action provides `flutter` for Github Actions.

## Usage examples

This example first fetches the dependencies with `flutter pub get` and then
builds an apk and runs the flutter tests in parallel.

```
action.yml
name: 'Flutter Mate'
description: ' This action provides flutter for Github Actions.'
runs:
  using: 'docker'
  image: 'Dockerfile'
  ---------------------------------------
main.yml
on: push
name: build and test app
jobs:
  build:
    name: install dependencies
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@master

    - name: install dependencies
      uses: ./action
      with:
        args: pub get

    - name: build apk
      uses: ./action
      with:
        args: build apk --release
```
