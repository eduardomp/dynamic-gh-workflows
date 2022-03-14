# Dynamic GH workflows

Repository with dynamic workflows that receive inputs (manually or not) to test, build and publish artifacts from target repos.

## Prerequisites

- 1 Create a secret called PAT with the value of your personal access token on the target repo.

- 2 Copy the file .github/workflows/start.yml to your target repo (on .github/workflows/start.yml) to execute remotelly the operations, or you can trigger manually in this repo if you want.

- 3 Copy the file pipeline.properties to the root of your target repo if you want to use the properties file to configure the workflow when your target repo receive a push event.

- 4 You need to be a collaborator or owner of this repo, and have access to the target repo. Using PAT secret in both of then.

## Features

- [x] Execute tasks based on choosen stack
- [x] windowns runner
- [x] using start.yml in the app, to remote call the workflows
- [x] add an pipeline.properties with a combination of inputs
- [x] PAT as a secret
- [x] maven goals
- [x] optimize checkout in the workflows, sharing the directory of source code (jobs reduced to accomplish this task)
- [x] build number that can be added to the generated artifacts as part of publish
