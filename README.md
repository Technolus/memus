# Automated Meme Webpages via Discord Bot
This Github repository contains meme webpages automatically generated and deployed on Github Pages via a Discord Bot. The bot uses ChatGPT, an OpenAI API for text generation, to generate a new meme page with a random title and content.

Once the page is generated, the bot uses Octokit, a Github API client, to create a new file in the /memes folder of this repository, set the front matter with the generated title, and add the content to the file. The bot then pushes the changes to Github, triggering a new deployment of the Github Pages site.

This automation helps to keep the site fresh with new content and reduces the manual effort required to add new pages.

The current Github Pages site for this repository can be found at https://{{ site.github.username }}.github.io/{{ site.github.repository_name }}


## Manually adding New Pages to /memes
To add new pages to your Github Pages site, you'll need to create them in the **/memes** folder. Only pages from this folder are displayed in the index at **/**.

Each page should be a **.html** file and have the following at the start:

```
---
title: my awesome title
---
```
Make sure to replace *\`my awesome title\`* with the actual title of your page. This front matter is used by Jekyll to generate the HTML for your page.

Once you've created your new page, you can test it locally by following the instructions in the previous section. Don't forget to push your changes to Github to publish your new page!


## Local Development of Github Pages

Github Pages is a free hosting service provided by Github that allows you to host a static website or blog directly from your Github repository. You can easily create a Github Pages site by creating a new branch called gh-pages or by using the docs folder of your main branch. However, before publishing your site, it's a good idea to test it locally to make sure everything is working as expected.

In this guide, we'll show you how to set up a local development environment for your Github Pages site.

### Step 1: Clone your Github repository
To get started, you'll need to clone your Github repository to your local machine. You can do this by opening a terminal window and running the following command:

```
$ git clone https://github.com/your-username/your-repository.git
```
Make sure to replace your-username and your-repository with your own Github username and repository name.

### Step 2: Install Jekyll
Github Pages uses Jekyll, a static site generator, to build your website. To install Jekyll on your local machine, you'll need to have Ruby installed. You can check if you have Ruby installed by running the following command:

```
$ ruby -v
```
If you don't have Ruby installed, you can download it from the official Ruby website: https://www.ruby-lang.org/en/downloads/.

Once you have Ruby installed, you can install Jekyll by running the following command:

```
$ gem install jekyll bundler
```
This will install Jekyll and its dependencies on your local machine.

### Step 3: Start the Jekyll server
With Jekyll installed, you can now start the local development server by running the following command in the root directory of your Github repository:

```
$ bundle exec jekyll serve
```
This will start the Jekyll server and generate your website. You should see output similar to the following:

```
$ Configuration file: /path/to/your/repository/_config.yml
```
            Source: /path/to/your/repository
       Destination: /path/to/your/repository/_site
 Incremental build: disabled. Enable with --incremental
      Generating...
                    done in 0.123 seconds.
 Auto-regeneration: enabled for '/path/to/your/repository'
    Server address: http://127.0.0.1:4000/
  Server running... press ctrl-c to stop.
The server should now be running at http://127.0.0.1:4000/. You can open this URL in your web browser to view your website.

### Step 4: Make changes and test locally
With the Jekyll server running, you can now make changes to your website and see them in real-time. Simply edit the files in your repository, save your changes, and refresh the page in your web browser to see the changes.

### Step 5: Publish your changes
Once you're happy with your changes, you can publish your website to Github Pages by pushing your changes to the gh-pages branch or the docs folder of your main branch. Github will automatically build and deploy your website to a public URL.

Congratulations, you now know how to set up a local development environment for your Github Pages site!
