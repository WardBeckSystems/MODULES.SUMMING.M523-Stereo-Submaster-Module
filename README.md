# M523 Stereo Submaster Module · Summing

Ward-Beck Systems M523, 1985|18. Wiki page: [M523 on WBSps.ca](https://wardbecksystems.github.io/WBSps.ca/PAGES/M523.html)

| Folder | What is in it | Files |
|---|---|---|
| [SCHEMATICS/](SCHEMATICS/) | electrical drawings: schematics, functional diagrams, component layouts, wiring | 65 |
| [MECHANICAL/](MECHANICAL/) | front panels, cover plates, metalwork, assemblies; the front panel as vectors | 14 |
| [PINOUTS/](PINOUTS/) | the RTO-144 connector: connection sheets, connector layouts, rear views | 13 |
| [MANUALS/](MANUALS/) | manuals, manual pages, price lists, brochures, documents | 35 |
| [PHOTOS/](PHOTOS/) | photographs of the module | 2 |
| [SOFTWARE/](SOFTWARE/) | program listings, firmware, the plugin | 1 |
| [KICAD/](KICAD/) | KiCad schematics traced from the drawings, the symbol, PCB projects | 12 |
| [OCR/](OCR/) | the note of every file: date, origin, title block, OCR text | 55 |

<!-- module data: tools/module_specs.py, tools/forum_quotes.py -->

**On the WBSps forum (2006|39 - 2014|47):** [3 topics](FORUM.md): what owners and technicians said about it.

## Specifications

From the technical data sheet: [1985 - M523 - ST Series - Stereo Submaster Module - 004.jpg](MANUALS/1985%20-%20M523%20-%20ST%20Series%20-%20Stereo%20Submaster%20Module%20-%20004.jpg) page 1 (read by OCR; check against the page). As data: [`Specifications.json`](Specifications.json).

| | |
|---|---|
| **Ambient temperature** | to 60 degrees Celsius_ The submastering functions ior the St series of Stereo Television consoles are found in the M523 Stereo Submaster Module. |
| **Dimensions** | 1.60&quot; ide 14.15&quot; high 6.50&quot; deep (41 mm 360 mm 165 mm The mixing bus amplifiers are an integral part of this module The outputs from these amplifiers feed the actively balanced insert points, where the insert jackfield and the stereo inline slide mixing attenuator are connected |
| **Weight** | Ibs (1.8 kg). 1 Answer erefadekftekeofincoine mixiov ideenuatorich Thonneess beeweere erefade auxiliary functions of the module as wel\| as the mix bus level sensors The module output amplifiers makeup for the insertion loss of the inline slide ixing attenuator and are capable of delivering an output level of +30 dBm (1 wait) into 600 ohm load_ The nomina output level is typically set to +8 dBm. Direct outputs are provided for externa program feeds and mon storing. The outputs from the M523 ia2 3C2 assignment selecio-s in stereo for master and master These selector outputs are through the module' s Balance control The stereo solo takeoff point is after the Balance control as well thus reflecting stereo spectral position in the selected solo function separately derived Mono ou Input is available, both directly at the module connector and via the master mono and master mono bus selectors_ The ST series of consoles have master and master outputs derived separately irom the submaster in both stereo and mono Four Auxiliary outputs are available, each ith separate pre/post fade selector assignment selector and level adjust control Auxiliaries and feed the stereo auxiliary mix buses and and feed the mono auxiliary mix buses _ The Channel On and Solo functions of the M523 Submaster Module are made via solid state FET switches This provides for very reliable and silent Swi thing. The control of these solid state switches maybe done directly through the pushbuttons on the module or remotely through the central microprocessor based control system |

## Circuit description

From [1985 - M523 - ST Series - Stereo Submaster Module - 007.jpg](MANUALS/1985%20-%20M523%20-%20ST%20Series%20-%20Stereo%20Submaster%20Module%20-%20007.jpg) page 1 (read by OCR; check against the pages). As data: [`CircuitDescription.json`](CircuitDescription.json).

<details><summary>Read it</summary>

Solo CR3, CR4, R117 and C30 makeup the peak detector circuit. U4A and 05 drive the red overload LED indicator of DSI When the red section illuminates 06 turns off extinguishing the green norma| level indicator The solid state solo switches are fed irom the Ba ance control output. The stereo solo monitoring wil follow the settings of balance control RI/R4. FETS 01 and 02 w i E th operational amplifiers UIA and U1B form the solid state switch and buffering amplifier ior the left channel solo output. The left output appears at P1 pins 29 and 30 of the module connector, fed through mix bus resistors R53 and R54 Simarily DS2, the out indicator, is driven by section and 08 through 010.

of U4 The threshold switch points of the four comparators in U4 are determined by the voltage divider R122, R1 24, R125 and the setting of the PEAK CAL trim control R116 Similarly the right channel solo circuit is made up of FETS Q3, 04 and operation amplifiers U2A and U2B Its output appears at P1 pins 31 and 32 of the module connector to correctly adjust R116, apply kHz test signals 50 that an insert level of +4 dBm is achieved at the left and right channel inserts of the submaster channel Adjust R116 So that Mix LED DSI just iuminates green, dropping the input level dB should resul in the LEC extinguishing. Raise the test signal level until the red LED iIuminates the green should extinguish) The insert signal level should be between +22 and +24 dBm. Auxiliaries Four auxiliary outputs are available from the M523 Auxiliaries and feed the stereo mix buses while and feed mono buses Each has pre/ post fade source selector, level adjust control ana an assignment se ector During tne above setup it is advisable to keep the inline slide mixing attenuator at 25 dB inhand or greater. Mix amplifiers 43A and U3B combine the stereo prefade inputs for mono auxiliaries and to conf rm the correct operation of DS2, the out program/peak indicator set the kHz test signals back to give an insert level of +4 dBm at the insert points. Also set the inline slide attenuator to 15 dB inhand The output level should now be +12 dBm and both DSI and DS2 should Muminate green Now raise the test signal levels until the red out LED iuminates (DS2) Confirm that the mono output level is +28 dBm +/-1 dB _ The prefade insert return inputs appear at P2 pins 49 and 50 (Left) and pins 51 and 52 (right) Program Peak Monitors The M523 has two sets of level monitors, one Label led Mix which measures the left and right channel signal levels at the module insert point and the other labelled out which monitors the modules monophonic OUtput. Normally the mono output is calibrated to match the left or right output Thus when the Teft and right stereo channels are driven simultaneously within phase signal material the mono output wil be dB higher in level DSI is the two colour LED indicator which illuminates green when the submaster mix bus level is at or above the nominal system operating level switches to red for an overload condition, which is at level of +22 dBm at the submaster insertion points Control Logic The details of the SA14-077 Control Subassembly are described under that particular section _ CRS CR6 R118, R123 and C31 form the averaging level detector. U4B and 07 drive the green normal LED section of DSI, This occurs when the program level at the prefade insert point is above dBm (it should be noted that 0 dB level difference exists between steady state tone and complex program material This assembly contains the matching circuitry for both the program channel switch and the solo switchThese latches maybe controlled either Loca Iy by momentary pushbuttons SW14 and SW15 or remotely through the console control system

</details>

<!-- /module data -->

## Mechanical

_Mechanical drawings: front panels, cover plates, metalwork and hardware (-03- drawings), AutoCAD files, each with its `(EXTRACTED).svg` vectors; `<module> - front panel.svg` is the front panel as vectors._

<table>
<tr><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/18HPkhyxLW1f6wjO3ep6i_ePOf6Ba6_Oj/view" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=18HPkhyxLW1f6wjO3ep6i_ePOf6Ba6_Oj" width="240" alt="1985 - M523 - B 523-04-001 - M523 STEREO SUBMASTER MODULE - MODULE LAYOUT.jpg"></a><br><sub>1985|18 · B 523-04-001 - M523 STEREO SUBMASTER MODULE - MODULE LAYOUT · <a href="MECHANICAL/1985%20-%20M523%20-%20B%20523-04-001%20-%20M523%20STEREO%20SUBMASTER%20MODULE%20-%20MODULE%20LAYOUT%20(EXTRACTED).svg">vectors</a></sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKY1BkakNsd3JZNVU/view?resourcekey=0-8S-UUmyhXYLRW_EeyyBZ6g" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKY1BkakNsd3JZNVU&resourcekey=0-8S-UUmyhXYLRW_EeyyBZ6g" width="240" alt="19xx - M523 - DOC - 3642-04-003 - ADERS STEREO MASTER FADERS MONO INPUT FADERS.jpg"></a><br><sub>19xx - M523 - DOC - 3642-04-003 - ADERS STEREO MASTER FADERS MONO INPUT FADERS · <a href="MECHANICAL/19xx%20-%20M523%20-%20DOC%20-%203642-04-003%20-%20ADERS%20STEREO%20MASTER%20FADERS%20MONO%20INPUT%20FADERS%20(EXTRACTED).svg">vectors</a></sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKNE04SVlJOHFBb28/view?resourcekey=0-GuSGF1-wsbyDzzYpjydCIQ" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKNE04SVlJOHFBb28&resourcekey=0-GuSGF1-wsbyDzzYpjydCIQ" width="240" alt="19xx - M523 - DOC - 523-04-001 - STEREO SUB MODULE.jpg"></a><br><sub>19xx - M523 - DOC - 523-04-001 - STEREO SUB MODULE · <a href="MECHANICAL/19xx%20-%20M523%20-%20DOC%20-%20523-04-001%20-%20STEREO%20SUB%20MODULE%20(EXTRACTED).svg">vectors</a></sub></td></tr>
</table>

## 3-D model

[`MECHANICAL/M523.stl`](MECHANICAL/M523.stl) (GitHub turns it in 3-D) · [view, change and generate it on WBSps.ca](https://wardbecksystems.github.io/WBSps.ca/2026/stl.html?m=M523)

- **Size:** 41 × 360 mm panel, 165 mm deep, 3.2 mm plate (TECHNICAL DATA: 1.60" ide 14.15" high 6.50" deep (41 mm 360 mm 165 mm The mixing bus amplifiers are an integral part of this module The outputs from these amplifiers feed the a)
- **From the drawing:** 17 holes and cut-outs, 0 knobs (front panel: `MECHANICAL/M523 - front panel.svg`)
- Made by `tools/module_models.py` (→ `MECHANICAL/M523.model.json`) and `tools/stl/make_stl.mjs` in [WBSps.ca](https://github.com/WardBeckSystems/WBSps.ca); the site makes the same STL from the same JSON.

## Schematics

_Electrical drawings: schematics (-02-), functional diagrams (-01-), component layouts (-06-), wiring (-09-), PCB files (.pcb .dsn), and beside each scan its `(EXTRACTED).svg`: the vectors traced from it._

<table>
<tr><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKQkdlbkpqSVJBRzg/view?resourcekey=0-SL55Lex7Hc3kODfC9IIwMg" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKQkdlbkpqSVJBRzg&resourcekey=0-SL55Lex7Hc3kODfC9IIwMg" width="240" alt="1985 - M523 - 523-02-001 - AICHT SOLO QUTPUT WES (2).jpg"></a><br><sub>1985|18 · 523-02-001 - AICHT SOLO QUTPUT WES (2) · <a href="SCHEMATICS/1985%20-%20M523%20-%20523-02-001%20-%20AICHT%20SOLO%20QUTPUT%20WES%20(2)%20(EXTRACTED).svg">vectors</a></sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/1AznwsFXhSNOPfyHLDSDZSWru_e59ZVSL/view" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=1AznwsFXhSNOPfyHLDSDZSWru_e59ZVSL" width="240" alt="1985 - M523 - 523-02-001 - AICHT SOLO QUTPUT WES.jpg"></a><br><sub>1985|18 · 523-02-001 - AICHT SOLO QUTPUT WES · <a href="SCHEMATICS/1985%20-%20M523%20-%20523-02-001%20-%20AICHT%20SOLO%20QUTPUT%20WES%20(EXTRACTED).svg">vectors</a></sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKd3lqNzBOUTh5Qm8/view?resourcekey=0-PIlUihJ0-lpUmBWd2rkJjQ" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKd3lqNzBOUTh5Qm8&resourcekey=0-PIlUihJ0-lpUmBWd2rkJjQ" width="240" alt="1985 - M523 - 523-06-001 - RERI ILHAH.jpg"></a><br><sub>1985|18 · 523-06-001 - RERI ILHAH · <a href="SCHEMATICS/1985%20-%20M523%20-%20523-06-001%20-%20RERI%20ILHAH%20(EXTRACTED).svg">vectors</a></sub></td></tr>
<tr><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/1zbebYqzI52iCBfLrlgLnFQAelsq0Gb2K/view" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=1zbebYqzI52iCBfLrlgLnFQAelsq0Gb2K" width="240" alt="1985 - M523 - 523-06-001 - STEREO SUBMASTER MODULE COMPONENT LAYOUT.jpg"></a><br><sub>1985|18 · 523-06-001 - STEREO SUBMASTER MODULE COMPONENT LAYOUT · <a href="SCHEMATICS/1985%20-%20M523%20-%20523-06-001%20-%20STEREO%20SUBMASTER%20MODULE%20COMPONENT%20LAYOUT%20(EXTRACTED).svg">vectors</a></sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/1cfQ86lCl7mbfEUWcwERgvMmT3Iw1Dpe3/view" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=1cfQ86lCl7mbfEUWcwERgvMmT3Iw1Dpe3" width="240" alt="1985 - M523 - B 14-077-02-001 - SA14-077 CONTROL ASSEMBLY - SCHEMATIC.jpg"></a><br><sub>1985|18 · B 14-077-02-001 - SA14-077 CONTROL ASSEMBLY - SCHEMATIC · <a href="SCHEMATICS/1985%20-%20M523%20-%20B%2014-077-02-001%20-%20SA14-077%20CONTROL%20ASSEMBLY%20-%20SCHEMATIC%20(EXTRACTED).svg">vectors</a></sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/1eTceHOzl809lUIhtljOssf-8gVsLRk0Z/view" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=1eTceHOzl809lUIhtljOssf-8gVsLRk0Z" width="240" alt="1985 - M523 - B 14-086-02-001 - SA14-086 SUMMING AMPLIFIER ASSEMBLY - SCHEMATIC.jpg"></a><br><sub>1985|18 · B 14-086-02-001 - SA14-086 SUMMING AMPLIFIER ASSEMBLY - SCHEMATIC · <a href="SCHEMATICS/1985%20-%20M523%20-%20B%2014-086-02-001%20-%20SA14-086%20SUMMING%20AMPLIFIER%20ASSEMBLY%20-%20SCHEMATIC%20(EXTRACTED).svg">vectors</a></sub></td></tr>
<tr><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/1BePxTnSCC7-Lxpn2VnKBRm6JUlfM8prf/view" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=1BePxTnSCC7-Lxpn2VnKBRm6JUlfM8prf" width="240" alt="1985 - M523 - B 14-087-02-001 - SA14-087 OUTPUT AMPLIFIER - SCHEMATIC.jpg"></a><br><sub>1985|18 · B 14-087-02-001 - SA14-087 OUTPUT AMPLIFIER - SCHEMATIC · <a href="SCHEMATICS/1985%20-%20M523%20-%20B%2014-087-02-001%20-%20SA14-087%20OUTPUT%20AMPLIFIER%20-%20SCHEMATIC%20(EXTRACTED).svg">vectors</a></sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/1WAQFHI02qLIyI5-unlRXZl0WDdlo7k5W/view" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=1WAQFHI02qLIyI5-unlRXZl0WDdlo7k5W" width="240" alt="1985 - M523 - B 523-01-001 - M523 STEREO SUBMASTER MODULE - FUNCTIONAL.jpg"></a><br><sub>1985|18 · B 523-01-001 - M523 STEREO SUBMASTER MODULE - FUNCTIONAL · <a href="SCHEMATICS/1985%20-%20M523%20-%20B%20523-01-001%20-%20M523%20STEREO%20SUBMASTER%20MODULE%20-%20FUNCTIONAL%20(EXTRACTED).svg">vectors</a></sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/1kgb1q3J1Ic4Wa26Ig4krOF8CbxrQyjSz/view" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=1kgb1q3J1Ic4Wa26Ig4krOF8CbxrQyjSz" width="240" alt="1985 - M523 - B 523-02-001-1 - M523 STEREO SUBMASTER MODULE - SCHEMATIC.jpg"></a><br><sub>1985|18 · B 523-02-001-1 - M523 STEREO SUBMASTER MODULE - SCHEMATIC · <a href="SCHEMATICS/1985%20-%20M523%20-%20B%20523-02-001-1%20-%20M523%20STEREO%20SUBMASTER%20MODULE%20-%20SCHEMATIC%20(EXTRACTED).svg">vectors</a></sub></td></tr>
<tr><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/1VwqPX4F1mlZo5JO8dpfjVSpn8hEvAhEZ/view" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=1VwqPX4F1mlZo5JO8dpfjVSpn8hEvAhEZ" width="240" alt="1985 - M523 - B 523-02-001-2 - M523 STEREO SUBMASTER MODULE - SCHEMATIC.jpg"></a><br><sub>1985|18 · B 523-02-001-2 - M523 STEREO SUBMASTER MODULE - SCHEMATIC · <a href="SCHEMATICS/1985%20-%20M523%20-%20B%20523-02-001-2%20-%20M523%20STEREO%20SUBMASTER%20MODULE%20-%20SCHEMATIC%20(EXTRACTED).svg">vectors</a></sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/1judBEgFFxNF_Pyg8qHFYrrzAO5gDCoFS/view" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=1judBEgFFxNF_Pyg8qHFYrrzAO5gDCoFS" width="240" alt="1985 - M523 - B 523-06-001 - M523 STEREO SUBMASTER MODULE - COMPONENT LAYOUT.jpg"></a><br><sub>1985|18 · B 523-06-001 - M523 STEREO SUBMASTER MODULE - COMPONENT LAYOUT · <a href="SCHEMATICS/1985%20-%20M523%20-%20B%20523-06-001%20-%20M523%20STEREO%20SUBMASTER%20MODULE%20-%20COMPONENT%20LAYOUT%20(EXTRACTED).svg">vectors</a></sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/1W64xAcD7SToSlIe-0pauYkiJcs9PBn7w/view" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=1W64xAcD7SToSlIe-0pauYkiJcs9PBn7w" width="240" alt="1985 - M523 - ST Series - Stereo Submaster Module - 026 - SA14-077 Control Assembly - Component Layout.jpg"></a><br><sub>1985|18 · ST Series - Stereo Submaster Module - 026 - SA14-077 Control Assembly - Component Layout · <a href="SCHEMATICS/1985%20-%20M523%20-%20ST%20Series%20-%20Stereo%20Submaster%20Module%20-%20026%20-%20SA14-077%20Control%20Assembly%20-%20Component%20Layout%20(EXTRACTED).svg">vectors</a></sub></td></tr>
<tr><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/1zvvI15Rx9vjZfhQ661CKeXu5fLh6DOGX/view" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=1zvvI15Rx9vjZfhQ661CKeXu5fLh6DOGX" width="240" alt="1985 - M523 - ST Series - Stereo Submaster Module - 033 - SA14-086 Summing Amp - Component Layout.jpg"></a><br><sub>1985|18 · ST Series - Stereo Submaster Module - 033 - SA14-086 Summing Amp - Component Layout · <a href="SCHEMATICS/1985%20-%20M523%20-%20ST%20Series%20-%20Stereo%20Submaster%20Module%20-%20033%20-%20SA14-086%20Summing%20Amp%20-%20Component%20Layout%20(EXTRACTED).svg">vectors</a></sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/1-50UTAg6hbMLLDbB7awc0Brqqp1gbMVn/view" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=1-50UTAg6hbMLLDbB7awc0Brqqp1gbMVn" width="240" alt="1985 - M523 - ST Series - Stereo Submaster Module - 041 - SA14-087 Output Amp - Component Layout.jpg"></a><br><sub>1985|18 · ST Series - Stereo Submaster Module - 041 - SA14-087 Output Amp - Component Layout · <a href="SCHEMATICS/1985%20-%20M523%20-%20ST%20Series%20-%20Stereo%20Submaster%20Module%20-%20041%20-%20SA14-087%20Output%20Amp%20-%20Component%20Layout%20(EXTRACTED).svg">vectors</a></sub></td></tr>
</table>

Not on Google Drive yet: `19xx - 523-02-001 - STEREO SUBMASTER MODULE SCHEMATIC (2).jpg`, `19xx - 523-02-001 - STEREO SUBMASTER MODULE SCHEMATIC.jpg`

## Pinouts

_Pinouts: the RTO-144 edge connector (connection sheets, connector layouts and rear views, strapping), and the pinout / connections drawings made from them. The module root `RTO.json` lists every contact._

<table>
<tr><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/18Hw7cCBF3BYsFj6oC4aQZ05Z45M3Y4UU/view" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=18Hw7cCBF3BYsFj6oC4aQZ05Z45M3Y4UU" width="240" alt="1985 - M523 - ST Series - Stereo Submaster Module - 013 - p1 Connector pinout.jpg"></a><br><sub>1985|18 · ST Series - Stereo Submaster Module - 013 - p1 Connector pinout · <a href="PINOUTS/1985%20-%20M523%20-%20ST%20Series%20-%20Stereo%20Submaster%20Module%20-%20013%20-%20p1%20Connector%20pinout%20(EXTRACTED).svg">vectors</a></sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/1HAMQtaOloJXOGeX6X971viLpeA1oALji/view" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=1HAMQtaOloJXOGeX6X971viLpeA1oALji" width="240" alt="1985 - M523 - ST Series - Stereo Submaster Module - 014 - p2 Connector pinout.jpg"></a><br><sub>1985|18 · ST Series - Stereo Submaster Module - 014 - p2 Connector pinout · <a href="PINOUTS/1985%20-%20M523%20-%20ST%20Series%20-%20Stereo%20Submaster%20Module%20-%20014%20-%20p2%20Connector%20pinout%20(EXTRACTED).svg">vectors</a></sub></td></tr>
</table>

## RTO-144 pinout

Read from 2 pinout pictures (each its own `.pinout.json` beside it). Every contact, with where it was read: [`RTO.json`](RTO.json). How a picture becomes this table: [the pinout decision tree](https://github.com/WardBeckSystems/WBSps.ca/blob/main/2026/Engineering/PINOUTS.md).

**To check:**

- insert guessed: INSERT PREFADE L/R is a third insert-labelled point, recorded as an output (kind out) because the drawing does not say whether it is a pre-fade send or a second return. (M523: 1985 - M523 - ST Series - Stereo Submaster Module - 013 - p1 Connector pinout.jpg)

**Inserts:** INSERT: INSERT OUT → INSERT IN

| Pin | Signal | Kind | Port | Confidence |
|---|---|---|---|---|
| P1-1 | M1 MONO BUS | bus | M1 MONO | high |
| P1-2 | M1 MONO BUS | bus | M1 MONO | high |
| P1-3 | N/C | nc |  | high |
| P1-4 | N/C | nc |  | high |
| P1-5 | M2 MONO BUS | bus | M2 MONO | high |
| P1-6 | M2 MONO BUS | bus | M2 MONO | high |
| P1-7 | N/C | nc |  | high |
| P1-8 | N/C | nc |  | high |
| P1-9 | M1 LEFT BUS | bus | M1 L | high |
| P1-10 | M1 LEFT BUS | bus | M1 L | high |
| P1-11 | M1 RIGHT BUS | bus | M1 R | high |
| P1-12 | M1 RIGHT BUS | bus | M1 R | high |
| P1-13 | M2 LEFT BUS | bus | M2 L | high |
| P1-14 | M2 LEFT BUS | bus | M2 L | high |
| P1-15 | M2 RIGHT BUS | bus | M2 R | high |
| P1-16 | M2 RIGHT BUS | bus | M2 R | high |
| P1-17 | AUX 4 BUS | bus | AUX 4 | high |
| P1-18 | AUX 4 BUS | bus | AUX 4 | high |
| P1-19 | AUX 3 BUS | bus | AUX 3 | high |
| P1-20 | AUX 3 BUS | bus | AUX 3 | high |
| P1-21 | AUX 2 RIGHT BUS | bus | AUX 2 R | high |
| P1-22 | AUX 2 RIGHT BUS | bus | AUX 2 R | high |
| P1-23 | AUX 2 LEFT BUS | bus | AUX 2 L | high |
| P1-24 | AUX 2 LEFT BUS | bus | AUX 2 L | high |
| P1-25 | AUX 1 RIGHT BUS | bus | AUX 1 R | high |
| P1-26 | AUX 1 RIGHT BUS | bus | AUX 1 R | high |
| P1-27 | AUX 1 LEFT BUS | bus | AUX 1 L | high |
| P1-28 | AUX 1 LEFT BUS | bus | AUX 1 L | high |
| P1-29 | SOLO LEFT BUS | bus | SOLO L | high |
| P1-30 | SOLO LEFT BUS | bus | SOLO L | high |
| P1-31 | SOLO RIGHT BUS | bus | SOLO R | high |
| P1-32 | SOLO RIGHT BUS | bus | SOLO R | high |
| P1-33 | SHIELD | shield |  | high |
| P1-34 | SHIELD | shield |  | high |
| P1-35 | SHIELD | shield |  | high |
| P1-36 | SHIELD | shield |  | high |
| P1-37 | SUMMING INPUT LEFT | in | SUMMING INPUT L | high |
| P1-38 | SUMMING INPUT LEFT | in | SUMMING INPUT L | high |
| P1-39 | SUMMING INPUT RIGHT | in | SUMMING INPUT R | high |
| P1-40 | SUMMING INPUT RIGHT | in | SUMMING INPUT R | high |
| P1-41 | SHIELD | shield |  | high |
| P1-42 | SHIELD | shield |  | high |
| P1-43 | SHIELD | shield |  | high |
| P1-44 | SHIELD | shield |  | high |
| P1-45 | INSERT OUT LEFT | insert_send | INSERT OUT L | high |
| P1-46 | INSERT OUT LEFT | insert_send | INSERT OUT L | high |
| P1-47 | INSERT OUT RIGHT | insert_send | INSERT OUT R | high |
| P1-48 | INSERT OUT RIGHT | insert_send | INSERT OUT R | high |
| P1-49 | INSERT PREFADE LEFT | out | INSERT PREFADE L | high |
| P1-50 | INSERT PREFADE LEFT | out | INSERT PREFADE L | high |
| P1-51 | INSERT PREFADE RIGHT | out | INSERT PREFADE R | high |
| P1-52 | INSERT PREFADE RIGHT | out | INSERT PREFADE R | high |
| P1-53 | INSERT IN LEFT | insert_return | INSERT IN L | high |
| P1-54 | INSERT IN LEFT | insert_return | INSERT IN L | high |
| P1-55 | INSERT IN RIGHT | insert_return | INSERT IN R | high |
| P1-56 | INSERT IN RIGHT | insert_return | INSERT IN R | high |
| P2-1 | MONO DIRECT OUT | out | MONO DIR OUT | high |
| P2-2 | MONO METER OUT | out | MONO METER OUT | high |
| P2-3 | LEFT DIRECT OUT | out | LEFT DIR OUT | high |
| P2-4 | LEFT METER OUT | out | LEFT METER OUT | high |
| P2-5 | RIGHT DIRECT OUT | out | RIGHT DIR OUT | high |
| P2-6 | RIGHT METER OUT | out | RIGHT METER OUT | high |
| P2-7 | N/C | nc |  | high |
| P2-8 | N/C | nc |  | high |
| P2-9 | SHIELD | shield |  | high |
| P2-10 | SHIELD | shield |  | high |
| P2-11 | N/C | nc |  | high |
| P2-12 | RD/NWR | control_in | RD/NWR | high |
| P2-13 | DATA BUS D0 | bus | DATA BUS D0 | high |
| P2-14 | DATA BUS D2 | bus | DATA BUS D2 | high |
| P2-15 | DATA BUS D4 | bus | DATA BUS D4 | high |
| P2-16 | DATA BUS D6 | bus | DATA BUS D6 | high |
| P2-17 | ATTENUATOR SENSE | other | ATTENUATOR SENSE | high |
| P2-18 | N/C | nc |  | high |
| P2-19 | -25 V | power |  | high |
| P2-20 | 25 V COMMON | ground |  | high |
| P2-21 | +25 V | power |  | high |
| P2-22 | CHASSIS | ground |  | high |
| P2-A | MONO DIRECT OUT | out | MONO DIR OUT | high |
| P2-B | MONO METER OUT | out | MONO METER OUT | high |
| P2-C | LEFT DIRECT OUT | out | LEFT DIR OUT | high |
| P2-D | LEFT METER OUT | out | LEFT METER OUT | high |
| P2-E | RIGHT DIRECT OUT | out | RIGHT DIR OUT | high |
| P2-F | RIGHT METER OUT | out | RIGHT METER OUT | high |
| P2-H | N/C | nc |  | high |
| P2-J | N/C | nc |  | high |
| P2-K | SHIELD | shield |  | high |
| P2-L | SHIELD | shield |  | high |
| P2-M | N/C | nc |  | high |
| P2-N | NSEL (SELECT, ACTIVE LOW) | control_in | NSEL | high |
| P2-P | DATA BUS D1 | bus | DATA BUS D1 | high |
| P2-R | DATA BUS D3 | bus | DATA BUS D3 | high |
| P2-S | DATA BUS D5 | bus | DATA BUS D5 | high |
| P2-T | DATA BUS D7 | bus | DATA BUS D7 | high |
| P2-U | N/C | nc |  | high |
| P2-V | CONTROL COMMON | ground |  | high |
| P2-W | N/C | nc |  | high |
| P2-X | 25 V COMMON | ground |  | high |
| P2-Y | +12 V | power |  | high |
| P2-Z | N/C | nc |  | high |

## Manuals and documents

_Manuals and manual pages, price lists, RTO-144 connection sheets, brochures, ads and other document scans._

<table>
<tr><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/1Rc1w5Xn7IPSe5iW8dTywPNdaulgb2XWU/view" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=1Rc1w5Xn7IPSe5iW8dTywPNdaulgb2XWU" width="240" alt="1985 - M523 - ST Series - Stereo Submaster Module - 000.jpg"></a><br><sub>1985|18 · ST Series - Stereo Submaster Module - 000</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/1SLoGYMcFr44flM5ETbrS3NlTCWy-PPle/view" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=1SLoGYMcFr44flM5ETbrS3NlTCWy-PPle" width="240" alt="1985 - M523 - ST Series - Stereo Submaster Module - 001.jpg"></a><br><sub>1985|18 · ST Series - Stereo Submaster Module - 001</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/1sTyxbM1K57SF0pCBudKkUFWWP2oR2bcX/view" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=1sTyxbM1K57SF0pCBudKkUFWWP2oR2bcX" width="240" alt="1985 - M523 - ST Series - Stereo Submaster Module - 002.jpg"></a><br><sub>1985|18 · ST Series - Stereo Submaster Module - 002</sub></td></tr>
<tr><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/1Gg-m_j3D8XGY6PkkFOev4rOq9dRf86_I/view" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=1Gg-m_j3D8XGY6PkkFOev4rOq9dRf86_I" width="240" alt="1985 - M523 - ST Series - Stereo Submaster Module - 003.jpg"></a><br><sub>1985|18 · ST Series - Stereo Submaster Module - 003</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/1C_a3Iwl_4UKHOp1rNsd05j2FLKFuuIAq/view" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=1C_a3Iwl_4UKHOp1rNsd05j2FLKFuuIAq" width="240" alt="1985 - M523 - ST Series - Stereo Submaster Module - 004.jpg"></a><br><sub>1985|18 · ST Series - Stereo Submaster Module - 004</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/1oFIfd_5WpQYUskebix2Vuvf6KEPqhb5E/view" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=1oFIfd_5WpQYUskebix2Vuvf6KEPqhb5E" width="240" alt="1985 - M523 - ST Series - Stereo Submaster Module - 005.jpg"></a><br><sub>1985|18 · ST Series - Stereo Submaster Module - 005</sub></td></tr>
<tr><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/1-oE1jM7amW1cxFwDN7cSHwsBaC0rABID/view" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=1-oE1jM7amW1cxFwDN7cSHwsBaC0rABID" width="240" alt="1985 - M523 - ST Series - Stereo Submaster Module - 006.jpg"></a><br><sub>1985|18 · ST Series - Stereo Submaster Module - 006</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/1l3-8DJy7ubJK900LOOS_3d1bXkbjWo3_/view" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=1l3-8DJy7ubJK900LOOS_3d1bXkbjWo3_" width="240" alt="1985 - M523 - ST Series - Stereo Submaster Module - 007.jpg"></a><br><sub>1985|18 · ST Series - Stereo Submaster Module - 007</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/1tCSTVLvY6PtsiKZDiQr2E7zrZzDDZ-Ki/view" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=1tCSTVLvY6PtsiKZDiQr2E7zrZzDDZ-Ki" width="240" alt="1985 - M523 - ST Series - Stereo Submaster Module - 008.jpg"></a><br><sub>1985|18 · ST Series - Stereo Submaster Module - 008</sub></td></tr>
<tr><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/1H8-JvqDgxJHfEDIukG-fPIgr6VAuSHp7/view" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=1H8-JvqDgxJHfEDIukG-fPIgr6VAuSHp7" width="240" alt="1985 - M523 - ST Series - Stereo Submaster Module - 009.jpg"></a><br><sub>1985|18 · ST Series - Stereo Submaster Module - 009</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/1vQhnWbSOQEiKwkkgY6VkBtkhCd4pgK-J/view" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=1vQhnWbSOQEiKwkkgY6VkBtkhCd4pgK-J" width="240" alt="1985 - M523 - ST Series - Stereo Submaster Module - 010.jpg"></a><br><sub>1985|18 · ST Series - Stereo Submaster Module - 010</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/1IfhrVNwBxMdv8Lbt4_6biWACcPQHxWC9/view" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=1IfhrVNwBxMdv8Lbt4_6biWACcPQHxWC9" width="240" alt="1985 - M523 - ST Series - Stereo Submaster Module - 011.jpg"></a><br><sub>1985|18 · ST Series - Stereo Submaster Module - 011</sub></td></tr>
<tr><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/1kA30oLFs3sL-PdTAfnKv78IlUxkWvU7v/view" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=1kA30oLFs3sL-PdTAfnKv78IlUxkWvU7v" width="240" alt="1985 - M523 - ST Series - Stereo Submaster Module - 012.jpg"></a><br><sub>1985|18 · ST Series - Stereo Submaster Module - 012</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/1I3Hh_7Jsch5uUhQ-qjkFjm5tDZIY9PSI/view" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=1I3Hh_7Jsch5uUhQ-qjkFjm5tDZIY9PSI" width="240" alt="1985 - M523 - ST Series - Stereo Submaster Module - 020.jpg"></a><br><sub>1985|18 · ST Series - Stereo Submaster Module - 020</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/1O24YDE4Rf6Z_3zbbwSF549LX1aLIFcu9/view" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=1O24YDE4Rf6Z_3zbbwSF549LX1aLIFcu9" width="240" alt="1985 - M523 - ST Series - Stereo Submaster Module - 021 - SA14-077 Control Assembly.jpg"></a><br><sub>1985|18 · ST Series - Stereo Submaster Module - 021 - SA14-077 Control Assembly</sub></td></tr>
<tr><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/1tCCeykfkyMyu-QIreqFcwSnCpinwNXap/view" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=1tCCeykfkyMyu-QIreqFcwSnCpinwNXap" width="240" alt="1985 - M523 - ST Series - Stereo Submaster Module - 022 - SA14-077 Control Assembly.jpg"></a><br><sub>1985|18 · ST Series - Stereo Submaster Module - 022 - SA14-077 Control Assembly</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/133JCdyMwvtZz7mD-alDZ8iUoHe-VXuns/view" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=133JCdyMwvtZz7mD-alDZ8iUoHe-VXuns" width="240" alt="1985 - M523 - ST Series - Stereo Submaster Module - 023 - SA14-077 Control Assembly.jpg"></a><br><sub>1985|18 · ST Series - Stereo Submaster Module - 023 - SA14-077 Control Assembly</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/1mpBpjy3HkS-98SSf9Lkik8Ot_KKlfPyq/view" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=1mpBpjy3HkS-98SSf9Lkik8Ot_KKlfPyq" width="240" alt="1985 - M523 - ST Series - Stereo Submaster Module - 024 - SA14-077 Control Assembly.jpg"></a><br><sub>1985|18 · ST Series - Stereo Submaster Module - 024 - SA14-077 Control Assembly</sub></td></tr>
<tr><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/13jWnWyjpibPuCrPKg1BffaGOObQj_aI6/view" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=13jWnWyjpibPuCrPKg1BffaGOObQj_aI6" width="240" alt="1985 - M523 - ST Series - Stereo Submaster Module - 027 - SA14-086 Summing Amp.jpg"></a><br><sub>1985|18 · ST Series - Stereo Submaster Module - 027 - SA14-086 Summing Amp</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/15j_2hXBciZuahkbjMTcvVvSMWj6-WCjb/view" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=15j_2hXBciZuahkbjMTcvVvSMWj6-WCjb" width="240" alt="1985 - M523 - ST Series - Stereo Submaster Module - 028 - SA14-086 Summing Amp.jpg"></a><br><sub>1985|18 · ST Series - Stereo Submaster Module - 028 - SA14-086 Summing Amp</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/1ujJ9Cg3sniRA1XALjfre2RthtPoiVyO1/view" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=1ujJ9Cg3sniRA1XALjfre2RthtPoiVyO1" width="240" alt="1985 - M523 - ST Series - Stereo Submaster Module - 029 - SA14-086 Summing Amp.jpg"></a><br><sub>1985|18 · ST Series - Stereo Submaster Module - 029 - SA14-086 Summing Amp</sub></td></tr>
<tr><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/1NxXLIfeFHi53o5V5ELWg6xHet03WIgy7/view" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=1NxXLIfeFHi53o5V5ELWg6xHet03WIgy7" width="240" alt="1985 - M523 - ST Series - Stereo Submaster Module - 030 - SA14-086 Summing Amp.jpg"></a><br><sub>1985|18 · ST Series - Stereo Submaster Module - 030 - SA14-086 Summing Amp</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/1vnPzGofJ7C5Tjyqve3zfKmLDhrhjP3mG/view" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=1vnPzGofJ7C5Tjyqve3zfKmLDhrhjP3mG" width="240" alt="1985 - M523 - ST Series - Stereo Submaster Module - 031 - SA14-086 Summing Amp.jpg"></a><br><sub>1985|18 · ST Series - Stereo Submaster Module - 031 - SA14-086 Summing Amp</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/1X8IRkE0-Da8jBRRXFTyFjb8X5pzACcA4/view" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=1X8IRkE0-Da8jBRRXFTyFjb8X5pzACcA4" width="240" alt="1985 - M523 - ST Series - Stereo Submaster Module - 034 - SA14-087 Output Amp.jpg"></a><br><sub>1985|18 · ST Series - Stereo Submaster Module - 034 - SA14-087 Output Amp</sub></td></tr>
<tr><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/1Q711DS6qJyn98MRNsIcZyk1bsO8GBYYd/view" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=1Q711DS6qJyn98MRNsIcZyk1bsO8GBYYd" width="240" alt="1985 - M523 - ST Series - Stereo Submaster Module - 035 - SA14-087 Output Amp.jpg"></a><br><sub>1985|18 · ST Series - Stereo Submaster Module - 035 - SA14-087 Output Amp</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/1LQKD2VA6l8daH3C2XrpCwsdU5pZ4aWGq/view" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=1LQKD2VA6l8daH3C2XrpCwsdU5pZ4aWGq" width="240" alt="1985 - M523 - ST Series - Stereo Submaster Module - 036 - SA14-087 Output Amp.jpg"></a><br><sub>1985|18 · ST Series - Stereo Submaster Module - 036 - SA14-087 Output Amp</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/1IztSb1opsedS8jYi2YxP5Cd-jdjKgpcT/view" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=1IztSb1opsedS8jYi2YxP5Cd-jdjKgpcT" width="240" alt="1985 - M523 - ST Series - Stereo Submaster Module - 037 - SA14-087 Output Amp.jpg"></a><br><sub>1985|18 · ST Series - Stereo Submaster Module - 037 - SA14-087 Output Amp</sub></td></tr>
<tr><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/1hmJqLrw5fz_t7WLbdSAPP1GYynxJO8FP/view" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=1hmJqLrw5fz_t7WLbdSAPP1GYynxJO8FP" width="240" alt="1985 - M523 - ST Series - Stereo Submaster Module - 038 - SA14-087 Output Amp.jpg"></a><br><sub>1985|18 · ST Series - Stereo Submaster Module - 038 - SA14-087 Output Amp</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/1R1dva-PNSCv_ie9BvLN7J2wflVR6DP8o/view" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=1R1dva-PNSCv_ie9BvLN7J2wflVR6DP8o" width="240" alt="1985 - M523 - ST Series - Stereo Submaster Module - 039 - SA14-087 Output Amp.jpg"></a><br><sub>1985|18 · ST Series - Stereo Submaster Module - 039 - SA14-087 Output Amp</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKRk9uUUFMSHN6NWs/view?resourcekey=0-lJj9wE69ZJbzM-_k_6va0A" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKRk9uUUFMSHN6NWs&resourcekey=0-lJj9wE69ZJbzM-_k_6va0A" width="240" alt="19xx - M523 - AD - WBSPS - AD - LS series 003.jpg"></a><br><sub>19xx - M523 - AD - WBSPS - AD - LS series 003</sub></td></tr>
<tr><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKbFk3ZWlfQTQxdHc/view?resourcekey=0-HhWPKcg7Ls5SELA1psGokQ" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKbFk3ZWlfQTQxdHc&resourcekey=0-HhWPKcg7Ls5SELA1psGokQ" width="240" alt="19xx - M523 - DOC - 004.jpg"></a><br><sub>19xx - M523 - DOC - 004</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKaVExUlNPcU5VTkk/view?resourcekey=0-99-0K0XkkijrSRAOK8Vz1w" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKaVExUlNPcU5VTkk&resourcekey=0-99-0K0XkkijrSRAOK8Vz1w" width="240" alt="19xx - M523 - DOC - 007.jpg"></a><br><sub>19xx - M523 - DOC - 007</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKTUx2eG9mNEE3Zmc/view?resourcekey=0-woHDC3XPEimdNHPuO4pvwQ" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKTUx2eG9mNEE3Zmc&resourcekey=0-woHDC3XPEimdNHPuO4pvwQ" width="240" alt="19xx - M523 - DOC - 019.jpg"></a><br><sub>19xx - M523 - DOC - 019</sub></td></tr>
<tr><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKbkZZRmp3d3Q1RmM/view?resourcekey=0-MnZxtyDRE4JjGML6hHU65w" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKbkZZRmp3d3Q1RmM&resourcekey=0-MnZxtyDRE4JjGML6hHU65w" width="240" alt="19xx - M523 - DOC - 032.jpg"></a><br><sub>19xx - M523 - DOC - 032</sub></td></tr>
</table>

## KiCad

_KiCad: a schematic (`.kicad_sch`) traced from each electrical drawing, the module symbol (`.kicad_sym`) and its PCB projects. Traced schematics are the line work only: redraw with symbols over them._

- [1985 - M523 - 523-02-001 - AICHT SOLO QUTPUT WES (2).kicad_sch](KICAD/1985%20-%20M523%20-%20523-02-001%20-%20AICHT%20SOLO%20QUTPUT%20WES%20(2).kicad_sch)
- [1985 - M523 - 523-02-001 - AICHT SOLO QUTPUT WES.kicad_sch](KICAD/1985%20-%20M523%20-%20523-02-001%20-%20AICHT%20SOLO%20QUTPUT%20WES.kicad_sch)
- [1985 - M523 - B 14-077-02-001 - SA14-077 CONTROL ASSEMBLY - SCHEMATIC.kicad_sch](KICAD/1985%20-%20M523%20-%20B%2014-077-02-001%20-%20SA14-077%20CONTROL%20ASSEMBLY%20-%20SCHEMATIC.kicad_sch)
- [1985 - M523 - B 14-086-02-001 - SA14-086 SUMMING AMPLIFIER ASSEMBLY - SCHEMATIC.kicad_sch](KICAD/1985%20-%20M523%20-%20B%2014-086-02-001%20-%20SA14-086%20SUMMING%20AMPLIFIER%20ASSEMBLY%20-%20SCHEMATIC.kicad_sch)
- [1985 - M523 - B 14-087-02-001 - SA14-087 OUTPUT AMPLIFIER - SCHEMATIC.kicad_sch](KICAD/1985%20-%20M523%20-%20B%2014-087-02-001%20-%20SA14-087%20OUTPUT%20AMPLIFIER%20-%20SCHEMATIC.kicad_sch)
- [1985 - M523 - B 523-01-001 - M523 STEREO SUBMASTER MODULE - FUNCTIONAL.kicad_sch](KICAD/1985%20-%20M523%20-%20B%20523-01-001%20-%20M523%20STEREO%20SUBMASTER%20MODULE%20-%20FUNCTIONAL.kicad_sch)
- [1985 - M523 - B 523-02-001-1 - M523 STEREO SUBMASTER MODULE - SCHEMATIC.kicad_sch](KICAD/1985%20-%20M523%20-%20B%20523-02-001-1%20-%20M523%20STEREO%20SUBMASTER%20MODULE%20-%20SCHEMATIC.kicad_sch)
- [1985 - M523 - B 523-02-001-2 - M523 STEREO SUBMASTER MODULE - SCHEMATIC.kicad_sch](KICAD/1985%20-%20M523%20-%20B%20523-02-001-2%20-%20M523%20STEREO%20SUBMASTER%20MODULE%20-%20SCHEMATIC.kicad_sch)
- [19xx - 523-02-001 - STEREO SUBMASTER MODULE SCHEMATIC (2).kicad_sch](KICAD/19xx%20-%20523-02-001%20-%20STEREO%20SUBMASTER%20MODULE%20SCHEMATIC%20(2).kicad_sch)
- [19xx - 523-02-001 - STEREO SUBMASTER MODULE SCHEMATIC.kicad_sch](KICAD/19xx%20-%20523-02-001%20-%20STEREO%20SUBMASTER%20MODULE%20SCHEMATIC.kicad_sch)
- [M523.kicad_sym](KICAD/M523.kicad_sym)
- [index.html](KICAD/index.html)

---
Archive: Anthony Peter Kuzub · [WBSps.ca](https://WBSps.ca) · [WBSps.Kuzub.com](https://WBSps.Kuzub.com)
