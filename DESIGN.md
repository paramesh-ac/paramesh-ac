# Profile artwork source

The profile uses self-contained SVG editorial panels, project cards, and interactive GitHub Actions workflows.

## Files

- `scripts/build_editorial.py`: Python script generating responsive SVG panels for hero, about, stack, projects, dashboard, certifications, and connect sections using Barlow Condensed font glyphs and CSS keyframe animations.
- `scripts/build_cards.py`: standard-library Python generator for project, achievement, hiring, toolkit, and footer SVGs. Run `python scripts/build_cards.py`.
- `scripts/update_profile.py`: GitHub Actions automation script that fetches live public repository counts, stars, and follower statistics from the GitHub API and renders them dynamically into `assets/stats.svg` and `assets/editorial-dashboard.svg`.

## GitHub delivery

All README artwork and the supplied résumé PDF are hosted in this repository:
- Résumé: `assets/Paramesh-Resume.pdf`
- Avatar: `assets/profile-avatar.jpg`
- Panels & Cards: `assets/editorial-*.svg`

The `Update profile` GitHub Actions workflow refreshes the contribution snake, public statistics, and profile links daily. Keep the `PROFILE-STATS` and `PROFILE-LINKS` comment markers intact when editing the README.
