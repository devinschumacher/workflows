# Reusable GitHub Actions Workflows

This repository contains reusable GitHub Actions workflows that can be called from other repositories.

## Available Workflows

- **create-gist.yml** - Creates a GitHub Gist from a markdown file
- **comment-on-gist.yml** - Posts comments to existing GitHub Gists
- **update-gist.yml** - Updates existing GitHub Gists
- **create-gist-cross-repo.yml** - Creates gists from files in other repositories

## Usage

In your repository, create a workflow that calls these reusable workflows:

```yaml
name: Create Gist

on:
  workflow_dispatch:
    inputs:
      file_path:
        description: 'Path to markdown file'
        required: true
        type: string

jobs:
  create:
    uses: devinschumacher/workflows/.github/workflows/create-gist.yml@main
    with:
      file_path: ${{ github.event.inputs.file_path }}
    secrets:
      GH_PAT_PROFESSOR_SERP: ${{ secrets.GH_PAT_PROFESSOR_SERP }}
```

