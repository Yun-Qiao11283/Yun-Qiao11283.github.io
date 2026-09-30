# Yun Qiao's academic website

This site uses the existing Academic Pages / Jekyll template.

## Editing

- `_pages/about.md`: biography, education, awards, and contact.
- `_pages/research.md`: research interests and a concise project list.
- `_data/research.yml`: project titles, dates, supervisors, summaries, and links. Append an entry here to add a future research project.
- `_pages/cv.md`: education, all research experiences, manuscript status, awards, coursework, and skills.
- `files/Yun_Qiao_CV.pdf`: latest supplied CV (updated September 30, 2026), copied without editing.
- `images/yun-qiao.jpg`: original portrait.
- `_config.yml`: identity, metadata, and demo content exclusions.
- `_data/navigation.yml`: About, Research, and CV navigation.
- `assets/css/profile.css`: responsive additions to the original theme.

Website content follows the CV supplied September 30, 2026. All three research experiences and the manuscript under review are included. The PDF lists six Dean’s List semesters while saying five; web pages list the semesters without a count. The original PDF is preserved as supplied. TDA code and poster links remain available.

## Preview and publish

With Ruby and Bundler installed:

```sh
bundle install
bundle exec jekyll serve
```

Open http://localhost:4000. Use `bundle exec jekyll build` to build without serving.

After review, commit and push to the repository's publishing branch. GitHub Pages must be configured for that branch and its root folder. The expected public URL is https://Yun-Qiao11283.github.io/.

Demo pages and collections are excluded from the generated site; template sources and license remain available for maintenance and attribution.
