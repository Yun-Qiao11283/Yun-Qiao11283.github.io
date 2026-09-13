# Yun Qiao's academic website

This site uses the existing Academic Pages / Jekyll template.

## Editing

- `_pages/about.md`: biography, education, awards, and contact.
- `_pages/research.md`: TDA for Equity Markets only.
- `_pages/cv.md`: education, selected TDA research, awards, and coursework.
- `files/Yun_Qiao_CV.pdf`: original CV, unchanged, including the full research history.
- `images/yun-qiao.jpg`: original portrait.
- `_config.yml`: identity, metadata, and demo content exclusions.
- `_data/navigation.yml`: About, Research, and CV navigation.
- `assets/css/profile.css`: responsive additions to the original theme.

The text follows the supplied CV. The TDA pipeline is work in progress. Unverified details from the previous homepage (asset counts, library names, and thesis status) are omitted.

## Preview and publish

With Ruby and Bundler installed:

```sh
bundle install
bundle exec jekyll serve
```

Open http://localhost:4000. Use `bundle exec jekyll build` to build without serving.

After review, commit and push to the repository's publishing branch. GitHub Pages must be configured for that branch and its root folder. The expected public URL is https://Yun-Qiao11283.github.io/.

Demo pages and collections are excluded from the generated site; template sources and license remain available for maintenance and attribution.
