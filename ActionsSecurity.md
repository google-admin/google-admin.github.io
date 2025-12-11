# New Security Check for GitHub Actions in Public Repositories

To improve the security posture of GitHub Actions, mitigate PWN request vulnerabilities, and other high-severity CI/CD issues, we are introducing an automated security scan for GitHub Actions for all Alphabet-owned public repositories. This scan will run as a new check on Pull Requests.

## What's changing?

The workflow triggers on Pull Requests affecting `.github/workflows` or `actions` directories to parse for vulnerabilities.

## Impact on Your Pull Requests

You will notice a new status check appearing on your Pull Requests in Alphabet-owned public repositories. This check will **NOT** block merging your Pull Request, even if it doesn't run or fails.

## Understanding Statuses:

*   **Not Run:** For PRs created before implementation of the rule, the check might appear as not run. You can still merge.

*   **Failing:** A failed status indicates potential security issues were found. You can still merge, though caution should be taken to ensure that the potential security issues found are mitigated.

## No Required Action

You do not need to take any special action to merge your PRs.