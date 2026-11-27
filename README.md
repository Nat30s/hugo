# News site (Hugo + Blank Magazine theme)

## Add a post
Create `content/posts/anything.md`:

    ---
    title: Post title
    description: One-line summary
    pubDate: 2026-09-29
    author: Your Name
    category: Transport
    tags: [metro, news]
    cover: https://example.com/image.jpg   # optional, full https link
    toc: false        # true = show a collapsible Contents box
    updates: true     # false = hide the Updates timeline box
    ---
    Intro paragraph (shown above the Updates box).

    ## 29 Sep 2026 · Headline of this update
    Text...

    ## 20 Sep 2026 · Older update
    Text...

Each `## date · headline` becomes an entry in the Updates box (newest first, as written).
A post without dated headings simply has no Updates box.
The `category` value creates an archive page automatically: `/category/<name>/` (index at `/category/`). Add `featured: true` to pin a post on the home page.

## Optional post switches (frontmatter)
- `toc: true` shows a collapsible **Contents** box listing `##` and `###` headings. Default: hidden.
- `updates: false` hides the **Updates** timeline box. Default: shown (only appears if the post has dated headings).
- The two are independent; on a dated post `toc: true` shows both boxes.
- `cover:` takes a full `https://` image link; it appears on the post, home page and lists.

## Settings
Edit `hugo.toml`: `title`, `author` (footer) and `description`.
`baseURL` is overridden automatically on GitHub Pages.

## Notes
- `themes/blank-magazine/` is a patched copy of github.com/codesign2020/blank-magazine (English text, sub-path fixes).
- Your post layout lives in `layouts/_default/single.html`.
- Hugo version is pinned in `.github/workflows/hugo.yaml`.
