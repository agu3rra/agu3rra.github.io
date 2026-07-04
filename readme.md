# Andre Guerra's Blog
Welcome to the code repo that powers my personal blog.

Built with [Zensical](https://zensical.org/) and Python's [`uv`](https://docs.astral.sh/uv/).

## Local setup
```bash
git clone https://github.com/agu3rra/agu3rra.github.io.git
cd agu3rra.github.io

# Install dependencies
uv sync

# Activate virtual environment
source .venv/bin/activate

# Serve the blog locally
zensical serve -a localhost:8088
```

## Repository setup
Go to your repository on GitHub and make sure you select **Settings → Pages → Build and deployment → Source →  GitHub Actions**. This allow the current pipeline to build and deploy the blog automatically on every merge to `main`.