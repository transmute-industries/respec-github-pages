# ReSpec GitHub Pages

This repo is a [GitHub template](https://github.blog/2019-06-06-generate-new-repositories-with-repository-templates/) for
creating GitHub repositories containing [ReSpec specification](https://respec.org) documents.
Repos created from this template use off-the-shelf components for previewing (before you commit!), generating and
publishing your spec. Notably it uses the [ReSpec JS library](https://www.npmjs.com/package/respec) for generating the
specification document from source, and [GitHub Pages](https://pages.github.com/) for previewing and publishing your spec using an
implicit build/deploy process. By using off-the-shelf components that are built, maintained and supported by others,
you can focus on your spec work and not on the tools/platform for formatting and publishing your specification.

## Creating a new Spec Repository

If you are reading this document on the [respec-github-pages repo](https://github.com/transmute-industries/respec-github-pages) on github.com, click the `Use This Template` button above the file list and follow the steps to create a new repo. There
are other ways (command line, etc.) to create a repo from a template that are described in [GitHub documentation](https://docs.github.com/en/github/creating-cloning-and-archiving-repositories/creating-a-repository-from-a-template). See the benefit of
using off-the-shelf things?  Documentation is maintained by others!

Your new spec is in the `docs` folder of your new repo, the [index.md file](docs/index.md). You can now start editing the spec.  If you are new to ReSpec, check out the [About ReSepc](#about-respec) section of this document for getting started links.

Once you have created your new repo, you probably want to clone (or fork and clone) the repo so that you can edit it locally. Management of the spec can use whatever GitHub workflows work
for you and your co-editors.

## Previewing your Spec Locally

The new repo uses a standard [GitHub Pages](https://pages.github.com/) process for editing/previewing/committing/PRing. To preview your to-be-published
spec before committing, you can run a local instance of Jekyll, the static website generator that powers GitHub pages. To
run it locally, following the GitHub instructions [here](https://docs.github.com/en/github/working-with-github-pages/testing-your-github-pages-site-locally-with-jekyll). The `<tl;dr>` of those instructions are:

- Install `Ruby` and `bundle` on the device on which you are editing the spec.
  - If you have to install those, you should definitely read the [GitHub instructions](https://docs.github.com/en/github/working-with-github-pages/testing-your-github-pages-site-locally-with-jekyll).
- The first time you preview the site run `bundle install` from the `./docs` folder
  - Per the GitHub instructions linked above, you may want to run this from time to time to get the latest versions of the underlying code generator
- Whenever you want to preview the site run `bundle exec jekyll serve --incremental`
  - The `--incremental` option regenerates the spec on every save so you can make changes to the spec and immediately see what you did in a browser. You do have to hit `refresh` in the browser to see the changes.
  - Run `bundle exec jekyll serve --help` for other options that might be useful.
- Open your browser to http://localhost:4000 and voila! Your spec!

There are lots of variations on the instructions above, so use the GitHub guidance to figure out what you need to do.

## Publishing your Spec

Once you've iterated on your spec a bit, made some changes, commits and merged some PRs, you will want to share your
spec with the world. To do that, follow the GitHub Pages instructions for [configuring the source](https://docs.github.com/en/free-pro-team@latest/github/working-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site) for the
published GitHub Pages website. Chances are you want to use the `Main` (or `Master`) branch and you will want to use the `./docs` folder. Don't choose a theme as you will be using ReSpec style. A few moments later, your spec will be published at `https://<github account>.github.io/<repo name>`. w00t!

By using GitHub Pages to publish your site, updates to the spec are published automatically. Whenever the source branch/folder of your repo is
updated (for example, a PR is merged), GitHub pages automatically re-generates and publishes the spec.

Of course, if a merge messes up the document too much (for example, deletes the `./docs` folder), you may have to troubleshoot things. Fortunately,
there is a [troubleshooting GitHub Pages](https://docs.github.com/en/free-pro-team@latest/github/working-with-github-pages/troubleshooting-jekyll-build-errors-for-github-pages-sites)
document about that, part of the [overall GitHub Pages](https://docs.github.com/en/free-pro-team@latest/github/working-with-github-pages) documentation.

Although there are lots of docs on Github Pages, you won't need to do a lot because of your constrained use case (you are writing a ReSpec spec) and because this template sets up your spec.

### Configuring a custom domain name

Chances are, you will want to have a nice URL for your spec, something like `https://spec.example.com`. GitHub Pages has
instructions for how to do that [here](https://docs.github.com/en/github/working-with-github-pages/configuring-a-custom-domain-for-your-github-pages-site).

## FAQ - What you can do in the spec

### Markdown

Yes, you can use markdown in your spec document. See the example in this repo and use the 
guidance about ReSpec JS (below) for how to use markdown.

### Serve JSON files with nice URLs

GitHub will automatically serve JSON file with the correct `content-type` if you name them with a `.json` extension.

This means that `https://example.com/ns/spec/v1` will automatically be json if you create a file:

`./docs/ns/spec/v1/index.json`

For example, in the sample spec, see [./docs/v1](./docs/v1).

### Versioning Specs

You can create versions of your spec by creating a folder for the version and copying the spec files into that folder. For example, see [./docs/v0.1.2](./docs/v0.1.2) in this repo. That example version is visible at `<specURL>/v0.1.2`.

## About ReSpec

From the [ReSpec Documentation](https://respec.org) site:

> ReSpec is a JS library that makes it easier to write technical specifications, or documents that tend to be technical in nature in general. It was originally designed for the purpose of writing W3C specifications, but has since grown to be able to support other outputs as well.

If you are new to ReSpec, checkout the [ReSpec Editor's Guide](https://github.com/w3c/respec/wiki/ReSpec-Editor's-Guide) for both getting started and advanced material.  The ReSpec GitHub repo is [here](https://github.com/w3c/respec).

### Why to use ReSpec

You should use ReSpec if you are serious about writing standards. There are other tools out there, but ReSpec is the best.

ReSpec is well supported, so if you need help, you can get it.

See [respec.org/docs](https://respec.org/docs/).
