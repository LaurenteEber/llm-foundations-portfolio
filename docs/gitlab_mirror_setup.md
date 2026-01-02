# GitLab mirror setup

This repository is hosted on GitHub as the primary source of truth, and mirrored to GitLab for redundancy.

## Why a GitHub Action mirror

GitLab's built-in repository mirroring (pull mirrors) is not available on the GitLab Free tier. See GitLab documentation for details.

Therefore, the recommended approach is to mirror **from GitHub to GitLab** using a GitHub Action that pushes every change to a GitLab remote.

## Steps (SSH deploy key)

### 1) Create an empty GitLab repository

Create a new GitLab project (public or private). Do not add a README if you want the histories to match cleanly.

### 2) Create an SSH key pair for mirroring

On your local machine:

```bash
ssh-keygen -t ed25519 -C "github-to-gitlab-mirror" -f gitlab_mirror_key
```

This will create:
- `gitlab_mirror_key` (private key)
- `gitlab_mirror_key.pub` (public key)

### 3) Add the public key to GitLab

In your GitLab project:
- Go to **Settings → Repository → Deploy keys**
- Add `gitlab_mirror_key.pub`
- Enable **Write access** for the deploy key

### 4) Add secrets to GitHub

In GitHub:
- Go to **Settings → Secrets and variables → Actions**
- Add the secrets:

- `GITLAB_SSH_PRIVATE_KEY`: paste the full contents of `gitlab_mirror_key`
- `GITLAB_SSH_URL`: for example:

```text
git@gitlab.com:<your-gitlab-username>/<your-repo>.git
```

### 5) Enable the workflow

This repository includes `.github/workflows/gitlab-mirror.yml`.

Once the secrets are added, every push to `main` will be mirrored to GitLab automatically.
