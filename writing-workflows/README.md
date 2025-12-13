# GitHub-Actions: Writing Workflows
Create a new workflow file in your application repository (such as .github/workflows/deploy-image.yml), and add the following YAML.

## Sample YAML for self-hosted runners:

name: CI

on: [push, pull_request]

jobs:
  build:
    runs-on: self-hosted
    steps:
    - uses: actions/checkout@v2
    - name: Run a one-line script
      run: echo "Hello, world!"

**References: ** https://docs.github.com/en/actions/concepts/runners/self-hosted-runners

      
