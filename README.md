# 3D models & browser tools

3D-printable models, editable CAD sources and browser configurators.

**[Open the tools website](https://oliveres.github.io/3D/)**

## Projects

| Project | Browser tool | Files and guide |
|---|---|---|
| DIN rail distribution stud — M6 / M8 / M10 | [Open configurator](https://oliveres.github.io/3D/din-rail/) | [Project folder](din-rail/) |
| DIN rail MEGA fuse holder — 2 × M8, 50.8 mm pitch | [Open configurator](https://oliveres.github.io/3D/mega-fuse/) | [Project folder](mega-fuse/) |
| Parametric rebar cap — 6 / 8 / 10 / 12 mm | [Open configurator](https://oliveres.github.io/3D/rebar-cap/) | [Project folder](rebar-cap/) |

The DIN rail project provides a common-potential connection point for cable lugs, for example in Victron Energy systems. The separate MEGA fuse project mounts a fuse vertically across the rail on a compact 27 mm carrier. Both packages include printable STL files, STEP models, an OpenSCAD source, a Bambu Studio project and printing instructions.

Both projects use extended retaining lips and a U spring with 1.40 mm walls. The spring is thickened outwards by 0.20 mm, and its release-notch shoulder is removed. The inner spring opening, retaining-tip gap, rail registration faces and fuse carrier remain unchanged by this spring update.

The rebar cap project includes a browser configurator, four STL variants and a self-contained OpenSCAD model. Defaults are an 8 mm bar, 3 mm base and 28 mm head. It is an **untested fit prototype, not impact-rated impalement protection**. See its [printing notes](rebar-cap/README.md) and [CC BY-NC 4.0 attribution](rebar-cap/LICENSE.txt).

## One Pages site, multiple tools

GitHub Pages publishes the root of the `main` branch. `.nojekyll` keeps the site as plain static files; no build system is needed.

Every tool has its own folder and `index.html`:

```text
index.html                  → https://oliveres.github.io/3D/
din-rail/index.html         → https://oliveres.github.io/3D/din-rail/
mega-fuse/index.html        → https://oliveres.github.io/3D/mega-fuse/
rebar-cap/index.html        → https://oliveres.github.io/3D/rebar-cap/
```

To add another tool:

1. Create a folder such as `your-next-tool/` with an `index.html` and any required assets.
2. Use relative links for local assets and downloads, so the tool works under `/3D/`.
3. Add a link or card to the root `index.html` and a row to the project table above.
4. Commit and push to `main`. GitHub Pages publishes the updated site automatically.

The new folder URL works once deployment finishes; the card on the home page is added manually. Files with other names also work at their full path, such as `your-next-tool/configurator.html`.

See [GitHub's Pages publishing documentation](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site).

## Credits and licensing

See each project's credits and any licence supplied with it. See the [distribution stud credits](din-rail/CREDITS.md) and [MEGA fuse holder credits](mega-fuse/CREDITS.md). No distribution licence for the two DIN rail projects has been selected yet; credits to reference designs are included. The rebar cap derivative is distributed under [CC BY-NC 4.0](rebar-cap/LICENSE.txt), with attribution to the original model by Niklas.
