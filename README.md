# Edit in Infusion - review site

A sandbox site built with **wend**, which exists only so that the "Edit in Infusion" browser extension can be tried
out - by the Chrome Web Store's reviewers, among others - without access to any real site. Every edit made through the
extension is committed to this repository, and the site is rebuilt from it.

It is built with the npm packages `@fluid-project/wend` and its theme `@fluid-project/wend-theme-beautiful`, released from `packages/` of
[Infusion 6's repository](https://github.com/fluid-project/infusion-6). The README of
[amb26/ponder](https://github.com/amb26/ponder) describes the layout of a wend site.

## Building

```
npm install
npm run build
```

This writes the site to `docs/`, which GitHub Pages publishes. `.github/workflows/build-site.yml` rebuilds it whenever
its sources change on `main` - the branch which `wend/editing.json` names, to which the extension commits.

## Access for review

Reviewers are given a fine-grained personal access token with *Contents: read and write* on this repository alone,
entered in the extension's options under *Use a personal access token instead*. It is revoked once the review is done.
