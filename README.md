# DofManga

Static website deployed to GitHub Pages with GitHub Actions.

- Website: https://vuquangdai9x.github.io/DofManga/
- Repository: https://github.com/vuquangdai9x/DofManga
- Workflow: `.github/workflows/pages.yml`

## Development

Edit the files in `site/`. Open `site/index.html` in a browser to preview the starter page locally.
Keep links to local assets relative (for example, `./assets/cover.jpg`) so they work under the `/DofManga/` project path.

## CI/CD

Pull requests targeting `main` check that the HTML entry point exists, has an HTML doctype, and can be packaged.
Every push to `main` runs the same checks, uploads only the contents of `site/`, and deploys them to GitHub Pages.
The workflow can also be started manually from the Actions tab on `main`.

GitHub Pages must use **GitHub Actions** as its publishing source in **Settings → Pages**.
Deployment uses GitHub's built-in workflow token; no deployment secret is required.

If a frontend framework is added later, replace the static preparation step with its installation and build commands,
upload the framework's output directory, and configure its base URL for `/DofManga/`.
