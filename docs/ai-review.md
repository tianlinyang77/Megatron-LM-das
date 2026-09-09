# AI-assisted pull request review

The installed GitHub App reviews non-draft pull requests when they are opened,
updated with new commits, reopened, or marked ready for review. No label is
required. Review feedback appears as a PR comment and does not replace human
review or required CI checks.

For a completed, failed GitHub Actions workflow, the App can post a separate
failure analysis using available failed-job logs and the PR diff. This requires
Actions read permission and an explicit workflow-run association with the
current PR revision. Missing logs or missing PR associations limit the analysis.

The App reads changes through the GitHub API. It does not execute PR code,
modify repository files, rerun workflows, approve changes, or merge PRs.
