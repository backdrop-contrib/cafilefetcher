# CAFile Fetcher

**In an ideal world, this module wouldn't exist.**

You only need it if the server your site is running on doesn't get updated
regularly, and the ca-certificate package on that server is outdated.

The typical symtom for that are problems when fetching update information or
downloading modules via UI.

You'll find messages like that in your dblog (/admin/reports/dblog):

```
HTTP request to https://updates.backdropcms.org/release-history/...
failed with error: Error opening socket ssl://updates.backdropcms.org:443.
```

On the "Available updates" page you may also see a message like "Failed to
get available update data for XX projects." And the module status icons are
just grey with a question mark.

If that's the case on your site, install this module and things should be
fixed.

However, the fact that you ran into this problem indicates that you should
contact your hosting provider and inform them of the problem with the
outdated certificate authority package (ca-certificates) - and that they
should update it as soon as possible.

## Installation

Install this module using the
 [official Backdrop CMS instructions](https://docs.backdropcms.org/documentation/extend-with-modules).

When the module gets enabled, it automatically downloads a recent version of
the certificate authority bundle to use for certificate verification.
After that the file gets updated via cron runs, whenever a newer version is
available. So if you have set up cron properly, you never have to care about
that anymore. But you can also download it manually on the module's admin page.

## Issues

Bugs and feature requests should be reported in the
 [Issue Queue](https://github.com/backdrop-contrib/cafilefetcher/issues).

## Current maintainers

- [Indigoxela](https://github.com/indigoxela)

## Credits

- The Certificate Authority file gets fetched from https://curl.se/docs/caextract.html
- It's the [Mozilla CA certificate](https://wiki.mozilla.org/CA) store in PEM format

Both are licensed under Mozilla source file: MPL 2.0

## License

This project is GPL v2 software. See the LICENSE.txt file in this directory for complete text.
