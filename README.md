# umn-pages-template

Use this Template to quickly create a UMN Github Pages Site

## Github Actions and Dependabot

Remove the .tmpl file extension from `.github/dependabot.yml` and `.github/workflows/githubpages.yml`

The `dependabot.yml` file will create pull requests to keep your Actions up to date. 

The `githubpages.yml` file deploys your Github Pages site. The Action is configured to run on pushes to 'main' branch and will run on the [UMN Arc Runner](https://github-docs.devex.oit.umn.edu/action-runners/#self-hosted-runners).

## mkdocs.yml
This github pages configuration uses [mkdocs](https://www.mkdocs.org/) to build the site. 

There are several changes needed in the `mkdocs.yml` file. 

```yml
site_name: UMN PLACEHODLER Docs
site_url: https://PLACEHOLDER/
site_description: >-
  PLACEHODLER DESCRIPTION
# [...]
repo_url: https://github.com/umn-PLACEHODLER/PLACEHODLER-docs
repo_name: PLACEHODLER

```

## `/docs` Directory
`README.md` is your front page. 

Every other `.md` file in the `/docs` directory will be a page added to the left navigation bar (ex: `page-one.md`). It uses the first H1 markdown header (ex: `# Page One`) as the title. 

`/stylesheets/color.css` file is configured to a UMN color scheme.  

`/imgs/` has UMN icons. This is also a good directory to put other images you wish to reference in your docs. 

`metadata.json` stores metadata information based on your mkdocs configuration. 

## Pages Configuration on github.com
Configuration for Github Pages is found in your repository Settings tab in the `Code and Automation -> Pages` section. 

GitHub Pages visibility can public (anyone on the internet) or private (anyone has access to your repository).

Build and deployment Source should be set to **GitHub Actions**. 

### Custom Domains

ADD INFO HERE ON GETTING A CUSTOM DOMAIN

Enforce HTTPS should be checked. 