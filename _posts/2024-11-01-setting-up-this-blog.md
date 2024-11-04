# Build a Blog with Jekyll & Chirpy on Cloudflare Pages

## Introduction

In today’s digital world, having a personal blog can be a great way to share your thoughts, showcase your projects, or even document your learning journey. Jekyll is a powerful static site generator that makes it easy to turn plain text into beautiful static websites. Whether you want to create a documentation site, a blog, or any other type of website, Jekyll has you covered. Plus, with the Chirpy theme, you can get a polished look with minimal effort. In this post, I’ll walk you through the steps to install and configure Jekyll using the Chirpy theme and host it for free on Cloudflare Pages.

## Prerequisites

Before we dive in, make sure you have the following:

- A GitHub account
- A Cloudflare account
- A domain name registered or managed through Cloudflare

## Getting Started with GitHub

1. **Visit the Chirpy Template**
   - Navigate to the Chirpy GitHub repository.
   - Click on the “Use this template” button to create a new repository.
   - Name your repository and hit the “Create repository” button.

## Setting Up on Cloudflare

Now that we have our template ready, let’s build the initial version of the site.

1. Go to [Cloudflare Dashboard](https://dash.cloudflare.com).
2. Navigate to **Workers & Pages**.
3. Click on **Create**.
4. Select **Pages** and connect to Git.
5. Link your GitHub account if you haven't already. 
6. Choose the repository you just created and click on **Begin Setup**.
7. In the build settings, select **Jekyll** as your framework.

### Add Environment Variables

- **Name**: `BUNDLE_WITHOUT`
- **Value**: `""`
- Click **Save and Deploy**.

Cloudflare will clone your GitHub repository, build the website, and publish it. Once successful, click **Continue Project**. You’ll receive a generated domain name like `blog-joshua-dsylva.pages.dev`.

- Note: On the Free plan, you can build up to 500 times per month. It might take a few minutes before the DNS changes propagate.

## Custom Domain Setup

To make your blog accessible via your own domain, follow these steps:

1. Click on **Custom Domain**.
2. Go to **Set up a Custom Domain**.
3. Enter your domain name and click **Continue**.
4. Review the information and click **Activate Domain**.

This will create a CNAME DNS record linking your custom domain to the generated name.

## Filling Your Blog with Content

With your site set up, it’s time to add some content.

### Clone the Repository

Clone your new blog repository to your local machine.

```bash
git clone git@<YOUR-USER-NAME>/<YOUR-REPO-NAME>.git
cd YOUR-REPO-NAME
