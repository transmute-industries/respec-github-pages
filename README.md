### Respec GitHub Pages

#### How do I make a new specification?

Follow the default github instructions for [creating-a-repository-from-a-template](https://docs.github.com/en/github/creating-cloning-and-archiving-repositories/creating-a-repository-from-a-template).

#### Do I need to build anything?

No! GitHub will automatically handle everything for you.

#### What if I need to serve JSON files with nice URLs?

GitHub will automtically serve them with the correct `content-type` if you name them with a `.json` extension.

This means that `https://example.com/ns/spec/v1` will automatically be json if you create a file:

`./docs/ns/spec/v1/index.json`

See [./docs/v1](./docs/v1) for an example.

#### What about versioning?

You can create versions of your spec, and their URLs will be preserved.

See [./docs/v0.1.2](./docs/v0.1.2) for an example.

#### What is ReSpec?

> ReSpec is a JS library that makes it easier to write technical specifications, or documents that tend to be technical in nature in general. It was originally designed for the purpose of writing W3C specifications, but has since grown to be able to support other outputs as well.

- [w3c/respec](https://github.com/w3c/respec)

#### Why should I use ReSpec?

You should use ReSpec if you are serious about writing standards.

There are other tools out there, but ReSpec is the best.

ReSpec is also well supported, so if you need help, you can get it.

See [respec.org/docs](https://respec.org/docs/).

#### How do I configure a custom domain name?

If you want your spec to be hosted at a nice url, like:

https://spec.example.com

Please review the default github instructions for [configuring-a-custom-domain-for-your-github-pages-site](https://docs.github.com/en/github/working-with-github-pages/configuring-a-custom-domain-for-your-github-pages-site).

#### How do I edit / preview locally?

Please review the default github instructions for [testing-your-github-pages-site-locally-with-jekyll](https://docs.github.com/en/github/working-with-github-pages/testing-your-github-pages-site-locally-with-jekyll)
