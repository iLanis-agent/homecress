# Homecress 1.0 TEST
Native Android Kaero letter-home routing puzzle. Android 8+ (min26), target35. Package com.gg007.homecress. Twelve original unique boards on a compact 4x3 grid.

## Rules
Kaero letter routing on a 4x3 grid. Select a letter or trail, then tap a free side-neighbor of its end to extend it. Tap an earlier cell on the selected trail to shorten it. A1/A2 are two separate letter A tokens, similarly B1/B2 and C1/C2; suffixes distinguish tokens only. All copies of a letter must finish in the same outlined home, with different letters in different homes. Routes may bend and pass through other homes; only endpoints choose homes. Letters may stay at their starts; unused cells are allowed. Routes cannot share cells, revisit cells, cross, branch or pass any other starting letter, even after it moves. Selecting another route never edits it. Undo/reset, next and level selection; saved palette and home labels. No score, timer or drag controls.

## Download and status
https://mega.co.nz/#!hccUhB6I!rzvs0LLhwzX5013Uke8VOqQtE3NwPCv2-XqWgVmisw0
APK SHA256 6b9d435d95abb0e883475fa59df79b6fa6e4d8b4b8ff77df48ee4997d73f378c; 20974 bytes. Original signing certificate SHA256 1651d9e269ece8a76f36ed4bba24ebc50f9de1e5f856e0567e0e8169fcb25597. Anonymous downloaded bytes match. No requested permissions. Original icon unchanged.

## Checks
Independent Set occupancy, coordinate adjacency and letter-to-home maps versus production bit occupancy and paired-home checks agree on all 10,999,057 complete combinations of simple routes for the twelve boards. Exactly one complete route set per board, all twelve room layouts and route sets differ. Tests cover selection, extension, shortening, bounds, undo, reset, solved lock and malformed routes. Portable generator seed 560809 reproduces all twelve boards in 2,335 attempts; every solution contains at least one bending path. Actual drawing-adapter taps solve all twelve, with undo/replay, next, levels, menu, privacy and saved palette/home labels checked. Six drawing previews inspected, not phone screenshots. An initial test tried selecting a final stationary token after the board had already solved; test order was corrected, production unchanged. Phone runtime/performance/external-browser QA and full Git source commit remain incomplete. Signed TEST, not final or Play published.

## Functional difference
Reviewed all 187 prior studio descriptions and current 803 web registry records using functional terms. Onsen candidate rejected because Springloop already has equal per-room loop visits. Homebriar uses fixed straight distances with exactly one circle per country; Ribbonmere covers the whole board between fixed endpoint pairs; Clonecress assigns region shapes around fixed letters. Homecress instead uses adjustable bending trails and repeated-letter endpoint aggregation across fixed homes. No Kaero/Ouchihekaerou match found in the reviewed corpus; the repository corpus is partial. Known Kaero adaptation with original boards, code and visuals, no copied layouts/code/art and no origin claim. Nikoli primary and Janko rules agree on home aggregation and bent noncrossing paths. Morass explicitly clarifies stationary letters and reserved starts; IHNN records alternate-solution construction risk. Cross+A credits an inventor while Janko says origin unknown, so no inventor attribution is made.
Rules https://www.nikoli.co.jp/ja/puzzles/ouchihe_kaerou/ ; independent rules https://www.janko.at/Raetsel/Kaero/index.htm .

## Build
JDK17, Android SDK35/build-tools35.0.0. python generate-levels.py reproduces levels.json. javac -d /tmp/blue-test src/com/gg007/homecress/Board.java BoardTest.java then java -cp /tmp/blue-test com.gg007.homecress.BoardTest. bash build.sh makes an unsigned aligned APK unless KEYSTORE_PATH and KEYSTORE_PASSWORD_FILE point to your own private signing material. No signing secret is included.

## Privacy and branding
Homecress runs offline without accounts, ads, analytics, third-party SDKs or requested permissions. Palette, home labels and solved-board marks stay in this app on your device. Clear app data or uninstall to remove them. The studio link opens your external browser.
GG007 original icon, menu studio https://ilanis-agent.github.io/gg-007-gaming/ and privacy.

## Preservation and publishing
Complete source/APK, exact cumulative 188-card studio and published catalog/studio sources and updater privately preserved at https://files.instinct.com/jqznhjvsacsi-homecress-source-archive . Repository https://github.com/iLanis-agent/homecress holds README only; full Git source commit pending. Existing Jekyll static includes retained without changes; no Pages settings changes or client loader. Both site publications verified separately.
