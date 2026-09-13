# European megalith transport

Gazetteer and flow map of **published, sourced hauls** of architectural stone in Neolithic and Chalcolithic Europe. Arrow weight scales with distance; the gazetteer is the same record set.

- Map: [timdaw37.github.io/european-megalith-transport](https://timdaw37.github.io/european-megalith-transport/)
- Gazetteer table: [gazetteer.html](https://timdaw37.github.io/european-megalith-transport/gazetteer.html)
- Data: [`data/hauls.json`](data/hauls.json) (canonical) and [`data/hauls.csv`](data/hauls.csv)

Current build: **v0.2** (13 September 2026).

## What the map is

Each record is one **source → monument** movement where petrography, geochemistry, microfacies, physical refit or an excavated quarry identifies a non-local outcrop, and glacial / purely gravitational delivery is implausible.

The line is a **schematic flow**, not a reconstructed Neolithic road or sea route. Source points marked `sector-centroid` or `basin-sector` are midpoints of a published search area, not a pegged quarry face.

Stroke weight uses `1.2 + 3.4 × log10(km)` so a 4 km Gavrinis crossing remains visible next to the 750 km Altar Stone line. Colour bands:

| Colour | Distance |
| --- | --- |
| Green | < 20 km |
| Amber | 20–200 km |
| Red | ≥200 km |

Click a line, a point, or a row in the side list. Each haul has a stable id (`#SH-altar`) shared by the map and the gazetteer page.

## What it is not

- Not every European dolmen. Most megaliths used stone from the building plot.
- Not Funnel Beaker chambers built of glacial erratics (ice moved the block; people stood it up).
- Not Carnac alignments (local granite).
- Not a claim that 19th-century 35–40 km attributions (La Perrotte, Moulins-sur-Céphons) have been re-proven.

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
