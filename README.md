# pkgdown4gdpr

[pkgdown](https://pkgdown.r-lib.org) is a R package to generate a website with the documentation of an R package.

Unfortunately, pkgdown uses CDNs (such as cloudflare) and imports fonts directly from other resources in the internet.

Due to GDPR it's illegal in Germany to do this without prior consent by the user. (See German news at <https://www.golem.de/news/landgericht-muenchen-einbindung-von-google-fonts-ist-rechtswidrig-2202-162826.html>)

So I was looking for a simple solution to host all required files an my own server. The solution was quite simple: pkgdown4gdpr is a simple theme that overwrites the critical files of the original pkgdown theme and contains all resources that were loaded from CDNs by the original theme.

## Disclaimer

This package is work in progress. It works for me. There may be configurations or options which trigger downloading further files. So please double check on your own when using this package.
