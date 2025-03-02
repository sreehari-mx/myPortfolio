---
title: "Getting Started With Hugo"
description: "A step-by-step giude on how I built my first static website using Hugo and how you can do it too."
date: 2025-02-28
draft: false
weight: 101
cover:
    image: "/blog/getting-started-with-hugo/hugo-logo.png"
---
# How I Built My First Website Using Hugo

## Introduction
Building a website from scratch can seem intimidating ,but static site generators like **Hugo** make it much easier. In this post ,  I'll share my experience of creating my first static website using Hugo and walk you though the process step by step.

## What is Hugo
Hugo is a **lightning-fast static generator** written in Go. It helps you to build websites quickly without needing a database. With Hugo, you can create content using **Markdown** and generate a fully functional website with themes and templates.

## Why I Chose Hugo
- **Fast and lightweight** - Hugo generates pages in milliseconds.
- **Easy to use** - Simple Markdown based content management.
- **Customizable** - Supports themes,templates, and shortcodes.
- **No dependencies** - No need for PHP,database, or CMS.

## Setting up hugo
To get started with Hugo, follow these steps :

### 1. Install Hugo
On Linux/macOS:
```bash
sudo apt install hugo # For Debain-based systems
brew install hugo # For macOS (using Homebrew)
hugo version # For verify the installation
```
On Windows :
- [Visit Hugo's Official Website](https://gohugo.io/installation/windows/)
- Extract the archives and move `hugo.exe` to a folder in your system `PATH`.
- Verify installation :
```bash
 hugo version
```
### 2. Create a New Hugo site
- Run the following command to create a new blog
``` bash
hugo new site my-blog
cd my-blog
```
### 3. Add a Theme
- Visit [Hugo Themes](https://themes.gohugo.io/) and choose a theme.
- I am using the `PaperMod` theme
- Install it using :
``` bash
cd /themes
git clone https://github.com/adityatelange/hugo-PaperMod.git
```
- Edit the hugo.toml/yaml(.yaml can be more flexible) file using any text editor, I prefer `Visual Studio Code` editor.
``` bash
baseURL: ""
languageCode: en-us
title: 
theme: hugo-PaperMod
```
- Give the appropriate `baseURL` and `title`.
- You can customize the page according to the theme you have chosen(Check out the theme documentation)
### 4. Create Your First Blog
``` bash
hugo new posts/my-first-blog.md
```
- Edit the file inside `content/post/` and add your blog content using [Markdown](https://en.wikipedia.org/wiki/Markdown)
- Don't forget to change `draft: true` into `draft : false`

### 5. Run Hugo Locally
- To preview your site , run :
``` bash 
hugo server -D
```
- Open the link `http://localhost:1313/` in your browser.

### 6. Build the Static Site 
- When you are ready to deploy :
``` bash
hugo
```
- This generate a public/folder with your website files.

### 7. Push Your Site to GitHub
#### 1. Creat a GitHub Repository
   - Go to GitHub
   - Click New Reository and give it a name (e.g.,my-blog).
   - Do not add a README,gitignore,or license file.
#### 2. Initialize Git and Push Files
- Now you need to link your Hugo project with GitHub. Run the following commands in your Hugo project folder
``` bash
cd my-blog  # Navigate to the project folder
git init    # Initailize a new Git repository 
git add .   # Stage all files for commit 
git commit -m "Initial commit" # Commit the changes
git branch -M main # Rename the branch to `main`
git remote add origin <repo-url> # Add GitHub repository URL
git push -u origin main # Push the code to GitHub 
```
### 8. Deploy to GitHub Pages
#### 1. Create a gh-pages Branch 
``` bash 
git checkout --orphan gh-pages
git rm -rf .
```
#### 2. Move Generated Files to gh-pages
``` bash
mv public/* .
rm -rf public 
git add .
git commit -m "Deploy Hugo site"
git push origin gh-pages 
```
#### 3. Enable GitHub Pages 
- Go to GitHub repository --> Settings -->Pages.
- Set Source to gh-pages branch and save.
- Your site will be live at 
  ` https:yourusername.github.io/my-blog/`

### Conclusion 
Congratualtions ! You've successfully built and deployed your own **Hugo-powered blog** on **GitHub Pages**.
In this guide, we covered :
- Installing and setting up **Hugo**.
- Creating a **new blog** and adding a theme.
- Writing your **first blog post** .
- Deploying the blog to **GitHub Pages**.
With this setup, you can now focus on **writing great content** without worrying about complex configurations. 
If you find this guide helpful, feel free to **share it with others**.

Happy blogging!

## Sources & Credits
Throughout this journey of building and deploying a **Hugo blog**, I refered to several resources that provided valuable guidance. Here are some of them:
- [Hugo Official Documentation](https://gohugo.io/documentation/) - for learnig Hugo commands and configurations.
- [Hugo Themes](https://themes.gohugo.io/)- To choose and install a theme for the site.
- [GitHub Pages](https://pages.github.com/) - To understand how GitHub Pages works for hosting.
- [https://youtu.be/LIFvgrRxdt4?si=qRrf_WF3hfLLs6Ds](https://youtu.be/LIFvgrRxdt4?si=qRrf_WF3hfLLs6Ds)
- [https://youtu.be/hjD9jTi_DQ4?si=7e_JRhWTbkEeZXWp](https://youtu.be/hjD9jTi_DQ4?si=7e_JRhWTbkEeZXWp)
- [https://youtu.be/EZI9kydYhfA?si=5ChEWWfy2omft1v1](https://youtu.be/EZI9kydYhfA?si=5ChEWWfy2omft1v1)
- If you encounter any problems with the steps, I highly recommend watching the tutorials I've shared above.