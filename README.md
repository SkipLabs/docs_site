# Skip Docs Site

This repo contains the generated static documentation site files, and is the source that feeds the Vercel hosted site. See the [docs-site](https://vercel.com/skiplabs-website/docs-site) project.

These files are generated and should not be modified directly, but instead should be regenerated after modifying the sources in skip/www, or the doc strings in the ts sources for API docs. See skip/www/README.md for instructions on modifying the documentation sources.

The workflow for publishing documentation updates is:
```
$ cd /path/to/skip/repo/root

# generate docs site static files
$ make docs-build

# run the static docs site locally, to test
$ make docs-serve

# mirror the generated files in the docs site repo
$ make DOCS_SITE_DIR=/path/to/docs_site/repo/root docs-sync

# commit new version
$ cd /path/to/docs_site/repo/root
$ git add -A
$ git commit ...
```
