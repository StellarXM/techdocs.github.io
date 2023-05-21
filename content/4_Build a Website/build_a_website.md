---
title: "Build a Local Website"
date: 2023-05-20T17:20:00Z
draft: false
---

## Create a Local Website

In this example, a new site named `techdocs.github.io` is created in the `C:\hugo` directory.

1. Open a command line tool.

   Some command line tools:
    - Microsoft Visual Studio Code (VS Code): Press **CTRL+`** to open the command line terminal.
    - Windows Command Prompt
    - PowerShell
    - Git Bash

2. On the command line, create a website using the following command:

    ```hugo
    hugo new site hugo/techdocs.github.io
    ```

    The website is created with the following default directories (the directories may vary for different themes):

    ```hugo
    |-hugo
        |-bin
            |-hugo.exe
        |-techdocs.github.io     <--Your site directory
            |-archetypes
                |-default.md
            |-assets
            |-content            <--Your site contents
            |-data
            |-layouts
            |-resources
            |-static             <--Static contents (for example, images)
            |-themes             <--Themes that can be used by your website
            |-config.toml        <--Configuration file of your website
    ```

    The `content`, `static`, `themes`, and `config.toml` are main directories and files that are used for setting up the website.

## Install a Hugo Theme for the Website

Hugo has many predefined themes. You can choose a theme that matches your requirements best. In this example, the `Techdoc` theme is used for the website.

1. Choose a theme from the [Hugo Themes (Tag: docs)](https://themes.gohugo.io/tags/docs/) page (for example, `Techdoc`).
2. Click the theme to open the theme page (for example, [https://themes.gohugo.io/themes/hugo-theme-techdoc/](https://themes.gohugo.io/themes/hugo-theme-techdoc/)). The theme page shows the instructins on how to use the theme.

3. On the command line, go to the site directory (for example, `C:\hugo\techdocs.github.io`).

    ```hugo
    cd C:\hugo\techdocs.github.io
    ```

4. Initiate a Git repository.

    ```git
    git init
    ```

5. Add the selected theme to your site directory.

    ```git
    git submodule add https://github.com/thingsym/hugo-theme-techdoc.git themes/hugo-theme-techdoc
    ```

    If the git operation fails, you can download the ZIP archive from [GitHub](https://github.com/thingsym/hugo-theme-techdoc) directly, extract the archive, and place the extracted files to the `C:\hugo\techdocs.github.io\themes` directory.
