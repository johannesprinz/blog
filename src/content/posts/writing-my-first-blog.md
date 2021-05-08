---
title: Writing My First Blog
date: 2021-05-02T09:28:33.000Z
draft: false
tags:
  - AzureStaticSite
  - Hugo
  - Blogging
  - Blogumentation
categories:
  - How to
---

## Why

I've been wanting to do this for such a long time. Recently I have had the synchronicity of multiple sources[^Podcasts] reminding me to start blogging or journaling. I see the importance for documenting your own path for reflection, self improvement and the chance for others to learn.

## What

> As an **engineer**
> I would like to **share my learnings** with my **future self**
> So that I can **reflect** on my journey **and improve** my workflow for the next journey.

It needs to be public www.johannesprinz.com to force a certain level of quality by social pressure.

## How

### Choose a blog engine

There are so many to choose from. A quick google gave me the following to look at:

- [Ghost](https://ghost.org/)
  Heard about these a few years ago when I first thought about blogging. This was my first intro to containers then too as they had a development container to launch from.
- [Wordpress](https://wordpress.com/)
  This comes up under almost any related "build a website" search.
- [Jekyll](https://jekyllrb.com/)
  Written in [Ruby](https://www.ruby-lang.org/en/).
- [Hugo](Hugo)

I have settled with [Hugo](Hugo), as I am a fan of markdown for authoring and it had easy quick start guides in all areas I have either familiarity in or wish to learn more about.

### Setup authoring environment

I work with a lot of frameworks and languages in my daily engineering workflow. Keep my main machine as clean as possible is very important to me. What I have found to keep the global scope of my machine clean and free of tooling and framework clutter is container based develop  ment. For this I use [Docker](https://www.docker.com/products/docker-desktop), [Visual Studio Code](https://code.visualstudio.com/) and the [Remote development container extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers). As it turns out [hugo has a development container](https://github.com/microsoft/vscode-dev-containers/tree/v0.158.0/containers/hugo).

1. Follow the [Remote development in Containers](https://code.visualstudio.com/docs/remote/containers-tutorial tutorial to get setup.
2. Setup your workspace and launch VS Code

   ```zsh
   mkdir blog
   cd blog
   git init
   code .
   ```

3. Once VisualStudio Code launches setup hugo development container
   - Open Command Pallet {{< kbd CTRL >}} + {{< kbd p >}}
     {{< figure src="/img/Screenshot 2021-05-06 085428.png" caption="Type `>remote-containers.createDevContainerFile`" >}}
     {{< figure src="/img/Screenshot 2021-05-06 085525.png" caption="Show all definitions" >}}
     {{< figure src="/img/Screenshot 2021-05-06 085605.png" caption="Search for hugo" >}}
     {{< figure src="/img/Screenshot 2021-05-06 085605.png" caption="Reopen in container" >}}
4. From here you can follow the [Hugo quick start](https://gohugo.io/getting-started/quick-start/) guide post the install step.

### Setup pipelines

Now that I can create content I need to enable publishing. I tried publishing to [Github pages](https://docs.github.com/en/pages). I followed this video [Creating a Blog with Hugo and Github in 10 minutes](https://www.youtube.com/watch?v=LIFvgrRxdt4).

> ⚠️ For this to work I needed to name my published repo by the same name as
> the github page url "https://[UserName].github.io".

But then I found this [Tutorial to Publish a Hugo site to Azure Static Web Apps Preview](https://docs.microsoft.com/en-us/azure/static-web-apps/publish-hugo). This setup a static site publishing git hub actions workflow with preview environments within the Pull Request process. Playing with a few GitHub repository settings to secure my main branch I was all set.

### Drafting the first post

At this stage I though I'd nailed it. If someone asked me "When will the first post be published?", I would of replied "Tomorrow". Finding the topic for this one was easy. And here are all the challenges I stumbled across writing my first post.

- Spell checking.
  - Do this via a VS Code extension
- Finding the right theme
- Learning Hugo [Hugo introduction](HugoIntro)
  - Syntax highlighting
    - Using Hugo short codes
  - Rendering of html tags like `<kbd></kbd>`
    - Using Hugo short codes
  - Styling and customising themes

All this ended up taking another few weeks to resolve to a point where I felt it was good enough to publish.

## Todo list

- [x] Choose a blog engine
- [x] Learn more about blog engine
- [x] Find a theme that supports syntax highlighting
- [x] Hosting
  - [x] Explore hosting using Azure blob storage
    Turns out Microsoft (MS) has simplified this into a static site
    hosting service.
  - [x] Explore hosting github pages
  - [x] Explore hosting using Static site hosting
  - [x] Configure DNS to point to hosted site
    - [ ] Make this work on my top level domain
- [x] Refine branching publishing workflow

## What I learned

- [Hugo](Hugo)
  - [Intro](HugoIntro)
- [git submodules](https://git-scm.com/book/en/v2/Git-Tools-Submodules)
- [GitHub Pages]([todo](https://pages.github.com/))
- [GitHub Actions](https://docs.github.com/en/actions)
- [Azure static website service](https://docs.microsoft.com/en-us/azure/static-web-apps/getting-started)

[^Podcasts]: [Podcasts](/podcasts)

[Hugo]: https://gohugo.io/
[HugoIntro]: https://www.youtube.com/watch?v=qtIqKaDlqXo&list=PLLAZ4kZ9dFpOnyRlyS-liKL5ReHDcj4G3
