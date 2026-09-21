# DIN Rail Distribution Stud Holder

This is a **distribution stud for cable lugs**: a common-potential connection point for joining incoming and outgoing cables and distributing power, for example in **Victron Energy systems**. Cable lugs are stacked on the metal bolt and clamped with a nut. The printed holder secures that stud to the DIN rail.

A one-piece holder that clips onto a nominal 35 mm DIN rail and holds a hex-head bolt perpendicular to the rail. The head inserts from the rear into a captive hex recess; the threaded shank points outwards. One rail hook is fixed and the opposite latch uses a U-shaped spring with a screwdriver release notch.

[Open the live configurator](https://oliveres.github.io/3D/din-rail/) · [Download the complete offline package](DIN_Rail_Bolt_Holder_MakerWorld_Package.zip)

## Quick start

Open **index.html** in a desktop browser. It works offline and needs no installation. Select the four settings, preview the part and download an STL.

Alternatively, choose an STL from the `STL` folder, or open **DIN_Rail_Bolt_Holder.scad** in OpenSCAD, use its Customizer, press **F6**, then **File → Export → Export as STL**.

For Bambu Studio, `BambuStudio/DIN_M8_2module_36mm_X1C_PLA.3mf` contains the default M8 holder and suggested X1 Carbon / 0.4 mm nozzle / Generic PLA settings. Check the selected printer, filament and build plate before slicing. The editable project includes a sliced preview. Select your own printer, material and plate settings and slice again before printing.

## Four settings

| Setting | Choices / range | Default |
|---|---|---|
| Hex-head bolt | M6, M8, M10 with 16 mm head, M10 with 17 mm head | M8, 13 mm head |
| Holder width | M6/M8: 18 or 36 mm; M10: 27 or 36 mm | 36 mm |
| Rail width allowance | −0.50 to +0.50 mm relative to the 35.75 mm stop spacing | 0.00 mm |
| DIN rail sheet thickness | 0.80 to 2.00 mm | 1.00 mm |

One module is defined as **18 mm** in this model. The 27 mm option is 1.5 modules. The browser offers only compatible widths; OpenSCAD rejects invalid combinations.

### Default dimensions

- Nominal DIN rail width: **35 mm**.
- Distance between the rail registration faces: **35.75 mm**.
- U spring wall: **1.40 mm**; outer radius: **3.00 mm**.
- Distance between the retaining tips: **31.80 mm** (each lip extended inward by 0.50 mm).
- Rail sheet thickness: **1.00 mm**; both flange grooves: **1.20 mm**.
- Clearance between the body support and spring latch: **0.40 mm**, maintained across the sheet-thickness range.
- M8 holder width along the rail: **36 mm**.
- Default overall mounted envelope: **36 × 50 × 14.2 mm**.
- M8 through-hole: **8.60 mm**; hex recess: **13.35 mm across flats**, **6.80 mm deep**.

The width allowance changes the total stop spacing, split equally between both ends. For example, **+0.10 mm** gives **35.85 mm** stop spacing; each end moves outwards by 0.05 mm. A negative value narrows the gap. This is an adjustment to the model, not a measurement of the rail itself.

| Bolt | Head across flats | Through-hole | Hex recess across flats | Recess depth |
|---|---:|---:|---:|---:|
| M6 | 10 mm | 6.60 mm | 10.35 mm | 5.50 mm |
| M8 | 13 mm | 8.60 mm | 13.35 mm | 6.80 mm |
| M10 ISO | 16 mm | 10.60 mm | 16.35 mm | 8.00 mm |
| M10 DIN | 17 mm | 10.60 mm | 17.35 mm | 8.00 mm |

All eight supplied STL/STEP variants use **0.00 mm allowance** and **1.00 mm sheet thickness**. Bolt length is left to the application. Bolts, washers, nuts and DIN rail are not included.

## Printing

The STL exports are already lying on their side. Keep this orientation: it places spring bending in the layer plane. The STEP models use the mounted coordinate system and must be oriented before printing.

Suggested starting settings, also included in the Bambu Studio project:

- 0.4 mm nozzle, 0.20 mm layer height.
- Arachne wall generator, 6 walls, 6 top and bottom layers.
- 60% gyroid infill.
- Supports off; optional 4 mm outer brim.
- Remove any brim strands from the spring gap before fitting.

The clip design was developed through physical fit trials in PLA. The modular widths and custom parameter combinations need their own fit check; holder width and material affect spring stiffness. PLA, PETG and ASA require material-specific printing settings. The included project uses Generic PLA.

## Assembly and release

1. Clear the through-hole, hex recess and spring gap of stray filament.
2. Insert the bolt from the rear until its head sits in the hex recess.
3. Hook the fixed side over one DIN rail flange, then press the spring side over the opposite flange.
4. Place the cable lugs for the same electrical potential onto the exposed bolt and secure the connection with the appropriate nut and washers.
5. To remove the holder, use the notch beside the moving jaw to gently deflect the latch away from the rail, then lift that side free.

This is a mechanical holder. It does not establish an electrical current rating or a certified insulation rating for a cable connection.

## Package contents

- `index.html` — self-contained English browser configurator and STL exporter.
- `DIN_Rail_Bolt_Holder.scad` — self-contained English OpenSCAD source with four Customizer inputs.
- `STL/` — eight ready-to-slice variants, in print orientation.
- `STEP/` — matching eight solid CAD models, in mounted orientation.
- `BambuStudio/` — default M8 / 36 mm editable project with suggested settings.
- `images/` — two labelled CAD renders and a dimension diagram.
- `publishing/` — English MakerWorld listing text and upload notes for the author.
- `CREDITS.md` — design inspiration and dimensional references.
- `variants.json` — dimensions and parameters of each supplied variant.
- `CHECKSUMS.sha256` — file integrity hashes.

Digital validation covered 72 parameter combinations and comparison of 16 OpenSCAD/browser export pairs. All those meshes are closed, single solids. The support-to-latch gap was checked in every export. This does not replace a physical fit or load test of a chosen variant.

## Retention update

Both retaining lips were extended 0.50 mm towards the centre, including their insertion chamfers. This reduces the tip gap by 1.00 mm while preserving the rail registration faces, groove thickness, spring profile and bolt pocket. At +0.05 mm rail allowance, the tip gap is 31.85 mm; at the default 0.00 mm allowance it is 31.80 mm. The longer lips address reported accidental release; this revision still needs its own physical fit check.

## Spring update

The U spring is thickened by 0.20 mm along its outside, increasing its nominal wall from 1.20 to 1.40 mm. The moving leg and release-notch wall meet without the former 0.10 mm shoulder. The inside of the U, retaining tips, rail fit and bolt recess stay unchanged. This adjustment follows print feedback that the previous spring released too easily; fitting and release force still need to be checked on the actual print.
