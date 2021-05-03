---
title: "Writing My First Blog"
date: 2021-05-02T09:28:33Z
draft: true
tag: ["AzureStaticSite", "Hugo", "Blogging", "Blogumentation"]
category: ["How to"]
---

## Why

I've been wanting to do this for such a long time. Recently I have had the synchronicity of multiple sources[^Podcasts] reminding me to "Just get started" and the importance for documenting your own path using blogs or journaling.

## What

> As an **engineer**
I would like to **share my learnings** with my **future self**
So that I can **reflect** on my journey **and improve** my workflow for the next journey.

It needs to be public www.johannesprinz.com to force a certain level of quality by social pressure.

## How

### Choose a blog engine

There are so many to choose from. A quick google gave me the following to look at:

- [Ghost](https://ghost.org/)
  Heard about these a few years ago when I first thought about blogging. This was my first intro to containers then too as they had a development container to launch from.
- [Wordpress](https://wordpress.com/)
  This comes up under almost any related "build a website" search.
- [Hugo](Hugo)

I have settled with [Hugo](https://gohugo.io/), as I am a fan of markdown for authoring and it had so many compelling quick start guides in all areas I have either familiarity in or wish to learn more about.

- Links to get started [todo](todo)
- [x] Learn more about blog engine

### Setup authoring environment

I meddle with a lot of frameworks and languages in my daily engineering workflow and to keep my main machine as clean as possible is very important to me. The best way I have found to keep the global scope of my machine clean and free of tooling and framework clutter, I have wholeheartedly adopted the use of container based development. For this I use [Docker](#todo), [Visual Studio Code](https://code.visualstudio.com/) and the [Remote development container extension](https://code.visualstudio.com/docs/remote/containers-tutorial). As it turns out [hugo has a development container](https://github.com/microsoft/vscode-dev-containers/tree/v0.158.0/containers/hugo).

```zsh
mkdir blog
cd blog
git init
code .
# Once VisualStudio Code launches
# - open command pallet (ctrl + p)+(>)
# - create development container (search for hugo)
```

From here you can follow the [Hugo quick start](https://gohugo.io/getting-started/quick-start/) guide post the install step.

- [ ] Hosting
  - [x] Explore hosting using Azure blob storage
    Turns out Microsoft (MS) has simplified this into a static site hosting service
  - [x] Explore hosting using Static site hosting
  - [x] Explore hosting github pages
  - [X] Configure DNS to point to hosted site
- [ ] Refine branching publishing workflow

## Todo list

- [x] Choose a blog engine
- [x] Learn more about blog engine
- [x] Find a theme that supports syntax highlighting
- [x] Hosting
  - [x] Explore hosting using Azure blob storage
    Turns out Microsoft (MS) has simplified this into a static site hosting service
  - [x] Explore hosting using Static site hosting
  - [x] Explore hosting github pages
  - [x] Configure DNS to point to hosted site
- [ ] Refine branching publishing workflow

## What I learned

- [Hugo](hugo)
- [git submodules](todo)
- [GitHub Pages](todo) When using Github pages with Hugo you need to match the repo name with the github pages url for them to work nicely together.
- [GitHub Actions](todo)
- [Azure static website service](todo) When using with Hugo you need to ensure the Hugo instance is in the root of your repo for the build action to work. In this case I chose not to build, just publish since I do this manually to control the publishing workflow. This is a remanence of playing with GitHub pages spike.

[^Podcasts]: [Podcasts](/posts/podcasts)

## If I where to do it again

[Hugo]: https://gohugo.io/