# Hugo command reference

Run these commands from the project directory:

```powershell
cd C:\Users\Ellipse\Desktop\homepage
```

## Preview locally

Start the development server:

```powershell
hugo server
```

Include draft articles:

```powershell
hugo server -D
```

Open <http://localhost:1313/>. Hugo watches the project and refreshes the
browser whenever a file changes. Press `Ctrl+C` to stop the server.

## Create content

Create an English article:

```powershell
hugo new content posts/article-name.md
```

Create its Chinese translation:

```powershell
hugo new content posts/article-name.zh.md
```

In the article front matter, keep `draft: true` while working and change it
to `draft: false` when the article is ready to publish.

## Build the production site

```powershell
hugo --gc --minify
```

The generated homepage is written to `public/`. The `--gc` option clears
unused generated resources, while `--minify` reduces the output size.

Build drafts for local inspection only:

```powershell
hugo --gc --minify -D
```

## Useful checks

Show the installed Hugo version:

```powershell
hugo version
```

Show available commands:

```powershell
hugo help
```

Show the effective project configuration:

```powershell
hugo config
```

List all content known to Hugo:

```powershell
hugo list all
```

List drafts:

```powershell
hugo list drafts
```

## Publish through GitHub Pages

Commit and push changes:

```powershell
git add .
git commit -m "Update homepage"
git push
```

The workflow in `.github/workflows/hugo.yaml` builds and deploys the homepage automatically after each push to `main`. Check progress in the repository's **Actions** tab.

## PaperMod theme

Download the theme after cloning this repository:

```powershell
git submodule update --init --recursive
```

Update PaperMod to its latest upstream commit:

```powershell
git submodule update --remote --merge themes/PaperMod
```

After updating the theme, rebuild and inspect the site before committing the new submodule revision.
