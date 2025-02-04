# sciwork 2024 Conference Repository

[![Netlify Status](https://api.netlify.com/api/v1/badges/2b43093f-4c05-4cdb-b868-963896c28928/deploy-status)](https://app.netlify.com/sites/swconf2024/deploys)

This repository holds the websites for sciwork 2024 annual conferences. The site is hosted at [https://conf2024.sciwork.dev](https://conf2024.sciwork.dev) via Netlify. It is built using [Next.js](https://nextjs.org/) bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app) and [Tailwind CSS](https://tailwindcss.com/).

## Repository Structure

The repository is organized into the following directories:

- `content/`: This directory contains sub-directories for each individual conference. Each sub-directory should be named as `YYYY` where `YYYY` is the conference year. These directories will contain the conference-specific content and configurations.

- `shared-assets/`: This directory contains common assets like logos, font styles, common scripts, and stylesheets that are shared across all the conferences.

- `netlify.toml`: This is the configuration file for Netlify. It instructs Netlify how to build and deploy the sites for the different conferences.

Please refer to the respective README file within each conference's directory for specific details and instructions about that conference's site.

## Getting Started

Before you start, make sure you have the following installed:

- `node` (v18.16.0). We recommend using [nvm](https://github.com/nvm-sh/nvm) to manage your node versions. Once you have `nvm` installed, run `nvm install v18.16.0` to install node. Then use [avn](https://github.com/wbyoung/avn) to automatically switch to the correct node version when you enter the project directory.
- `yarn`

Install the necessary dependencies via:

```bash
yarn install
```

Then run the development server:

```bash
make devserver
```

Open [http://localhost:8000](http://localhost:8000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

To generate static html files for the site, run:

```bash
make html
```

The generated files will be in the `output/` directory.

## Contribution Guidelines

Please follow these steps for contributing:

1. **Fork and clone the repository**
   Fork the project repository to your own GitHub account and clone it to your local machine.

2. **Create a new branch**
   Use a descriptive name for your branches, such as `feature/add-speaker-bio` or `bugfix/registration-link`. This helps others understand the purpose of a branch at a glance.

3. **Develop and test your changes**
   Make the necessary changes in your local project and commit them. Push your branch and changes to your forked GitHub repository. Then, create a Pull Request (PR) against the `develop` branch. In the PR description, describe the changes you've made, the problem they solve, or the feature they add.

4. **Deploy Previews with Netlify**
   Every PR will trigger a Deploy Preview on Netlify. This allows you and others to preview the changes made in a live environment. You can find the Deploy Preview link in the PR checks section on the GitHub PR page.

5. **Review and merge process**
   Await review of your PR. Incorporate any changes requested by reviewers. Once your PR is approved, it will be merged into the `develop` branch. The sciwork team will periodically merge `develop` into `main`, which will publish the changes.

For specific instructions on how to run and develop the site locally, refer to the README file within each conference's directory.

## Deploying to Netlify

We use Netlify to host our site.

- The `main` branch is deployed to the official website [https://conf2024.sciwork.dev](https://conf2024.sciwork.dev) and [https://conf2024.netlify.app](https://conf2024.netlify.app).

- The `develop` branch is deployed to the under development [https://develop--conf2024.netlify.app](https://develop--conf2024.netlify.app).

- Other branches are deployed to `https://{branch}--conf2024.netlify.app`. Replace `/` in the branch name with `-`.

- Pull requests are deployed to `https://deploy-preview-{id}--conf2024.netlify.app`. `{id}` is the PR ID.

To deploy your changes to Netlify, you will need to push your changes to GitHub. Netlify will then automatically detect these changes and rebuild the site.
