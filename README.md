# European megalith transport

Gazetteer and flow map of **published, sourced hauls** of architectural stone in Neolithic and Chalcolithic Europe. Arrow weight scales with distance; the gazetteer is the same record set.

- Map: [timdaw37.github.io/european-megalith-transport](https://timdaw37.github.io/european-megalith-transport/)
- Gazetteer table: [gazetteer.html](https://timdaw37.github.io/european-megalith-transport/gazetteer.html)
- Data: [`data/hauls.json`](data/hauls.json) (canonical) and [`data/hauls.csv`](data/hauls.csv)

Current build: **v0.3** (13 September 2026). 31 hauls. The map has a **Not Stonehenge** toggle so the four Salisbury Plain lines do not swamp western Europe.

## What the map is

Each record is one **source → monument** movement where petrography, geochemistry, microfacies, physical refit or an excavated quarry identifies a non-local outcrop, and glacial / purely gravitational delivery is implausible.

The line is a **schematic flow**, not a reconstructed Neolithic road or sea route. Source points marked `sector-centroid` or `basin-sector` are midpoints of a published search area, not a pegged quarry face.

Stroke weight uses `1.2 + 3.4 × log10(km)` so a 4 km Gavrinis crossing remains visible next to the 750 km Altar Stone line. Colour bands:

| Colour | Distance |
| --- | --- |
| Green | < 20 km |
| Amber | 20–200 km |
| Red | ≥ 200 km |

Click a line, a point, or a row in the side list. Each haul has a stable id (`#SH-altar`) shared by the map and the gazetteer page.

## What it is not

- Not every European dolmen. Most megaliths used stone from the building plot.
- Not Funnel Beaker chambers built of glacial erratics (ice moved the block; people stood it up).
- Not Carnac alignments (local granite).
- Not Callanish / Calanais. The pillars are Lewisian gneiss from the same ridge (Cnoc an Tursa knoll, Druim nan Eum, Na Dromannan). That is siting on the outcrop, not a sourced haul.
- Not a claim that 19th-century 35–40 km attributions (La Perrotte, Moulins-sur-Céphons) have been re-proven.

## The debate this list is for

The gazetteer is an evidence table for a three-paper exchange in *Antiquity* that still sets the terms:

1. **R. S. Thorpe & O. Williams-Thorpe 1991.** “The myth of long-distance megalith transport.” *Antiquity* 65: 64–73. Most published long hauls, Stonehenge bluestones included, were weakly provenanced; glacial erratics and local stone had been underplayed.
2. **Aubrey Burl 1991.** “Megalithic myth or man the mover?” *Antiquity* 65: 297–298. Push-back: people did move large stones, and the glacial-erratic reading of Stonehenge does not close the case.
3. **Mark Patton 1992.** “Megalithic transport and territorial markers: evidence from the Channel Islands.” *Antiquity* 66: 392–395. Middle position. La Hougue Bie (`LHB-foreshore` in this gazetteer) shows short-to-medium hauls that are not simply “whatever is nearest.” Kalb 1996 on Vale de Rodrigo (`VDR-barroco`) is written as a sequel to the same argument.

Modern petrography and isotopes (Bevins, Ixer, Nash, Clarke and the Iberian geoarchaeology papers) have superseded parts of 1991 — the bluestones and the Altar Stone are no longer a myth — but they have also confirmed the other half of Thorpe & Williams-Thorpe: the default European megalith is local or a few kilometres. The histogram in this dataset is Patton’s picture with a thin long tail: a fat local peak, a 3–18 km territorial band, and a handful of genuine long hauls.

Clarke et al. 2026 on the Devil’s Arrows (`DA-brimham`) is a direct empirical reply to the 1991 glacial-erratic suggestion for that row.

## Evidence grades

- **high** — named outcrop or quarry, modern petrography / isotopes / physical refit.
- **medium** — solid published lithology match, but sector rather than face, or an older monograph not re-run with ICP-MS.

## How to add a haul

1. Add an object to `data/hauls.json` with the same keys as the existing rows.
2. `km_used` is the figure drawn; keep `km_min` / `km_max` as the published range.
3. Set `source_precision` honestly (`named-quarry`, `named-outcrop`, `sector-centroid`, `basin-sector`).
4. Cite the paper that pins the source, not a guidebook.
5. Rebuild `data/hauls.csv` from the JSON if you edit by hand.

## Licence

Text, gazetteer coordinates assembled here, and the map page: **CC BY-SA 4.0 Tim Daw**.

Underlying geological identifications remain those of the cited authors. Monument locations are public heritage coordinates. If a landowner or author wants a source point coarsened, open an issue.

## Related

Same workshop as [Altar-Stone-Source-Screening](https://github.com/TimDaw37/Altar-Stone-Source-Screening), [stonehenge-plan](https://github.com/TimDaw37/stonehenge-plan), [wiltshire-long-barrows](https://github.com/TimDaw37/wiltshire-long-barrows).
