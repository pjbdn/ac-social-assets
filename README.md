# Athlete Creditor — social image assets

Public image files for organic Instagram posts on
[@athletecreditor](https://www.instagram.com/athletecreditor/).

This repository is public for one technical reason: Meta's Instagram Content
Publishing API fetches a post's image **from its own servers** over public
HTTPS. A private repository, a signed URL or a local path will not work.

Everything here is artwork that is published to a public Instagram feed anyway.
Nothing operational lives in this repo — no captions, no schedule, no
credentials, no account data.

## Layout

```
posts/
  YYYY-MM/
    YYYY-MM-DD-<slug>.jpg
manifest.json
```

One file per post, named for the date it goes out and the slug used by the
publisher. Files are never overwritten — a changed creative gets a new post
slug — so a URL that has already been handed to Meta keeps resolving.

## manifest.json

Maps each post slug to its file and its raw URL, so the publisher never builds a
URL by string-joining.

```json
{
  "base_url": "https://raw.githubusercontent.com/pjbdn/ac-social-assets/main/",
  "posts": { "<slug>": { "path": "...", "url": "...", "width": 1080, "height": 1350 } }
}
```

## Sizes

Instagram feed: **1080×1350** (4:5, preferred — takes the most screen) or
**1080×1080** (1:1). Anything taller than 4:5 is cropped by Instagram, so tall
source art is letterboxed to 4:5 before it lands here.

## Where the rest lives

Captions, the schedule and the publisher are in a private repository, not here.

© Grand Teton Systems Inc. Athlete Creditor is not affiliated with or endorsed
by the NCAA.
