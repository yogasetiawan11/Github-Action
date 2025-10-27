# ⚙️ Introduction to GitHub Actions and CI/CD Comparison
## What is GitHub Actions (GHA)?

GHA is another CI/CD solution that is specifically focused on the GitHub platform.

## GHA vs Jenkins (and other CI tools)

- Platform Lock-in: The biggest disadvantage of GHA is its limitation to the GitHub platform. If your organization might migrate to other platforms CI/CD like GitLab or Azure DevOps, GHA is not the recommended solution.

- Hosting and Maintenance: GHA eliminates the need for hosting/maintenance effort required by Jenkins (e.g., setting up EC2 instances, installing Jenkins, managing plugins, and updates).

- User Interface: Writing a GHA pipeline is simpler than a Jenkins pipeline.

- Cost: GHA is typically free for public/open-source projects and has a low cost with less overhead for private repositories, making it more cost-effective than managing a self-hosted Jenkins setup.

## 📝 GitHub Actions Pipeline Structure
- Configuration Files: GHA workflows are defined in YAML files placed in the directory: .github/workflows/ .

- Events (on): You define specific Git or GitHub activities (events) that will trigger the pipeline execution, such as on push (commit), on pull request, or on issue.

- Jobs: A workflow can contain multiple jobs, which simmilar to pipelines in Jenkins.

- Runner Environment: Each job defines the execution environment using an image like runs-on: ubuntu-latest.

- Matrix Testing: You can use a matrix strategy to test your application against multiple versions of a tool (e.g., Python 3.8 and 3.9) with a single configuration.

- Steps: Inside a job, you define sequential steps (like stages in Jenkins) that execute commands or use pre-built actions.

## 🛠️ Key Components and Examples
Actions (Plugins): GHA uses a Marketplace of pre-built actions (plugins) that are automatically installed, unlike Jenkins where you manually manage plugins.

- actions/checkout@v3: A standard action used to fetch the code from the repository.

- actions/setup-python@v2: A standard action to configure a specific language environment.

Refer to this [documentation](https://docs.github.com/en/actions/get-started/understand-github-actions) to see example of Github.