# GitHub Actions
## What are GitHub Actions?
GitHub Actions is a powerful automation tool that allows you to create workflows for your GitHub repository. You can automate tasks like building, testing, and deploying your code.

## Key Concepts
1. Workflow: A defined process consisting of one or more jobs. Workflows are stored in your repository under `.github/workflows/`.

2. Job: A set of steps that execute on the same runner. Jobs can run in parallel or sequentially, depending on dependencies.

3. Step: An individual task that is executed as part of a job. Steps can run commands or use actions.

4. Action: A reusable unit of code that can be used in workflows. You can create your own or use existing ones from the GitHub Marketplace.

5. Event: An occurrence that triggers a workflow, such as a push, pull request, or a scheduled time.

## Getting Started
1. Create a Workflow File
* In your GitHub repository, create a directory called .github/workflows/.
* Inside that directory, create a YAML file (e.g., ci.yml).
### Example of a basic workflow
`name: CI

on:
  push:
    branches:
      - main
  pull_request:
    branches:
      - main

jobs:
  build:
    runs-on: ubuntu-latest
    
    steps:
    - name: Check out code
      uses: actions/checkout@v2
      
    - name: Set up Node.js
      uses: actions/setup-node@v2
      with:
        node-version: '14'
        
    - name: Install dependencies
      run: npm install
      
    - name: Run tests
      run: npm test
`
## Key Components of the Workflow
* `name`: The name of the workflow.
* `on`: Specifies the events that trigger the workflow. Here, it triggers on pushes and pull requests to the main branch.
* `jobs`: Contains the jobs that will run in the workflow.
* `runs-on`: Specifies the type of runner (virtual machine) to use.
* `steps`: The individual tasks within the job.
## Common Actions
* Check Out Code: `actions/checkout@v2` allows you to pull down your repository’s code.
* Setup Node.js: `actions/setup-node@v2` helps set up Node.js on the runner.
* Docker Build: You can use Docker to build images.

## Resources
* GitHub Actions Documentation: [GitHub Docs](https://docs.github.com/en/actions)
* GitHub Marketplace for Actions: [Marketplace](https://github.com/marketplace?type=actions)
* Community Examples: Search for examples on GitHub for inspiration.
## Conclusion
GitHub Actions is a versatile tool for automating your development workflows. By leveraging workflows, jobs, and actions, you can streamline processes like testing and deployment, making your development lifecycle more efficient.

## [Takeaways](takeaways.md)
### [Table of Contents](README.md)
