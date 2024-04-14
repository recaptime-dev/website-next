# @recaptime-dev/website

[![Cloudflare Pages](https://github.com/recaptime-dev/website-next/actions/workflows/cf-pages.yml/badge.svg)](https://github.com/recaptime-dev/website-next/actions/workflows/cf-pages.yml)

Jekyll-based website for Recap Time Squad, with the [JTD theme]. If you're looking for
the old codebase, [go to `arhcived/old-theme` branch][old-code].

## Development

See [`CONTRIBUTING.md`](./CONTRIBUTING.md) file for full details. In nutshell:

1. Install dependencies: `bundle install`
2. Run localdev: `bundle exec jekyll serve --watch --livereload --drafts --unpublished`
3. Edit as needed (Markdown files are at `docs` directory with `permnalink` magic)
4. Signoff your commits and push to your personal fork.
5. Send a merge request or email patch.

[JTD theme]: https://just-the-docs.github.io/just-the-docs/
[old-code]: https://github.com/recaptime-dev/website-next/commits/archived/old-theme
