# Field Notes

A Hugo blog built with the PaperMod theme and inspired by the clean,
long-form reading experience of Lil'Log.

## Run locally

```powershell
hugo server -D
```

Then open <http://localhost:1313/>.

## Personalize

1. Replace the title, author, description, `baseURL`, email, and social links
   in `hugo.yaml`.
2. Replace `content/about.md` with your biography.
3. Remove the sample files in `content/posts/` and add a post with:

   ```powershell
   hugo new content posts/my-first-post.md
   ```

4. Change colors and typography in `assets/css/extended/custom.css`.

## Build

```powershell
hugo --minify
```

The deployable site is generated in `public/`.
