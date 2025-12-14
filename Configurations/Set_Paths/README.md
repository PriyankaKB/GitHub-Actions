# Set up path to you application

GitHub Actions workflows, you don’t usually hardcode a full path to your application because the runner checks out your repository into a working directory automatically. But if you need to reference the absolute path of your app or files, here’s how you can do it:

**Default working directory:** When your workflow runs, GitHub Actions checks out your repo into the GITHUB_WORKSPACE directory.

**Environment variable:** You can use ${{ github.workspace }} to get the full path to your repository root.

**Relative paths:** Most of the time, you can just use relative paths from the repo root.

For example: 

${{ github.workspace }}/src/app.py


**Note:** It is better to use full path to your files / absolute path while writing your workflow configuration.
