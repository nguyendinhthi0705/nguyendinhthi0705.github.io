# Setup
1. Use template academicpages/academicpages.github.io → new repo `nguyendinhthi0705.github.io` (Public).
2. Delete sample files in `_talks/ _teaching/ _portfolio/ _publications/ _posts/`.
3. Copy these files in. For `_config.yml`, edit the matching fields in the existing file (don't replace the whole file).
4. Add images: `images/profile.jpg`, `images/headshot-portrait.jpg`, `images/headshot-landscape.jpg`, `images/talks/...`.
5. Settings → Pages → Deploy from branch (master), /root.
6. Search "TODO" and fill in: email, LinkedIn, dates, cert list.
7. Talk map: generated automatically by the GitHub Action (`.github/workflows/scrape_talks.yml`, which runs `talkmap.ipynb`) when you add or edit talks.
