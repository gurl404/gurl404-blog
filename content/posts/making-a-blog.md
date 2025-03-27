+++
date = '2025-03-27T17:58:42-05:00'
draft = false
title = 'Making a Blog'
+++

# Building Your First Blog with Hugo and GitHub Pages: A Step-by-Step Guide

Creating a blog can be an exciting journey, and Hugo makes the process surprisingly straightforward. In this post, I'll walk you through setting up a Hugo blog and deploying it to GitHub Pages, from initial setup to your first published post.

## Getting Started with Hugo

Hugo is a powerful static site generator that allows you to create fast, secure websites with minimal complexity. Let's break down the process step by step:

### 1. Install Hugo

Before we begin, make sure you have Hugo installed. On most systems, you can use package managers:

- macOS (Homebrew): `brew install hugo`
- Windows (Chocolatey): `choco install hugo-extended`
- Linux: `sudo apt-get install hugo`

### 2. Create a New Hugo Site

Creating a new Hugo site is as simple as running a single command:

```bash
hugo new site myblog
cd myblog
```

This command sets up the basic structure for your new blog, creating directories for content, themes, and static files.

### 3. Choose and Install a Theme

Hugo has a wide variety of themes available. For this example, I'll use the popular "Ananke" theme:

```bash
git init
git submodule add https://github.com/theNewDynamic/gohugo-theme-ananke.git themes/ananke
```

Update your `hugo.toml` configuration to use the theme:

```toml
theme = "ananke"
```

### 4. Create Your First Post

Hugo makes creating content incredibly easy:

```bash
hugo new posts/my-first-post.md
```

This command generates a new markdown file in the `content/posts` directory. Open the file and you'll see a pre-populated front matter with metadata like date and draft status.

### 5. Preview Your Site Locally

Before publishing, you can preview your site:

```bash
hugo serve
```

This command starts a local server, typically at `http://localhost:1313`, where you can see your blog in real-time.

### 6. Setting Up GitHub Pages

Deploying to GitHub Pages involves a few steps:

1. Create a new GitHub repository named `<your-username>.github.io`
2. Initialize Git in your Hugo project:
   ```bash
   git init
   git remote add origin https://github.com/<your-username>/<your-username>.github.io.git
   ```

### 7. GitHub Actions for Automatic Deployment

GitHub Actions can automatically build and deploy your Hugo site:

1. In your GitHub repository, go to Actions
2. Choose the Hugo workflow template
3. Commit the generated workflow file

This will automatically build and deploy your site whenever you push changes.

### 8. Writing and Publishing Content

To publish a post, simply edit the markdown file created earlier. Set `draft = false` in the front matter to make it visible.

```markdown
+++
date = '2025-03-27T17:58:42-05:00'
draft = false
title = 'My First Blog Post'
+++

Welcome to my new blog! This is where I'll share my thoughts and experiences.
```

### Pro Tips

- Use `hugo new` to create posts
- Customize your `hugo.toml` for site-wide settings (I changed mine to hugo.yaml)
- Explore Hugo themes to find your perfect design
- Learn markdown for easy content creation

## Conclusion

Setting up a Hugo blog is a powerful way to create a fast, secure, and easily manageable website. With GitHub Pages, you get free hosting and continuous deployment. It's a win-win! 

Happy blogging!
