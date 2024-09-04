gh-workflow-test
================

This repository is an example for a single-branch setup with 3 environments:
- any pull request targeting `main` will execute `Checks`;
- once there is a push/merge to `main`, it will execute `Checks`, which, if
  succeeds will "deploy" to the `developer` environment;
- once a Release is created, it will automatically start "deploy" to `Test`;
- once a Release is released (no pre-release flag), it will start "deploy" to `Prod`;

During deployment, it will also update the Deployment Status so there is
feedback on the GitHub Page (and could easily be connected to Slack for example
for receiving alerts).
