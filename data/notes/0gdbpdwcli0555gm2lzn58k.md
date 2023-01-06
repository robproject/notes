# GHA 
## releaserc
branches: ['main']
repositoryUrl: 'https://github.com/Robproject/github-actions.git'

plugins: 
- '@semantic-release/commit-analyzer'
- '@semantic-release/release-notes-generator'
- - '@semantic-release/github'

## yml
name: CI
### Controls when the workflow will run
on:
  ### Triggers the workflow on push or pull request events but only for the "main" branch
  push:
    branches: [ main ]
  pull_request:
    branches: [ main ]
  ### Allows you to run this workflow manually from the Actions tab
  workflow_dispatch:
env:
  GH_TOKEN: ${{ secrets. GH_TOKEN }}
### A workflow run is made up of one or more jobs that can run sequentially or in parallel
jobs:
  build:
    # The type of runner that the job will run on
    runs-on: 'ubuntu-latest'
    # use node container with git
    container: 'timbru31/node-alpine-git'
    # Steps represent a sequence of tasks that will be executed as part of the job
    steps:
      # Checks-out your repository under $GITHUB_WORKSPACE, so your job can access it
      - uses: actions/checkout@v3
      # fix permissions (for git)
      - name: Permissions issue
        run: chown $(whoami):$(whoami) -R .
      # create version
      - name: release
        run: npx semantic-release
        
      
