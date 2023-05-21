---
title: "Publish the Website to the Internet"
date: 2023-05-20T17:20:00Z
draft: false
---

## Create a GitHub Repository

1. Go to [GitHub](https://github.com/login).
2. Register a unique GitHub account (for example, `StellarXM`) and log in to GitHub.
3. Create a Git respository in GitHub.
4. In GitHub, click **Create repository**.
5. In the **Create a new repository** page, provide the necessary information.
   - **Repository name**: Provide a unique repository name (for example, `StellarXM.github.io`). The name of the repository must begin with your GitHub user name (for example, `StellarXM`) and be followed by `.github.io`.
   - **Description (optional)**: Optional, provide a short description for this repository if you deem it necessary.
   - **Public**: This option must be selected to create a public repository.
   - **Add a README file**: Optional, select this if you need to write a description for your repository.
6. Click **Create repository** to create the repository.

## Push the Local Website Project to GitHub

In this example, the `StellarXM/StellarXM.github.io.git` GitHub repository name is used. Replace the repository name in the commands with yours.

1. On the command line, go to the site directory (for example, `C:\hugo\techdocs.github.io`).

2. Generate public contents for your website.

    ```hugo
    hugo --theme=hugo-theme-techdoc --baseUrl="http://techdocs.github.io"
    ```

    All local website contents are generated to public contents and placed in the `C:\hugo\techdocs.github.io\pulic` directory.
3. Connect the Git repository with your local project and push the public contents to GitHub.

    ```git
    cd public
    git init
    git config --global user.name "StellarXM"
    git remote add origin https://github.com/StellarXM/StellarXM.github.io.git
    git add .
    git commit -m "first commit"
    git push -u origin master
    ```

4. If required, provide the credentials or authorization to access GitHub.

## Create a GitHub Page for the Documentation Website

1. In GitHub, access your repository (`StellarXM.github.io`) and click **Settings** of the repository.
2. Click **Pages** to open **GitHub Pages**.
3. In **GitHub Pages**, from the **source** drop-down list, select "GitHub Actions".
4. Click the **Configure** button of the Hugo workflow.

   If "Hugo" workflow does not appear by default, click the *browser all workflows" link and search "hugo".

5. Commit the workflow. A workflow is started to create the GitHub page for the Hugo Website.
6. After the workflow is completed, the public site is created successfully and can be viewed by anyone on the Internet.

   ```github
   http://StellarXM.github.io
   ```
