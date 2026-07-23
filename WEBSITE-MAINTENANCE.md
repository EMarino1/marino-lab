# Marino Lab Website -- Maintenance Guide

This document describes the routine workflow for maintaining and
publishing the Marino Lab website.

## Standard publishing routine

1.  Preview:

``` powershell
quarto preview
```

2.  Render:

``` powershell
quarto render
```

3.  Commit:

``` powershell
git add .
git commit -m "Describe your changes"
```

4.  Push:

``` powershell
git push
```

If push fails:

``` powershell
git pull --rebase origin main
git push
```

## Custom domain

Keep a file named `CNAME` (no extension) in the project root containing:

    marinolab.unipa.it

Ensure `_quarto.yml` contains:

``` yaml
project:
  type: website
  output-dir: docs
  resources:
    - CNAME
```

Never delete `CNAME` or `docs/CNAME`.

## Branding

Homepage: `marinolab-logo.png`

Navbar & favicon: `marinolab-favicon.png`

## Backups

Periodically create a ZIP archive of the entire `marino-lab` project
folder.

## Useful commands

``` powershell
git status
quarto preview
quarto render
git add .
git commit -m "..."
git push
```

## Future improvements

-   Interactive collaboration map
-   Publication filtering
-   News page
-   Private member area
-   Research gallery
