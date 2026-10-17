# onyxterm.github.io

This repository is the **GitHub Pages site** for the `onyxterminal` organisation. It serves
https://onyxterminal.github.io/

**It contains no site code.** The site source lives in
[`onyxterminal/onyxterm-web`](https://github.com/onyxterminal/onyxterm-web).

To change the site, open a pull request against `onyxterminal/onyxterm-web` on `main`. This
repository's workflow checks that repo out, builds it with `BASE_PATH=/`, and publishes the
result to the apex.

## Why a separate repository

GitHub serves an organisation apex (`onyxterminal.github.io`) only from a repository named
`onyxterm.github.io`. A project site such as `onyxterm-web` is published to
`onyxterminal.github.io/onyxterm-web/` instead and cannot claim the root.

## The project site

`onyxterm-web` also publishes itself to https://onyxterminal.github.io/onyxterm-web/ on every
push to its `main`. Both are live; the apex is canonical.

## A custom domain

A `CNAME` file is only relevant when pointing this site at a domain you own. To use one:

1. Add a `CNAME` file at the repository root containing the hostname, e.g. `onyxterm.com`.
2. In the repo settings, set Pages → Custom domain.
3. At the DNS provider, add an `A` record for `onyxterm.com` pointing at GitHub Pages IPs, and
   a `TXT` record for `_github-challenge-onyxterm.com` with the verification value GitHub shows.

Until that is set up, the apex URL is the canonical one.