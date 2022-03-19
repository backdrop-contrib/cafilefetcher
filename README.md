# CAFile Fetcher

**In an ideal world, this module wouldn't exists.**

You only need it if the server your site is running on doesn't get updated
regularly, and the ca-certificate package on that server is outdated.

The typical symtom for that are problems when fetching update information or
downloading modules via UI.

You'll find messages like that in your dblog (/admin/reports/dblog):

```
HTTP request to https://updates.backdropcms.org/release-history/...
failed with error: Error opening socket ssl://updates.backdropcms.org:443.
```

If that's the case on your site, install this module and things should be
fixed.

However, the fact that you ran into this problem indicates that you should
contact your hosting provider and inform them of the problem with the
outdated certificate authority package (ca-certificates) - and that they
should update it as soon as possible.

## Installation

Install this module using the
 [official Backdrop CMS instructions](https://docs.backdropcms.org/documentation/extend-with-modules).

## Issues

Bugs and feature requests should be reported in the
 [Issue Queue](https://github.com/backdrop-contrib/cafilefetcher/issues).

## Current maintainers

* [Indigoxela](https://github.com/indigoxela)

## Credits

- The Certificate Authority file gets fetched from https://curl.se/docs/caextract.html
- It's the [Mozilla CA certificate](https://wiki.mozilla.org/CA) store in PEM format

Both are licensed under Mozilla source file: MPL 2.0

## License

This project is GPL v2 software. See the LICENSE.txt file in this directory for complete text.
