# VTuber Forge

Mobile-first, offline Android avatar editor. The editor is bundled in the APK and requires no network at runtime.

## Implemented
- Parametric per-part anatomy editor: height, width, depth, volume, muscle/soft-tissue shaping, region tags, and reset controls.
- Detailed editable base anatomy: torso, chest, pelvis, neck, head, ears, eyes, nose, mouth, hair, upper/lower arms, hands, fingers, thighs, calves, feet, and toes.
- WebGL 3D viewport with touch orbit/zoom and tap selection
- Procedural avatar parts and primitives
- Object transforms and material controls
- Vertex mode with per-vertex editing
- Bone hierarchy / IK target state and expression controls
- Timeline/keyframe state
- Offline autosave to local device storage
- `.vforge.json` project save/load
- OBJ export
- GLB export
- GLB/VRM binary import for mesh geometry
- VRM 1.0 binary export with humanoid metadata, expressions, first-person/look-at metadata and spring-bone extension scaffolding

## APK build
GitHub Actions builds `app-debug.apk` on push or manual dispatch. The workflow installs Android SDK 35 and Gradle 8.10, then uploads the APK as `vtuber-forge-debug-apk`.

## Runtime
No CDN, web server, account, or network connection is required by the editor.

## Important format note
VRM export is generated locally as a VRM 1.0 glTF binary with humanoid metadata. Complex externally authored VRM assets may contain skinning, morph, texture, MToon, and spring data that the lightweight editor does not yet preserve on round-trip import.
