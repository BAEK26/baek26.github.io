# Personal Website

This repository contains the source code for my personal academic website, built with Jekyll.

## Features

-   Clean and simple design
-   Easy to update content via YAML files
-   Sections for News, Publications, and CV

## Local Development

To set up and run the website locally, you need to have Ruby and Bundler installed.

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/your-username/your-repo-name.git
    cd your-repo-name
    ```

2.  **Install dependencies:**
    ```bash
    bundle install
    ```

3.  **Run the Jekyll server:**
    ```bash
    bundle exec jekyll serve
    ```

4.  Open your browser and navigate to `http://localhost:4000`.

## Customization

You can customize the website by editing the following files:

-   **`_config.yml`**: Main configuration file. Update your personal information, site title, navigation links, etc.
-   **`_data/news.yml`**: Add or update news items.
-   **`_data/publications.yml`**: Add or update your publications. The format is designed to work with the `_includes/publication_item.html` template.
-   **`index.md`**: The main "About" page content.
-   **`cv.md`**: The content for your CV page. You can also replace it with a PDF.
-   **`assets/css/site.css`**: Custom styles for the website.
-   **`images/`**: Place your profile picture and other images here.

## Deployment

This website is designed to be hosted on GitHub Pages. Simply push your changes to the `main` (or `master`) branch of your repository, and GitHub Pages will automatically build and deploy the site. Make sure to configure the repository settings to use GitHub Pages.
