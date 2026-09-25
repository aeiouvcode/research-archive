# Tiny Patiala

- Repository: https://github.com/aeiouvcode/tiny-patiala
- Live: https://aeiouvcode.github.io/tiny-patiala/

## Inspiration

An isometric miniature-city post on X (2026-09-21), made for the owner's own town. Asked where: "Patiala, punjab, the rest is your guess."

## References

- OpenStreetMap data around Qila Mubarak: 96 building footprints, 155 road segments.
- Google Street View coverage probe (2026-09-21): 112 of 169 probes around Qila Mubarak, Adalat Bazaar and Dharampura Bazaar returned panoramas.

## Findings

- The owner rejected the first stylized pass: "Not realistic, use google street view." The photoreal version is blocked on a Google Maps API key from him.
- v13 (2026-09-22) made the Qila its own precinct: gate, cupolas, arcades, courtyards. v14 live 2026-09-23.
- Still behind the reference: flat ground, buildings need stepped massing and balconies, Qila massing too regular.

## Technical decisions

- Real OSM footprints with stylized rooftops and chhatri domes, and a day/night toggle.
- The scene ships gzip-compressed in five chunks (p0-p4) that are decompressed in the browser.

## Gaps

- The source X post link is in chat history (2026-09-21 17:57).
- Photoreal rebuild: waiting on the owner's Google Maps API key.
