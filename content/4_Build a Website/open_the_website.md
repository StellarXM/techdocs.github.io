---
title: "Open and Configure the Local Website"
date: 2023-05-20T17:20:00Z
draft: false
---

1. In Windows file browser, copy the `config.toml` file from the `C:\hugo\techdocs.github.io\themes\hugo-theme-techdoc\exampleSite` directory to the `C:\hugo\techdocs.github.io` directory, replacing the existing `config.toml` file. This only needs to be done once.
2. Open the local website.

    ```hugo
    hugo server
    ```

    The command output information `Web Server is available at http://localhost:1313/ (bind address 127.0.0.1)` shows the web address of the local website.
3. Open `http://localhost:1313/` in your web browser.
4. Configure the website to better fulfil your requirements while keeping the website open in your web browser. Your saved changes are reflected in the website timely.

    At least, the following configuration must be made:
    - baseURL: The GitHub repository to be created for the Hugo website, for example, "[http://StellarXM.github.io](http://StellarXM.github.io)"
    - theme: The theme used for the website, for example, "hugo-theme-techdoc"

    For instructions on configuring the Hugo site, see the descriptions of the parameters in the `config.toml` file or the [Hugo Guide](https://gohugo.io/content-management/).
