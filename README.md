# My porridge blog

This repo holds a [porridge](https://github.com/alexjj/porridge) blog: the
content is OPML, and GitHub Actions builds it into a static site on GitHub
Pages.

```
blog.opml          blog settings, plus one include per year
blog/2026.opml     this year's posts (new years are added automatically)
pages/about.opml   an About page; add more files here for more pages
images/            uploaded images
```

## Setup

1. Create a repo from this template.
2. In **Settings → Pages**, set **Source** to **GitHub Actions**.
3. Edit `blog.opml`: set `title`, `ownerName`, `porridge:timezone`, and
   `porridge:baseUrl` to your Pages address
   (`https://YOUR-USERNAME.github.io/YOUR-REPO/`).
4. Push. The **Build blog** workflow publishes the site.

After that, write with the porridge editor:

5. Create a [fine-grained token](https://github.com/settings/personal-access-tokens/new)
   for just this repository, with **Contents** and **Actions** set to read
   and write.
6. Open the editor, choose **Connect GitHub**, and enter this repository and
   the token.

**Save** commits without rebuilding the site; **Publish** commits and
rebuilds it.

The file format is documented in
[porridge's format.md](https://github.com/alexjj/porridge/blob/main/docs/format.md).
