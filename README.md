# Cloud Computing - Github Actions: Automating testing workflow for the Polycube open-source project
This project aims at migrating the Polycube testing, which involves several VMs and Docker, into a "managed" service, the one provided by GitHub, hence freeing precious CPU (and human) resources at the POLITO premises.

## Prerequisites
### What is CI/CD?
Continuous integration (CI) and continuous delivery (CD) embody a culture, set of operating principles, and collection of practices that enable application development teams to deliver code changes more frequently and reliably. The implementation is also known as the CI/CD pipeline. 

CI/CD is one of the best practices for DevOps teams to implement. It is also an agile methodology best practice, as it enables software development teams to focus on meeting business requirements, code quality, and security because deployment steps are automated.

For more details you can also see [CI/CD Pipline](https://www.youtube.com/watch?v=Rq5TQlPyr8g&feature=emb_logo)

### What is YAML?
YAML is a data-orientated human readable serialization language, and I have come across it in many projects including OpenAPI, Docker, Kubernetes and Ansible playbooks among others.

YAML was originally an acronym for 'Yet Another Markup Language', but is now more commonly referred to as 'YAML Ain't Markup Language' (a bit like GNU is not unix!, or Bing! is not google!).

For basic rules you can learn [YAML in 5 minutes](https://www.codeproject.com/Articles/1214409/Learn-YAML-in-five-minutes)

### What is Docker? container and image?
Docker is an open source containerization platform. Docker enables developers to package applications into containers—standardized executable components that combine application source code with all the operating system (OS) libraries and dependencies required to run the code in any environment.

A Docker container image is a lightweight, standalone, executable package of software that includes everything needed to run an application: code, runtime, system tools, system libraries and settings.

Images become containers when they run on Docker Engine. 

### What is Jenkins?
Jenkins is an open-source server that is written entirely in Java. It lets you execute a series of actions to achieve the continuous integration process, that too in an automated fashion.

This CI server runs in servlet containers such as Apache Tomcat. Jenkins facilitates continuous integration and continuous delivery in software projects by automating parts related to build, test, and deployment. This makes it easy for developers to continuously work on the betterment of the product by integrating changes to the project.

## Why Github Actions?
You can create custom continuous integration (CI) and continuous deployment (CD) workflows directly in your GitHub repository.

Workflows can run on GitHub-hosted virtual machines (spare time on setup and mantains Jenkins servers), or on machines that you host yourself.

GitHub offers CI workflow templates for a variety of languages and frameworks and a community-powered workflows.

## Learn Github Actions

### Overview
GitHub Actions help you automate tasks within your software development life cycle. GitHub Actions are event-driven, meaning that you can run a series of commands after a specified event has occurred.

### Components

#### Workflows 
The workflow is an automated procedure that you add to your repository. Workflows are made up of one or more jobs and can be scheduled or triggered by an event. The workflow can be used to build, test, package, release, or deploy a project on GitHub.

#### Events
An event is a specific activity that triggers a workflow. For example, activity can originate from GitHub when someone pushes a commit to a repository or when an issue or pull request is created. You can also use the repository dispatch webhook to trigger a workflow when an external event occurs. For a complete list of events that can be used to trigger workflows, see Events that trigger workflows.

#### Jobs
A job is a set of steps that execute on the same runner. By default, a workflow with multiple jobs will run those jobs in parallel. You can also configure a workflow to run jobs sequentially. For example, a workflow can have two sequential jobs that build and test code, where the test job is dependent on the status of the build job. If the build job fails, the test job will not run.

#### Steps
A step is an individual task that can run commands (known as actions). Each step in a job executes on the same runner, allowing the actions in that job to share data with each other.

#### Actions
Actions are standalone commands that are combined into steps to create a job. Actions are the smallest portable building block of a workflow. You can create your own actions, or use actions created by the GitHub community. To use an action in a workflow, you must include it as a step.

#### Runners
A runner is a server that has the GitHub Actions runner application installed. You can use a runner hosted by GitHub, or you can host your own. A runner listens for available jobs, runs one job at a time, and reports the progress, logs, and results back to GitHub. For GitHub-hosted runners, each job in a workflow runs in a fresh virtual environment.

## Play with Docker and Github Actions
I recommend you to see [Configure GitHub Actions](https://docs.docker.com/ci-cd/github-actions/) that show how we can set up a basic workflow with optimization features and push on GitHub Container Registry a tagged version of a Docker container image.
