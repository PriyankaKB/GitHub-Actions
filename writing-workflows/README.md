# GitHub-Actions: Writing Workflows
Create a new workflow file in your application repository (such as .github/workflows/deploy-image.yml), and add the following YAML.

## Sample YAML for self-hosted runners:


```
name: CI

on: [push, pull_request]

jobs:
  build:
    runs-on: self-hosted
    steps:
    - uses: actions/checkout@v2
    - name: Run a one-line script
      run: echo "Hello, world!"
```

## Workflow Components:

<img width="721" height="515" alt="image" src="https://github.com/user-attachments/assets/10faeede-2bb6-4599-9884-e4666ebc3661" />


### Workflow:
A workflow is an automated process that you add to your repository.

### Jobs:
The job is the first major component within the workflow, a section of the workflow that will be associated with a runner.

### Steps:
A step is an individual task that can run commands in a job.

### Actions
The actions inside your workflow are the standalone commands that are executed. 

**Note:**
For more details on writing workflow you can refer official GitHub documentation on GitHub Actions.


**References:**
https://docs.github.com/en/actions/concepts/runners/self-hosted-runners

      
