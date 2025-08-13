# README

The PAT needs these permissions:

For Gist Operations:

- gist - Create, read, update, and delete gists

For Cross-Repo Operations (create-gist-cross-repo.yml):

- repo - Full control of private repositories (or public_repo for public repos
only)
  - Needed to checkout/read files from other repositories

How to Create the PAT:

1. Go to GitHub Settings > Developer settings > Personal access tokens > Tokens
(classic)
2. Click "Generate new token (classic)"
3. Select scopes:
  - ✅ gist - For all gist operations
  - ✅ repo - If you need to access private repositories
  - OR ✅ public_repo - If you only need to access public repositories

Summary:

- Minimum for basic gist workflows: gist
- For cross-repo workflow: gist + repo (or public_repo)
- For commenting on issues/releases: Also needs repo to read issue/release content

The PAT determines whose account the gists are created under - they'll appear in
that user's gist list.
