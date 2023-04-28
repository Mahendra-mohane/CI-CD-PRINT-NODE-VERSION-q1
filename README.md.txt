CI CD PRINT NODE VERSION
Problem
Printing Node Versions: Create a workflow that prints the current version of Node.js. You can use the setup-node action to install Node.js and the run command to execute the node -v command. Here's an example YAML file: yaml

Approach :
name: Print Node Version
on: push
jobs:
  print-version:
    runs-on: ubuntu-latest
    steps:
      - name: Install Node.js
        uses: actions/setup-node@v2
        with:
          node-version: '14.x'
      - name: Print Node Version
        run: node -v