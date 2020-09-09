# Github Actions

GitHub Actions are a flexible way to automate nearly every aspect of your team's software workflow. Here are just a few of the ways teams are using GitHub Actions:

Automated testing (CI)
Continuous delivery and deployment
Responding to workflow triggers using issues, @ mentions, labels, and more
Triggering code reviews
Managing branches
Triaging issues and pull requests


## How to get started in 3 steps
1. Go to repo. There is an Actions tab at the top.
2. Click "New Workflow"
3. Click "Set up workflow". This creates a .github folder and all the actions are placed in a .yml file

4. Click "Start commit" and create a new branch
5. Create the PR
6. There's a new check for Github Actions

## more about it

<iframe src="https://share.getcloudapp.com/geuzDqeQ?embed=true" width="100%" height="100%" style="border:none" frameborder="0" allowtransparency="true" allowfullscreen="true"></iframe>

Here are some important details about why each part of the block exists and what each part does.

jobs: is the base component of a workflow run
build: is the identifier we're attaching to this job
name: is the name of the job, this is displayed on GitHub when the workflow is running
steps: the linear sequence of operations that make up a job
uses: actions/checkout@v1 uses a community action called checkout to allow the workflow to access the contents of the repository
uses: ./action-a provides the relative path the action we've created in the action-a directory of the repository
with: is used to specify the input variables that will be available to your action in the runtime environment. In this case, the input variable is MY_NAME, and it is currently initialized to "Mona".


## Other Notes
Do you need a CI setup in place to use actions? No, you don't. Github Actions is its own CI in a way. You don't need Jenkins set up.

## References
https://github.com/features/actions
Jasper's notes: https://www.notion.so/Github-Actions-101-9fa8e8e281084f33b57ac733517189b3
https://github.com/christinaatai/hello-github-actions/issues/1
