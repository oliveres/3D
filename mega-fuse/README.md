# DIN rail MEGA fuse holder

A compact, two-part holder for mounting a MEGA fuse vertically across a 35 mm DIN rail, for example in Victron Energy systems. Two M8 bolts have a fixed 50.8 mm centre spacing. Cable lugs attach at the two separate fuse terminals.

The current package combines **DIN clip v5** with the accepted **fuse carrier v3**. The U spring is thickened by 0.20 mm on the outside, increasing its nominal wall from 1.20 to 1.40 mm and removing the small shoulder at the release notch. The previously extended retaining tips remain unchanged. The carrier is unchanged. One hook stays fixed and the opposite hook releases through a U-shaped spring and screwdriver notch.

[Open the live configurator](https://oliveres.github.io/3D/mega-fuse/) · [Download the complete offline package](MEGA_Fuse_Holder_Package.zip)

## Quick start

Open `index.html` in a browser to preview the assembly, inspect the profile or exploded view, adjust rail fit and download STL files. Everything works offline. The package also includes editable OpenSCAD and STEP models and a Bambu Studio project.

## Dimensions

| Feature | Default |
|---|---:|
| Width along rail | 27 mm / 1.5 modules |
| Height across rail | 72.8 mm |
| Assembly depth, excluding hardware | 25.2 mm |
| M8 bolt pitch | 50.8 mm |
| M8 clearance holes | 8.6 mm |
| M8 hex-head pockets | 13.35 mm across flats × 6.3 mm deep |
| Matching clip/carrier contact footprint | 27 × 22 mm |
| Central recess below the terminal pads | 7.4 mm |
| Minimum free depth over the 29.2 × 19 mm fuse footprint, including chamfers | 6.1 mm |
| Rail registration spacing | 35.75 mm |
| Gap between retaining tips | 31.80 mm |
| Rail sheet thickness / flange grooves | 1.00 / 1.20 mm |
| Support-to-latch gap | 0.40 mm |
| U spring wall / outer radius | 1.40 / 3.00 mm |
| Static clearance above the spring arch | 0.80 mm |

The fuse footprint follows the supplied drawing: 68.8 mm overall length, 50.8 mm hole pitch, 8.7 mm holes, a 29.2 × 19 mm central body and 16.2 mm wide terminals. The drawing did not specify the side profile; check the actual body underside against the recess.

## Hardware and assembly

- Two M8 hex-head bolts with 13 mm heads; choose their length for the fuse and terminal stack.
- Two **M4 × 8 DIN 912 socket-head screws** and two plain M4 nuts, 7 mm across flats and nominally 3.2 mm thick.
- Suitable M8 nuts and washers for the actual terminal stack.

1. Insert the M8 bolts into the carrier from the rear, with their threads pointing outwards.
2. Insert the two M4 nuts into the rear pockets of the DIN clip.
3. Join the parts with the two M4 × 8 screws inserted through the central front recess. Their heads sit below its floor. Longer screws can protrude towards the rail.
4. Engage the fixed hook, then press the spring side onto the DIN rail. For removal, use the notch to move the spring latch outwards.
5. Mount the fuse and cable lugs with metal-to-metal contact. The two terminals remain separate except through the fuse.

This is a mechanical holder. It does not establish a current, thermal, fastening-torque or certified insulation rating for an electrical installation.

## Printing and rail fit

Both STL files are already oriented on their side, with a print height of 27 mm, so spring bending stays in the layer plane. Suggested starting settings are a 0.4 mm nozzle, 0.2 mm layers, Arachne, 6 walls, 60% gyroid infill and supports off. Clear any brim strands from the spring gap. The included Bambu project uses X1 Carbon and Generic PLA settings; select your actual printer, material and build plate, then slice again before printing. The project includes a sliced preview.

Rail allowance ranges from −0.50 to +0.50 mm. It changes the registration spacing of 35.75 mm and the retaining-tip gap of 31.80 mm by the same amount, shared equally between both ends. **At +0.05 mm allowance, the tip gap is 31.85 mm.** Sheet thickness ranges from 0.80 to 2.00 mm; each groove adds 0.20 mm clearance. The M8 pitch and carrier stay fixed.

The previous clip and carrier were refined from user feedback. The thicker spring is a new retention change and needs a fit check on the actual rail; narrower/wider allowances and material changes affect fitting and release force.

## Files

- `STL/MEGA_M8_clip_27mm_v5.stl` — current DIN clip with a thicker U spring and extended lips.
- `STL/MEGA_M8_carrier_27mm_v3.stl` — unchanged fuse carrier; an existing v3 print can be reused.
- `STEP/` — both parts and their assembly in installed coordinates.
- `MEGA_Fuse_Holder.scad` — both parts with rail allowance and sheet-thickness parameters; select `clip`, `carrier`, `layout` or `assembly`, render with F6, then export STL.
- `BambuStudio/` — current two-part X1 Carbon project, prepared on its side.
- `images/` — current CAD renders and dimensioned profile.
- `dimensions.json`, `CHECKSUMS.sha256` — dimensions and file integrity hashes.
- `publishing/`, `CREDITS.md` — listing text and references.

Product names identify compatibility; this is an independent design without a Victron Energy endorsement.
