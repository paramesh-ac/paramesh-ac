# Profile design

The editorial layout uses original SVG code and artwork, inspired by modern developer portfolios with an editorial dark blue visual direction. It uses Paramesh's own photo, projects, experience, education, and public GitHub metrics.

## Regenerate the design

Run the following from this repository. No external dependencies are required.

```sh
python scripts/build_editorial.py
python scripts/build_cards.py
GITHUB_REPOSITORY_OWNER=paramesh-ac python scripts/update_profile.py
```

The third command fetches the current public metrics from GitHub. The scheduled workflow also refreshes both builder dashboards and the README metrics.

Edit the text and layout in `scripts/build_editorial.py`. All editorial panels have a separate mobile layout. Their CSS animations stop when the viewer requests reduced motion, and their content remains visible without animation. GitHub's Markdown supports animated images; it does not run JavaScript or background audio. Clickable project and contact links are placed in the README around or below the images because SVG images cannot contain interactive controls on GitHub.

## Sources

- `assets/profile-avatar.jpg` is the public photo from Paramesh's GitHub avatar (`@paramesh-ac`).
- Display lettering is Barlow Condensed Bold by Jeremy Tribby, converted to SVG glyph outlines. Source: https://github.com/google/fonts/tree/main/ofl/barlowcondensed
- The font is distributed under the SIL Open Font License 1.1. Its copyright and license are retained in `assets/editorial-source/OFL-BarlowCondensed.txt`.
- Résumé PDF: `assets/Paramesh-Resume.pdf`.
