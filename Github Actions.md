# Github Actions

GitHub Actions are a flexible way to automate nearly every aspect of your team's software workflow. Here are just a few of the ways teams are using GitHub Actions:

* Automated testing (CI)
* Continuous delivery and deployment
* Responding to workflow triggers using issues, @ mentions, labels, and more
* Triggering code reviews
* Managing branches
* Triaging issues and pull requests

In a way, they are like customizable plugins. Similar to how there are plug-ins for Sketch, you can make your own plug-in for git/github.


## How to get started in 3(ish) steps
1. Go to repo. There is an Actions tab at the top.
2. Click "New Workflow"
3. Click "Set up workflow". This creates a .github folder and all the actions are placed in a .yml file

4. Click "Start commit" and create a new branch
5. Create the PR
6. There's a new check for Github Actions

## Action blocks

```
name: A workflow for my Hello World file
on: push

jobs:
    build:
      name: Hello world action
      runs-on: ubuntu-latest
      steps:
        - uses: actions/checkout@v1
        - uses: ./action-a
          with:
            MY_NAME: "Mona"
```

Here are some important details about why each part of the block exists and what each part does.

* `job`: is the base component of a workflow run
* `build`: is the identifier we're attaching to this job
* `name`: is the name of the job, this is displayed on GitHub when the workflow is running
* `steps`: the linear sequence of operations that make up a job
* `uses`: actions/checkout@v1 uses a community action called checkout to allow the workflow to access the contents of the repository
* `uses`: ./action-a provides the relative path the action we've created in the action-a directory of the repository
* `with`: is used to specify the input variables that will be available to your action in the runtime environment. In this case, the input variable is MY_NAME, and it is currently initialized to "Mona".


## Other notes

### Do you need a CI setup in place to use actions?
No, you don't. Github Actions is its own CI in a way. You don't need Jenkins set up.

### List of different actions
https://github.com/marketplace?type=actions


## Links & references
- [Jasper's notes](https://www.notion.so/Github-Actions-101-9fa8e8e281084f33b57ac733517189b3)
- [Features and actions](https://github.com/features/actions)
- Review the [GitHub Actions documentation](https://help.github.com/articles/about-github-actions) on the GitHub Developer site.
- Use existing actions from the [GitHub Marketplace](https://github.com/marketplace/actions).
- Use existing actions from GitHub's [official actions community](https://github.com/actions).
- Use actions created by others in [awesome-actions](https://github.com/sdras/awesome-actions).


---


# Github Actions Learning Session v2
## Goal
Provide the team with an overview of how to create a moderately complex Github action based on the Github JS API. 

## Section 1 - Getting Started (again)
- [ ] Go to your Playbook directory
- [ ] Get the latest from `master`
- [ ] Check out a Playbook branch of your own `gco -b name/github-actions-tutorial-v2`
- [ ] [Visit the landing page](https://github.com/features/actions)
- [ ] [Get started with a new action](https://docs.github.com/en/actions)
- [ ] [Click the â€œQuick Startâ€ button](https://docs.github.com/en/actions/quickstart)

[Events that trigger workflows](https://docs.github.com/en/actions/reference/events-that-trigger-workflows)

## Section 2 - Start Coding
- [ ] [Create your first workflow](https://docs.github.com/en/actions/quickstart#creating-your-first-workflow)
- [ ] Navigate to your `/playbook/.github` directory
- [ ] Under `workflows`, create a new yml named `hello.yml`
- [ ] Copy the contents of `workflows/coverage.yml` to your new file
- [ ] Change the `pull_request` branch to your branch
- [ ] Add the `on: push` section
	- [ ] Ensure the sub-key `branches` exists with your branch name
- [ ] Remove the `Produce Test Coverage Data` section

## Section 3 - Setup your Custom Action
- [ ] Create a directory named `actions/hello`
- [ ] Copy the contents of `actions/badge` to your new directory
- [ ] Modify the `action.yml`  to fit the needs, leaving only these inputs
	- [ ] github-repo
	- [ ] github-token
	- [ ] pull-number
- [ ] Change the `runs` section to point to your new action JS file

## Section 4 - Code your Action 
Reference: [Creating a JavaScript action - GitHub Docs](https://docs.github.com/en/actions/creating-actions/creating-a-javascript-action)

## Section 5 - Test your Action
- [ ] Navigate to https://github.com/powerhome/playbook/settings/secrets/actions and ensure that `ACTIONS_STEP_DEBUG` is there and `true`
- [ ] Push your new branch up to Github and then open PR against `master`
- [ ] At the bottom of the page, look for your actionâ€™s status and click it
- [ ] Watch your action run against your PR

