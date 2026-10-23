# V2 Build + Testing Proof

Build/test dates: October 13-20, 2026. This is the V2 revision (ESP32-S3-WROOM-1,
E22-900M30S, NEO-M9N GPS, IP5306 power stage, SSD1306 OLED, DS3231M RTC, JST-PH
battery input, USB-C).

## Build

- October 13: PCB arrived.
- October 19: solder paste stencil, hotplate reflow, front and back of the
  assembled board.
- October 20: board powered up and working; first Meshtastic mesh test.
- LED blink test recorded in `video/blink.mp4`.

Assembly details to fill in: <paste + reflow notes, bridges and fixes, parts
fitted or skipped, bodges, first power-up result>.

## Testing

| Check | Expected | Measured | Result |
|-------|----------|----------|--------|
| VBUS / USB-C input | 5V | <fill> | <pass/fail> |
| Battery charge (IP5306) | charges, status LEDs | <fill> | <pass/fail> |
| 5V boost output | 5V, up to 2.4A | <fill> | <pass/fail> |
| 3.3V rail (TLV75733) | 3.3V | <fill> | <pass/fail> |
| ESP32 flash + boot | flashes, boots | <fill> | <pass/fail> |
| USB serial / console | enumerates | <fill> | <pass/fail> |
| OLED | displays | <fill> | <pass/fail> |
| RTC (DS3231M) | I2C detected, keeps time | <fill> | <pass/fail> |
| GPS (NEO-M9N) | NMEA sentences / fix | <fill> | <pass/fail> |
| Radio (E22-900M30S) | TX/RX with another node | messages exchanged over the mesh | pass (mesh test) |
| Meshtastic firmware | node joins mesh | 6 nodes online, own message delivered, replies received | pass |

Mesh test evidence (October 20, 19:01-19:13): node list shows 6 online / 6 shown /
6 total; a `Test` message was delivered to the LongFast channel and other nodes
answered. Screenshots below.

## Known issues

- <fill in: bugs, errata, bodges, things that did not work first try>

## Media

| File | What it shows |
|------|---------------|
| `image/pcb_arrived.jpg` | PCB arrived, October 13 |
| `image/pcb_pasting.jpg` | solder paste applied, October 19 |
| `image/pcb_hotplate.jpg` | reflow on the hotplate, October 19 |
| `image/radio_front.jpg` | assembled board, front |
| `image/radio_back.jpg` | assembled board, back |
| `image/radio_working.jpg` | board working, October 20 |
| `image/screenshot_nodes.png` | Meshtastic app: 6 nodes online, 6 shown, 6 total |
| `image/screenshot_sendmessage.png` | LongFast: `Test` message delivered to mesh |
| `image/screenshot_receivemessage.png` | LongFast: replies from other nodes |
| `video/blink.mp4` | LED blink test (4K original) |
| `video/compressed/blink.mp4` | same clip, 1080p preview |
