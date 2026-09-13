# NAATI CCL Hindi Simulator — my build, with the supplied sets added

Open `index.html` over **https** or `http://localhost` (Chrome or Edge).
Speech recognition and the microphone are both blocked on `file://`.

    python3 -m http.server 8000      # then http://localhost:8000/

## What's in it

Seven tests, 183 segments, 553 meaning units, 76 entity checks.

| Test | Dialogues | Audio |
|---|---|---|
| TEST-001 | Banking / school enrolment | synthesised |
| TEST-002 | GP back injury / Centrelink JobSeeker | synthesised |
| TEST-003 | Rental inspection / workplace injury | synthesised |
| REF-01 | Health / Housing | supplied recordings |
| REF-02 | Employment / Financial | supplied recordings |
| REF-03 | Education 1 / Education 2 | supplied recordings |
| REF-04 | Social Services / Consumer Affairs | supplied recordings |

The eight supplied sets are paired into four two-dialogue tests, so each one
scores out of 90 with the real pass rule: 63 overall and at least 29 per
dialogue. Use the Dialogue 1 / Dialogue 2 modes to sit one on its own.

Segments with a supplied recording play that file. If the `audio` folder is
missing, they fall back to synthesised speech automatically.

Keep `audio/reference/` beside `index.html` — the paths are relative.
