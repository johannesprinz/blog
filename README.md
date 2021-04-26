# Spike 

To figure out how to create a static site using hugo and deploy to azure blob storage using github actions. Goal is to have a profile / blog site that uses mark down and can easily publish to a no-low cost hosting solution.

I've been meaning todo this for a long time and I have had enough syncronisties telling me to get on with it and just do. 

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
