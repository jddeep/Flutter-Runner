# Github Action for Flutter CLI

This action provides `flutter` for Github Actions.

## Usage examples

This example first cleans any stale build, gets and updates the dependencies with `flutter pub get` and then
builds a release apk to run on all mobile devices(android) and runs the flutter tests in parallel.
