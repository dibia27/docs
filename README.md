# Website

This website is built using [Docusaurus 2](https://docusaurus.io/), a modern static website generator.

### JLD Notes

Currently deploys to a [tenant cluster](https://3439bd42-d622-41f7-8c82-85b142d2a30d.lb.civo.com/).

Uses ArgoCD under the hood to pull from Git and NPM is always really slow to build, so you may have to give it 5 mins after committing before seeing your changes on the above link.


### Installation

You will need Yarn installed, which in turn requires npm and Node. On a Mac using homebrew, you can run `brew install node`.

Assuming you have npm set up, you can run:

```console
npm install --global yarn
```

Then run

```console
$ yarn
```

### Local Development

```
$ yarn start
```

This command starts a local development server and opens up a browser window. Most changes are reflected live without having to restart the server.

### Build

```
$ yarn build
```

This command generates static content into the `build` directory and can be served using any static contents hosting service.

### Deployment

Using SSH:

```
$ USE_SSH=true yarn deploy
```

Not using SSH:

```
$ GIT_USER=<Your GitHub username> yarn deploy
```

If you are using GitHub pages for hosting, this command is a convenient way to build the website and push to the `gh-pages` branch.
