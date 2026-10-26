# Ṣaṭkāla Hexagram — Vaikhānasa Archana Times

An interactive six-pointed star (hexagram) visualization of the **Vaikhānasa Ṣaṭkāla** — the six daily worship times prescribed in the Vaikhānasa Āgama tradition.

<p align="center">
  <img src="preview.png" alt="Ṣaṭkāla Hexagram" width="400">
</p>

## What It Shows

A **Star of David (hexagram)** formed by two interlocking equilateral triangles, with each of the six points representing one of the six daily archana times:

| Star Point | Kāla | Sanskrit | Telugu | Astronomical Basis |
|:---:|---|---|---|---|
| ⬆️ Top (0°) | **Madhyāhna** | मध्याह्न | మధ్యాహ్నం | Solar noon (zenith) |
| ↗️ Upper-right (60°) | **Aparāhṇa** | अपराह्ण | అపరాహ్ణం | Midpoint of noon → sunset |
| ↘️ Lower-right (120°) | **Sāyaṅkāla** | सायङ्काल | సాయంకాలం | Sunset |
| ⬇️ Bottom (180°) | **Niśi** | निशि | నిశి | Pradoṣa (~1.5 hrs after sunset) |
| ↙️ Lower-left (240°) | **Prātyuṣam** | प्रात्युषम् | ప్రాత్యుషం | Brahma muhūrta (~96 min before sunrise) |
| ↖️ Upper-left (300°) | **Prātaḥkāla** | प्रातःकाल | ప్రాతఃకాలం | Sunrise |

### Visual Elements

- **Sun indicator** orbits the circumcircle, interpolating between kāla points based on live solar position
- **Active arc** highlights the current kāla segment
- **Active triangle** fills to show which section of the day is current
- **Countdown text** shows time remaining to the next kāla
- **Thirunāmam** (Śrīvaiṣṇava ūrdhva puṇḍra with Śrī Chūrṇam) drawn in the central hexagon
- **Bilingual labels** — Sanskrit (IAST) + Telugu script + computed local time at each point

## How It Works

All six archana times are **computed from live solar position** using your device's geolocation:

- **Sunrise / Sunset / Solar Noon** — calculated from Julian Date, Equation of Time, and solar declination
- **Brahma Muhūrta** — 96 minutes (1.6 hours) before sunrise
- **Pradoṣa Kāla** — ~1.5 hours after sunset
- **Aparāhṇa** — midpoint between solar noon and sunset

No external APIs are called. Everything runs client-side in a single HTML file with zero dependencies.

## Usage

Open `index.html` in any modern browser. The page will:

1. Request your geolocation (or default to Tirupati / Śrī Veṅkaṭeśvara if denied)
2. Compute sunrise, solar noon, and sunset for your coordinates
3. Derive the six archana times and render the hexagram
4. Update every 60 seconds

### Theming

Automatically adapts to light and dark mode via `prefers-color-scheme`. The warm parchment palette in light mode transitions to a deep temple-interior dark mode.

## Tradition

The **Vaikhānasa** tradition is one of the two principal Āgamic traditions of Śrīvaiṣṇavism (alongside Pāñcarātra). The **Ṣaṭkāla** (six-time) worship schedule structures the daily ritual cycle at temples such as Tirumala Śrī Veṅkaṭeśvara.

The six times are not arbitrary clock hours but astronomical events — dawn, sunrise, zenith, afternoon, sunset, and nightfall — ensuring that worship follows the natural solar rhythm.

## License

MIT
