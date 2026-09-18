# 3D models & browser tools

3D-printable models, editable CAD sources and browser configurators.

**[Open the tools website](https://oliveres.github.io/3D/)**

## Projects

| Project | Browser tool | Files and guide |
|---|---|---|
| DIN rail distribution stud — M6 / M8 / M10 | [Open configurator](https://oliveres.github.io/3D/din-rail/) | [Project folder](din-rail/) |
| DIN rail MEGA fuse holder — 2 × M8, 50.8 mm pitch | [Open configurator](https://oliveres.github.io/3D/mega-fuse/) | [Project folder](mega-fuse/) |

The DIN rail project provides a common-potential connection point for cable lugs, for example in Victron Energy systems. The separate MEGA fuse project mounts a fuse vertically across the rail on a compact 27 mm carrier. Both packages include printable STL files, STEP models, an OpenSCAD source, a Bambu Studio project and printing instructions.

Both projects use extended retaining lips: each tip reaches 0.50 mm farther inwards, while the rail registration faces and fuse carrier remain unchanged.

## One Pages site, multiple tools

GitHub Pages publishes the root of the `main` branch. `.nojekyll` keeps the site as plain static files; no build system is needed.

Every tool has its own folder and `index.html`:

```text
index.html                  → https://oliveres.github.io/3D/
din-rail/index.html         → https://oliveres.github.io/3D/din-rail/
mega-fuse/index.html        → https://oliveres.github.io/3D/mega-fuse/
```

To add another tool:

1. Create a folder such as `your-next-tool/` with an `index.html` and any required assets.
2. Use relative links for local assets and downloads, so the tool works under `/3D/`.
3. Add a link or card to the root `index.html` and a row to the project table above.
4. Commit and push to `main`. GitHub Pages publishes the updated site automatically.

The new folder URL works once deployment finishes; the card on the home page is added manually. Files with other names also work at their full path, such as `your-next-tool/configurator.html`.

See [GitHub's Pages publishing documentation](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site).

## Credits and licensing

See each project's credits and any licence supplied with it. See the [distribution stud credits](din-rail/CREDITS.md) and [MEGA fuse holder credits](mega-fuse/CREDITS.md). No distribution licence for these new projects has been selected yet; credits to reference designs are included.
