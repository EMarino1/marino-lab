# Marino Lab Website Maintenance Manual

This manual explains how to maintain and publish the Marino Lab website.

## Website stack

-   Quarto
-   Git
-   GitHub Pages
-   Custom domain: https://marinolab.unipa.it

## Standard workflow

1.  Edit `.qmd`, `.css`, or image files.
2.  Preview:

``` powershell
quarto preview
```

3.  Stop preview (Ctrl+C)

4.  Render:

``` powershell
quarto render
```

5.  Commit:

``` powershell
git add .
git commit -m "Describe your changes"
```

6.  Publish:

``` powershell
git push
```

## Important files

-   `_quarto.yml` --- configuration
-   `styles.css` --- global styling
-   `collaborators.css` --- collaborator styling
-   `CNAME` --- custom domain (never delete)
-   `images/logo/marinolab-logo.png`
-   `images/logo/marinolab-favicon.png`

Never edit files inside `docs/`; they are generated automatically.

## Git problems

If push is rejected:

``` powershell
git pull --rebase origin main
git push
```

Never use `git push --force`.

## Mobile testing

Open Chrome:

-   F12
-   Ctrl+Shift+M
-   Select Pixel 7
-   Refresh

## Backups

Zip the entire `marino-lab` folder after major updates.

## Never do

-   Delete `CNAME`
-   Delete `docs/CNAME`
-   Rename `docs`
-   Remove the custom domain
-   Edit generated HTML in `docs`

## Checklist

-   Edit
-   Preview
-   Render
-   Commit
-   Push
-   Verify https://marinolab.unipa.it
