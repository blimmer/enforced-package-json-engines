# Demo - Enforced `package.json` engine versions

This demo repository shows how to enforce the `engines` property in a `package.json` file. See also
[this StackOverflow answer](https://stackoverflow.com/a/68653111/808678).

In the [package.json](https://github.com/blimmer/enforced-package-json-engines/blob/main/package.json), we're requiring
Node >= 14. Because we have a local [.npmrc](https://github.com/blimmer/enforced-package-json-engines/blob/main/.npmrc)
file with `engines-strict=true`, running `npm install` with any Node version earlier than 14 will cause an error:

![](https://i.imgur.com/T3w1fC8.png)

You can see this configuration working by checking out the
[GitHub action](https://github.com/blimmer/enforced-package-json-engines/actions/workflows/npm-enforced-engines.yml)
results.

![](https://i.imgur.com/Pn6AvNr.png)
