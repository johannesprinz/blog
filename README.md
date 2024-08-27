# My personal blog

## Getting started

You will need [Docker](#todo), [Visual Studio Code](https://code.visualstudio.com/) and use the [Remote development container extension](https://code.visualstudio.com/docs/remote/containers-tutorial). Once this has re-opened in the remote container you are setup and ready to go.
After the initial clone sun the following to spin up the project:

```bash
git submodule update --init --recursive
cd src
hugo server -D
```

## Hosting

Blog is hosted at www.johannesprinz.com via [Azure static page](https://docs.microsoft.com/en-nz/azure/static-web-apps/). Following the Hugo example I could not get the build step to work. So I've decided to skip the build and control the publishing step via manual publishing `> hugo` and is also published to a separate repo https://github.com/johannesprinz/johannesprinz.github.io which publishes to [Github pages](https://docs.github.com/en/pages). For this to work I needed to name my published repo by the same name as the github page url linked to my account. At least for deploying a Hugo site. Followed this video [Creating a Blog with Hugo and Github in 10 minutes](https://www.youtube.com/watch?v=LIFvgrRxdt4) to get this to work.

## Guides followed so far

- [Hugo quick start](https://gohugo.io/getting-started/quick-start/)
- [Set up a GitHub Actions workflow to deploy your static website in Azure Storage](https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blobs-static-site-github-actions)

## How we got here

```zsh
mkdir blog
cd blog
git init
code .
# ctrl + p, >, create development container (found a hugo one)
```

### Once re-opened in container

```zsh
hugo new site quickstart
cd quickstart
git submodule add https://github.com/theNewDynamic/gohugo-theme-ananke.git themes/ananke 
# Then any other theme you are after, at this stage I tried a few to see which support syntax highlighting
echo theme = \"ananke\" >> config.toml
hugo new posts/my-first-post.md
hugo server -D
```

## Struggles

- Learning Hugo
- Learning how to work with git submodules
- Deployment
  - Azure blob storage
  - Azure static sites
  - GitHub pages
    - Wont play nice with base urls containing sub paths https://example.com
    > Start building sites … 
Total in 126 ms
Error: Error building site: TOCSS: failed to transform "css/main.scss" (text/x-scss). Check your Hugo installation; you need the extended version to build SCSS/SASS.
  - make sure the publishing page is your base uri eg  johannesprinz.github.io