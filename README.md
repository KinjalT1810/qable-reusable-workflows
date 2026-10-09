
## Shared Node.js Build Workflow

### Workflow File
.github/workflows/reusable-node-build.yml

### Purpose
Provides a reusable Node.js build workflow for consumer repositories.

### Inputs
- app_name (required): Application name displayed in build logs.
- node_version (optional): Node.js version; defaults to 24.

### Example Usage
jobs:
  shared-build:
    uses: KinjalT1810/qable-reusable-workflows/.github/workflows/reusable-node-build.yml@main
    with:
      app_name: github-actions-practice
      node_version: '24'

### Troubleshooting
- Verify the shared workflow path and reference.
- Confirm the workflow defines workflow_call.
- Check that npm ci succeeds in the consumer repository.
- Review the caller workflow's logs for errors.
