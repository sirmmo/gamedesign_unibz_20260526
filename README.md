# Inside Board Game Publishing

Talk for the **Game Design course at the Free University of Bozen-Bolzano** — *Editorial Process, Post-2020 Economics, and Computer-Aided Games.*

**Marco Montanari** · 26 May 2026 · [BoardGameGeek @sirmmo](https://boardgamegeek.com/user/sirmmo)

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.20310092.svg)](https://doi.org/10.5281/zenodo.20310092)

📽 **Slides:** https://ingmmo.com/gamedesign_unibz_20260526/
📄 **PDF:** https://ingmmo.com/gamedesign_unibz_20260526/unibz_boardgame_publishing_talk.pdf

## Structure

The deck is built with [Marp](https://marp.app/). Source of truth is a single Markdown file plus a custom theme.

| File | Purpose |
|------|---------|
| `unibz_boardgame_publishing_talk.md` | The deck (slides + speaker notes) |
| `themes/editorial-press.css` | Custom Marp theme — "editorial trade press" aesthetic |
| `images/` | Box art, museum artifacts, and OpenFantasyMaps renders |
| `.github/workflows/pages.yml` | Builds the HTML/PDF and deploys to GitHub Pages on every push to `main` |

Four acts: a quick **field guide**, **the publisher's perspective**, **why everything costs double**, and **computer-aided games**.

## Build locally

No local Node toolchain required — use the official Marp Docker image:

```bash
docker run --rm -e MARP_USER=root:root -v "$PWD":/home/marp/app marpteam/marp-cli \
  unibz_boardgame_publishing_talk.md --theme themes/editorial-press.css \
  --html --allow-local-files -o index.html
```

Swap `--html` for `--pdf`, `--pptx`, or `--images png` for other formats. (`MARP_USER` is set so the container writes files as the host user.)

Or, with a local Node 18+ install:

```bash
npx --yes @marp-team/marp-cli@4 unibz_boardgame_publishing_talk.md \
  --theme themes/editorial-press.css --html -o index.html
```

## Citation

Archived on Zenodo: **[https://doi.org/10.5281/zenodo.20310092](https://doi.org/10.5281/zenodo.20310092)**
(GitHub's *"Cite this repository"* button reads [`CITATION.cff`](CITATION.cff).)

> Montanari, M. (2026). *Inside Board Game Publishing: Editorial Process, Post-2020 Economics, and Computer-Aided Games* [Slides]. Game Design course, Free University of Bozen-Bolzano, Bolzano, Italy. https://doi.org/10.5281/zenodo.20310092

```bibtex
@misc{montanari2026boardgame,
  author       = {Montanari, Marco},
  title        = {{Inside Board Game Publishing: Editorial Process,
                   Post-2020 Economics, and Computer-Aided Games}},
  year         = {2026},
  month        = may,
  howpublished = {Slides, Game Design course, Free University of Bozen-Bolzano},
  doi          = {10.5281/zenodo.20310092},
  url          = {https://doi.org/10.5281/zenodo.20310092}
}
```

## Image credits

Museum artifact photographs (Royal Game of Ur, Senet) are from Wikimedia Commons. Box-art and app images are used illustratively for educational commentary. OpenFantasyMaps renders are the author's own work.
