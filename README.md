# GitHubActionslab-HaspinderDhillon

This is my InClass 05 

Created two workflows to show different GitHub Actions, including job dependencies and running jobs on multiple operating systems.

Workflow 1: Dependent Jobs Workflow

The first workflow was created to demonstrate job dependencies using the `needs` keyword.

This workflow contains three jobs:

1. Build
2. Test
3. Deploy

The jobs are executed in sequence. The test job only starts after the build job is completed successfully, and the deploy job only starts after the test job finishes successfully. This helped me understand how workflows can be organized to follow a specific order of execution.

 Concepts Demonstrated

* **needs** – Used to create dependencies between jobs.
* **runs-on** – Specifies the operating system used to run a job.
* **push trigger** – Automatically runs the workflow when changes are pushed to the main branch.


  Workflow 2: Multi-Platform Testing

The second workflow was created to demonstrate how GitHub Actions can run jobs on different operating systems at the same time.

This workflow includes three independent jobs:

* Ubuntu Job
* Windows Job
* macOS Job

Since there are no dependencies between these jobs, GitHub Actions runs them in parallel. Each job checks out the repository, displays operating system information, and performs a simple task to confirm successful execution.

### Concepts Demonstrated

* **runs-on** – Used to run workflows on Ubuntu, Windows, and macOS.
* **actions/checkout@v4** – Checks out repository code before executing steps.
* **pull_request trigger** – Automatically runs the workflow when a pull request is created.


## Environment Variables (env)

Although this lab primarily focused on job dependencies and multi-platform execution, GitHub Actions also supports environment variables using the `env` keyword. Environment variables can be defined at the workflow, job, or step level and can be reused throughout a workflow to simplify configuration and improve maintainability.



## Challenges Faced

One challenge I faced was understanding how workflow triggers work and when a workflow actually executes. Initially, I had difficulty distinguishing between workflows triggered by a push event and those triggered by a pull request.

Another challenge was making sure workflow files were placed in the correct `.github/workflows` directory. After reviewing the workflow structure and testing multiple runs through the Actions tab, I was able to identify and correct the issue.

Working through these problems helped me gain a better understanding of how GitHub Actions workflows are configured, triggered, and monitored.



## Conclusion

This lab provided hands-on experience with GitHub Actions and demonstrated how workflows can automate development tasks. Through creating dependent jobs and multi-platform workflows, I learned how to control job execution, work with different runners, and monitor workflow activity using GitHub's Actions interface.

