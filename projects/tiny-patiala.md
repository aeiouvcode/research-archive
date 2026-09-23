# Tiny Patiala

- Repository: https://github.com/aeiouvcode/tiny-patiala
- Live: https://aeiouvcode.github.io/tiny-patiala/

## Inspiration

An isometric miniature-city post on X (2026-09-21), made for the owner's own town, Patiala, Punjab.

## References

- OpenStreetMap data around Qila Mubarak: 96 building footprints, 155 road segments.

## Findings

- A photoreal version was requested. A Street View coverage probe found 112 of 169 points around Qila Mubarak, Adalat Bazaar and Dharampura Bazaar returned panoramas. That version is blocked on a Google Maps API key.

## Technical decisions

- Real OSM footprints with stylized rooftops and chhatri domes, and a day/night toggle.
- The scene ships gzip-compressed in five chunks (p0-p4) that are decompressed in the browser.

## Gaps

- The source X post link is in chat history (2026-09-21 17:57).
