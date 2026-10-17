# Parametric rebar cap — fit prototype v5

A modification of the supplied 8 mm STL, with five flexible slotted segments, a hollow internal guide and an independently adjustable head and closed base. **This prototype has not been impact tested and must not be relied on to prevent impalement if someone falls onto rebar.** Geometry and slicer checks do not demonstrate protective performance.

[Open the live configurator](https://oliveres.github.io/3D/rebar-cap/) · [Download the complete offline package](Rebar_Cap_Parametric_v5.zip)

## Three parameters

| Parameter | Choices / range | Default |
| --- | --- | --- |
| Nominal rebar diameter | 6, 8, 10 or 12 mm | 8 mm |
| Closed base thickness | 2–8 mm | 3 mm |
| Head diameter | 25–40 mm | 28 mm |

Open `index.html` in a browser. It works offline and generates STL locally. The `Section` view reveals the cavity and closed base; `Installed` shows the cap upside down relative to its print orientation. Every STL export is the complete model, oriented with the broad closed face on the print bed.

The `STL` folder contains four nominal bar sizes with a 28 mm head and a 3 mm base. `Rebar_Cap_Parametric.scad` is a self-contained OpenSCAD model with the same three parameters and no external dependencies.

## Revised outer neck

The local reinforcement used in versions 2 and 3 left visible changes in curvature. Version 4 replaces this outer neck with a surface of revolution defined by one continuous radial profile. Its slope and curvature match the adjacent reference cones at the profile endpoints (C2 continuity); nonnegative profile curvature prevents the previous local bump. The exported outer skin is sampled from this profile, with finer angular facets. This changes the actual STL, independently of the browser's smooth shading.

The nominal inner gripping surface, narrow slot outlines and guide dimensions are retained. For the default 8 mm variant, the slot opening at the original waist remains 1.50 mm inside and approximately 1.66 mm outside, with rounded ends. The new outer curve redistributes wall thickness: it is approximately 0.5 mm fuller radially at the original waist, rather than carrying a small localized reinforcement. In version 4, total solid model volume increased by about 1.7% relative to v3; version 5 removes material at the head bevel. Insertion force and durability need a new physical test.

## Guide and head geometry

Version 1 fitted the user's bar, but its wide head cavity allowed the bar tip to rock and the spring waist fractured between layers. Version 2 added a hollow guide, and the user reported a substantial improvement. This guide is retained in version 5: **13 mm high from the inside floor**, **internal diameter = nominal bar + 2 mm**, **2 mm wall**. For an 8 mm bar it is Ø10 mm inside and Ø14 mm outside. Space around the guide remains empty.

The head has a broad flat printing face, a 3 × 3 mm edge bevel at 45°, and a hollow tapered transition. Version 5 enlarges the bevel from 1 to 3 mm. The flat face diameter is `head_diameter − 6` mm. For base thicknesses below 3 mm, the outer shoulder is raised to 3 mm to accommodate the complete bevel; the central floor retains the selected thickness. Changing head diameter does not resize the neck. Changing base thickness raises the neck and guide without stretching them. Selecting another nominal bar size offsets neck surfaces radially by half the diameter difference; it does not guarantee the same insertion force across sizes.

Default dimensions are approximately Ø28 × 42.95 mm, with a flat bed-contact face of approximately Ø22 mm. Overall height is `39.9474 + base_thickness` mm. Polygonal approximations introduce small differences in bounding-box measurements.

## Printing and fit

Print with the broad closed face on the bed. Check one cap on the actual bar first. The nominal bar diameter does not specify rib height or the width of a hammered end. An enlarged end must fit through the continuous guide ring. Stop if it cracks or requires excessive force.

The thickness parameter defines **geometric material space**, not slicer infill. To make the default 3 mm base solid at 0.20 mm layers, use at least 15 bottom solid layers with a 0.20 mm first layer, or a height-range modifier that makes the full first 3 mm solid. Adjust for other thicknesses and layer settings. Sparse infill would not produce the full solid base thickness specified in CAD.

Slicing checks use a Bambu Lab X1 Carbon, 0.4 mm nozzle, 0.20 mm layers, six walls, supports off, and sufficient bottom solid layers. Generic PLA is used only as a reproducible slicing profile, not a qualification of that material for impact protection. Version 5 has not yet been physically printed or fit-tested.

## Validation

Thirty-six combinations were checked for closed, connected, consistently oriented meshes, guide clearance, independent parameter behavior and matching browser exports. Three OpenSCAD exports were compared with the generator. Default and extreme variants were sliced. Bevel checks confirm the 45° profile, the flat face dimensions and the thin-base transition. Additional checks compare the retained inner vertices and slot widths with v3, verify continuous and nonnegative profile curvature, and measure actual STL sections against the intended outer profile. Results are in `validation.json`.

These checks do **not** measure impact resistance, puncture resistance, fatigue or a maximum permissible fall. For a fall hazard, use a guard with documented protective performance appropriate to the situation. See [OSHA's published findings on ordinary plastic rebar caps](https://www.osha.gov/laws-regs/standardinterpretations/1997-05-29-0), cited for the technical distinction rather than as a statement of applicable Czech law.

## Source and licence

Original: [Rebar Safety Cap 6/8/10mm by Niklas](https://www.printables.com/model/1302065-rebar-safety-cap-6810mm), [author profile](https://www.printables.com/@Niklas), licensed [CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/).

This derivative adapts the user's supplied `rebar_cap_8mm.stl`, adding the parametric head/base, radial bar-size variants, hollow guide, narrowed slots and rebuilt outer neck. The 6, 10 and 12 mm variants are adaptations of that supplied 8 mm file, not copies of the author's other sizes. No endorsement is implied. See `LICENSE.txt` for attribution and non-commercial conditions.
