# My personal blog

## Hosting

Plan is to host at johannesprinz.com. Options at this stage are via:

- [Github pages](https://docs.github.com/en/pages)
  - For this to work I needed to name my repo by the same name as the github page url linked to my account. At least for deploying a Hugo site. Followed this video [Creating a Blog with Hugo and Github in 10 minutes](https://www.youtube.com/watch?v=LIFvgrRxdt4) to get this to work.
- [Azure static page](https://docs.microsoft.com/en-nz/azure/static-web-apps/)
  Following the Hugo example I could not get the build step to work. So I've decided to skip the build and control the publishing step via a seperat repo.

Having looked at the following blog options:

- [Ghost](https://ghost.org/)
- [Wordpress](https://wordpress.com/)
- [Hugo](https://gohugo.io/)

I have settled with [Hugo](https://gohugo.io/), as I am a fan of markodwn for authoring.


I've been meaning todo this for a long time and I have ls
had enough syncronisties telling me to get on with it and just do. 

- TODO Try to add refs that pushed me to this.

## Guides folowed so far

- [Hugo quick start](https://gohugo.io/getting-started/quick-start/)
- [Set up a GitHub Actions workflow to deploy your static website in Azure Storage](https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blobs-static-site-github-actions)

## How we got here

```zsh
mkdir hugoGettingStarted
cd hugoGettingStarted
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