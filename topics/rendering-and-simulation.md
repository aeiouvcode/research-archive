# Rendering and simulation

Shared lessons from ISSEN, Stillwater, KIN, Tidemill, Apex Tide, Ljusvik and Vargmyra.

- **Simulate the named effect.** Shader noise is not water; a flat tilemap is not 3D. Stillwater uses a damped heightfield; Tidemill was rebuilt in real 3D after a side-by-side with its reference.
- **Phone budgets decide the ceiling.** KIN leaves out true refraction and ray-traced bounce for phone performance; Apex Tide is tuned for mid-range GPUs.
- **Three.js from a CDN vs vendored.** CDN with an import map and SRI keeps repos small (ISSEN, Tidemill, Stillwater, Apex Tide); vendoring (Clock Out, Optimus Prime, Patiala Flatball) removes the network dependency. Pick per project and note it in the README.
- **Check at 390px.** Phone-width audits repeatedly found the real weaknesses (ISSEN ground texture, FRAME ZERO choice screen, Clock Out touch controls).
