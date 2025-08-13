# Caller Workflow Templates

These are template workflows you can copy to your repository to call the reusable workflows in this repository.

## Setup Instructions

1. **Add your GitHub Personal Access Token (PAT) to your repository:**
   - Go to your repository's Settings
   - Navigate to Secrets and variables > Actions
   - Click "New repository secret"
   - Name: `GH_PAT` (or whatever name you prefer)
   - Value: Your GitHub PAT with gist permissions

2. **Copy a template workflow to your repository:**
   - Choose a template from this directory
   - Copy it to `.github/workflows/` in your repository
   - Update the secret name from `GH_PAT` to match your secret name

## Available Templates

### create-gist.yml
Creates a GitHub Gist from a markdown file in your repository.

### comment-on-gist.yml
Posts comments to existing GitHub Gists from various sources (files, releases, issues, or direct text).

### update-gist.yml
Updates an existing GitHub Gist with new content from a markdown file.

### create-gist-cross-repo.yml
Creates a GitHub Gist from a markdown file in a different repository.

## Example Usage

After copying a template to your repository:

1. Go to Actions tab in your repository
2. Select the workflow from the left sidebar
3. Click "Run workflow"
4. Fill in the required inputs
5. Click "Run workflow"

## Customization

You can modify these templates to:
- Use different secret names
- Add additional inputs
- Change default values
- Add multiple jobs