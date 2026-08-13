# ViSR Demonstration Guide

**Audience:** Communications / outreach staff running visitor demonstrations


| | |
|---|---|
| **Version** | `[X.Y]` |
| **Last updated** | `[DATE]` |
| **Owner** | `[NAME / TEAM]` |
| **Beamline / lab** | `[LOCATION]` |
| **Contact** | `[NAME, EXT]` |


---

## Contents

1. [Introduction and setup](#1-introduction-and-setup)
2. [Spectroscopy](#2-spectroscopy)
3. [Tomography](#3-tomography)
4. [Manual experiments — diffraction](#4-manual-experiments--diffraction)
5. [Appendix](#5-appendix)


---

## 1. Introduction and setup

### 1.1 What the demonstration is

[PARAGRAPH: One or two paragraphs setting the scene for the demonstrator — what the facility does, why these three experiments were chosen, and the story arc you're taking visitors through (automated measurement → automated 3D imaging → hands-on physics). Written so a demonstrator can paraphrase it as an opening line to a group.]

| Part | Experiment | Mode | Approx. duration | Visitor involvement |
|---|---|---|---|---|
| 1 | Spectroscopy | Automated | `[TBC]` min | Watch / discuss |
| 2 | Tomography | Automated | `[TBC]` min | Watch / discuss |
| 3 | Diffraction optics | Manual | `[TBC]` min | Hands-on |

[IMAGE: Annotated overview photo or schematic of the lab showing the automated branch, the manual branch, and where visitors stand.]

### 1.2 Before you start

[PARAGRAPH: Access requirements, training sign-off, PPE, who to notify that you're using the lab, and the rule about never running a demo alone / never running with an unfamiliar setup.]

**Safety notes** — full detail in *→ Appendix E*.

- `[TBC — laser class and control measures for the manual branch]`
- `[TBC — radiation / enclosure interlocks for the automated branch]`
- `[TBC — visitor boundary lines and supervision ratio]`

### 1.3 Opening the GUIs from the launcher

[PARAGRAPH: What the launcher is, where to find it (desktop icon / terminal command), and the principle that everything should be started from the launcher rather than by hand so that the correct environment and configuration are picked up.]

1. Open the launcher: `[TBC — command or icon]`
2. Start the following, in this order:
   | Order | GUI | Launcher entry | What it's for |
   |---|---|---|---|
   | 1 | `[TBC]` | `[TBC]` | Overall status / synoptic |
   | 2 | `[TBC]` | `[TBC]` | Spectroscopy control |
   | 3 | `[TBC]` | `[TBC]` | Tomography control |
   | 4 | `[TBC]` | `[TBC]` | Detector / camera view |
   | 5 | `[TBC]` | `[TBC]` | Data viewer |
3. Arrange the windows across the screens as shown below.

[IMAGE: Screenshot of the launcher with the required entries highlighted.]

[IMAGE: Screenshot of the expected final desktop layout across both/all monitors.]

> If a GUI fails to open, closes immediately, or opens with blank/greyed fields → **Appendix A1**.

### 1.4 Checking alignment on the manual branch

[PARAGRAPH: Short explanation of why alignment is checked first — it's the quickest way to confirm the source and optics are behaving, and it's the part visitors get closest to. Emphasise this is a *check*, not a realignment; realignment is a separate procedure.]

1. `[TBC — step]`
2. `[TBC — step]`
3. `[TBC — step]`

**Pass criteria:** `[TBC — e.g. beam centred on target within X mm, spot round and of expected size, intensity reading in range Y–Z]`

[IMAGE: Photo of a correctly aligned beam on the alignment target, ideally next to a misaligned example for comparison.]

> Alignment out of tolerance, drifting, or unrecoverable → **Appendix A2**. Full realignment procedure → **Appendix B**.

### 1.5 Checking the IOCs

[PARAGRAPH: One short paragraph explaining what an IOC is in plain terms — the piece of software that talks to a given bit of hardware — and why a demo fails in confusing ways if one is down. Keep it non-technical; the deeper explanation goes in the appendix.]

1. Open `[TBC — status / synoptic screen]`
2. Confirm every entry in the table below reads **green / OK**.
3. Confirm live values are *updating*, not frozen — a stale value can look healthy.

| IOC | Controls | Healthy indication |
|---|---|---|
| `[TBC]` | `[TBC]` | `[TBC]` |
| `[TBC]` | `[TBC]` | `[TBC]` |
| `[TBC]` | `[TBC]` | `[TBC]` |
| `[TBC]` | `[TBC]` | `[TBC]` |

[IMAGE: Screenshot of the status screen in a fully healthy state, with the key indicators circled.]

> Any IOC red, amber, disconnected or frozen → **Appendix A3**. What an IOC actually is and how restarts work → **Appendix C**.

### 1.6 Dry run

[PARAGRAPH: Why you always run each automated experiment once before visitors arrive — it warms up hardware, confirms the data path end to end, and gives you a known-good result to fall back on if the live run misbehaves.]

- [ ] Run spectroscopy once with the standard demo sample *(→ Section 2)*. Confirm a spectrum appears **and** the file is written to `[TBC — path]`.
- [ ] Run tomography once with the standard demo sample *(→ Section 3)*. Confirm the reconstruction completes and displays.
- [ ] Set out and test the diffraction optics *(→ Section 4)*. Confirm a clean pattern on the screen.
- [ ] Save or note the location of the dry-run data as a backup demo. *(→ Appendix D)*

### 1.7 Setup sign-off

[PARAGRAPH: Short note on logging the setup — where to record that checks were completed, any faults raised, and handover if a different person is running the demo.]

| Check | Signed | Time |
|---|---|---|
| GUIs launched | | |
| Alignment verified | | |
| IOCs green | | |
| Dry runs complete | | |

---

## 2. Spectroscopy

### 2.1 What the experiment is

[PARAGRAPH: Plain-language explanation of spectroscopy for the demonstrator to adapt for visitors — measuring how a sample absorbs or emits across a range of energies/wavelengths, and what that tells you about the material. Include one memorable analogy and one real-world application.]

[IMAGE: Simple schematic — source → sample → detector → spectrum.]

**Talking points**

- `[TBC — what visitors are actually looking at on screen]`
- `[TBC — a "why does this matter" hook]`
- `[TBC — a good question to ask the group]`

**Common visitor questions** → **Appendix F1**

### 2.2 Running the experiment

1. In `[TBC — GUI name]`, select the demo configuration `[TBC]`.
2. Confirm the sample is loaded and the correct sample position is selected *(→ 2.3)*.
3. Check the scan parameters against the table below.
4. Press **`[TBC — start button]`**.
5. Watch the live plot build. Expected run time: `[TBC]` minutes.
6. When complete, confirm the data has saved to `[TBC — path]`.

| Parameter | Demo value | Note |
|---|---|---|
| `[TBC]` | `[TBC]` | Do not change |
| `[TBC]` | `[TBC]` | Shorten if running behind |
| `[TBC]` | `[TBC]` | |

[IMAGE: Screenshot of the spectroscopy GUI with the start control and key parameter fields annotated.]

[IMAGE: Example of a good result — a clean spectrum with the interesting feature labelled.]

> Scan won't start, aborts, or the spectrum looks wrong → **Appendix A4**.

### 2.3 Changing samples

[PARAGRAPH: When and why you'd swap samples during a demo — showing contrast between two materials is usually the strongest moment. Note anything about handling, contamination, or letting visitors hold samples.]

1. Confirm no scan is running.
2. `[TBC — safe state / interlock step before opening]`
3. `[TBC — physical swap step]`
4. `[TBC — update sample position / metadata in GUI]`
5. `[TBC — close up and confirm ready state]`

**Demo sample set**

| Sample | Position | Why it's interesting | Expected feature |
|---|---|---|---|
| `[TBC]` | `[TBC]` | `[TBC]` | `[TBC]` |
| `[TBC]` | `[TBC]` | `[TBC]` | `[TBC]` |
| `[TBC]` | `[TBC]` | `[TBC]` | `[TBC]` |

[IMAGE: Photo of the sample holder with positions numbered.]

> Sample not detected, or the wrong sample appears in the data → **Appendix A5**.

---

## 3. Tomography

### 3.1 What the experiment is

[PARAGRAPH: Plain-language explanation — taking many projections as the sample rotates and computationally reconstructing a 3D volume. The medical CT comparison is the obvious hook; note what makes this version different (resolution, sample type, speed).]

[IMAGE: Schematic — sample rotating between source and detector, plus the projection → sinogram → reconstruction chain.]

**Talking points**

- `[TBC — the CT scanner comparison, and where it breaks down]`
- `[TBC — what the 3D volume is actually used for]`
- `[TBC — the "slice through it live" moment, if available]`

**Common visitor questions** → **Appendix F2**

### 3.2 Running the experiment

1. In `[TBC — GUI name]`, select the demo configuration `[TBC]`.
2. Confirm the sample is mounted and centred on the rotation axis. *(Centring check → Appendix G)*
3. Confirm flat-field and dark-field references are current, or acquire new ones: `[TBC]`.
4. Check the scan parameters below.
5. Press **`[TBC — start button]`**.
6. Projections will stream during acquisition (`[TBC]` min), then reconstruction runs automatically (`[TBC]` min).
7. Open the result in `[TBC — viewer]` and step through the slices.

| Parameter | Demo value | Note |
|---|---|---|
| Number of projections | `[TBC]` | Reduce for a faster demo |
| Exposure | `[TBC]` | |
| Rotation range | `[TBC]` | |
| Reconstruction preset | `[TBC]` | |

[IMAGE: Screenshot of the tomography GUI mid-acquisition.]

[IMAGE: Example reconstruction — a good slice and a 3D rendering side by side.]

> Reconstruction fails, looks streaky, blurred or doubled → **Appendix A6**. Sample not centred → **Appendix G**.

---

## 4. Manual experiments — diffraction

### 4.1 What the experiments are

[PARAGRAPH: Plain-language explanation of diffraction and interference — light bending around obstacles and adding up to make patterns, and how the pattern encodes the size and spacing of what it passed through. Link it explicitly back to Sections 2 and 3 so the demo feels like one story: this is the hands-on version of the physics the big instruments rely on.]

[IMAGE: Photo of the manual optics bench laid out for the demo, components labelled.]

**Safety — read before every session**

- `[TBC — laser class, never look into the beam, beam height rule]`
- `[TBC — who may touch what; visitor boundary]`
- `[TBC — what to do if the beam is misdirected]`

Full safety detail → **Appendix E**.

### 4.2 Setting up the bench

1. `[TBC — mount and power the source]`
2. `[TBC — set beam height / levelling]`
3. `[TBC — position the slide holder at distance X]`
4. `[TBC — position the screen at distance Y]`
5. `[TBC — darken the room to the required level]`

[IMAGE: Diagram with the standard distances between source, sample and screen marked.]

### 4.3 The demonstrations

Run these in order — each one builds on the last.

| # | Demo | Optic used | What visitors see | Time |
|---|---|---|---|---|
| 1 | Single slit | `[TBC]` | `[TBC]` | `[TBC]` |
| 2 | Double slit | `[TBC]` | `[TBC]` | `[TBC]` |
| 3 | Grating | `[TBC]` | `[TBC]` | `[TBC]` |
| 4 | `[TBC — e.g. mesh / 2D aperture / hair]` | `[TBC]` | `[TBC]` | `[TBC]` |

**For each demo:**

1. Insert the optic in the holder.
2. `[TBC — adjust to centre the pattern]`
3. Point out the feature to look for: `[TBC]`
4. Ask the group: `[TBC — the question that leads into the next demo]`

[IMAGE: Gallery of the expected patterns, one per demo, for comparison against what's on the screen.]

**Letting visitors take part**

[PARAGRAPH: What visitors are allowed to do themselves — swapping slides, moving the screen, measuring fringe spacing — and how to keep that safe and quick with a group. Include the fallback if the group is too large or too young.]

> Pattern faint, smeared, doubled or absent → **Appendix A7**.

---

## 5. Appendix

### A. Troubleshooting

Ordered by where it goes wrong. Each entry: symptom → likely cause → what to do → who to call if that fails.

#### A1. GUIs and the launcher

| Symptom | Likely cause | Action |
|---|---|---|
| Launcher won't open | `[TBC]` | `[TBC]` |
| GUI opens then closes immediately | `[TBC]` | `[TBC]` |
| Fields blank, greyed or showing `[TBC — disconnected marker]` | `[TBC]` | `[TBC]` |
| GUI unresponsive / frozen | `[TBC]` | `[TBC]` |
| Wrong configuration loaded | `[TBC]` | `[TBC]` |

[PARAGRAPH: Note on the safe way to restart a GUI mid-session, and what state is and isn't preserved.]

#### A2. Alignment

| Symptom | Likely cause | Action |
|---|---|---|
| No beam on target | `[TBC]` | `[TBC]` |
| Beam present but off-centre | `[TBC]` | `[TBC]` |
| Spot distorted or larger than expected | `[TBC]` | `[TBC]` |
| Intensity low | `[TBC]` | `[TBC]` |
| Alignment drifts during the session | `[TBC]` | `[TBC]` |

**When to stop and call for help:** `[TBC]`

#### A3. IOCs

| Symptom | Likely cause | Action |
|---|---|---|
| IOC red / disconnected | `[TBC]` | `[TBC]` |
| Values frozen but IOC appears green | `[TBC]` | `[TBC]` |
| Motor reports a position that's obviously wrong | `[TBC]` | `[TBC]` |
| IOC restarts but doesn't reconnect | `[TBC]` | `[TBC]` |

**Restart procedure:** `[TBC — exact commands or GUI actions, and the order to do them in]`
**Never restart:** `[TBC — list of IOCs that must only be touched by staff, and why]`

#### A4. Spectroscopy

| Symptom | Likely cause | Action |
|---|---|---|
| Scan won't start | `[TBC]` | `[TBC]` |
| Scan aborts partway | `[TBC]` | `[TBC]` |
| Spectrum flat / no signal | `[TBC]` | `[TBC]` |
| Spectrum noisy | `[TBC]` | `[TBC]` |
| Features in the wrong place | `[TBC]` | `[TBC]` |
| Data not written to disk | `[TBC]` | `[TBC]` |

#### A5. Samples

| Symptom | Likely cause | Action |
|---|---|---|
| Sample not detected | `[TBC]` | `[TBC]` |
| Wrong sample recorded in metadata | `[TBC]` | `[TBC]` |
| Sample dropped, damaged or contaminated | `[TBC]` | `[TBC]` |

#### A6. Tomography

| Symptom | Likely cause | Action |
|---|---|---|
| Acquisition stalls | `[TBC]` | `[TBC]` |
| Reconstruction fails to launch | `[TBC]` | `[TBC]` |
| Ring artefacts | `[TBC]` | `[TBC]` |
| Streaks / doubled edges | `[TBC]` | `[TBC]` |
| Blurred reconstruction | `[TBC]` | `[TBC]` |
| Rotation stage won't home | `[TBC]` | `[TBC]` |

[IMAGE: Side-by-side examples of the common artefacts, labelled, so demonstrators can diagnose by eye.]

#### A7. Manual optics

| Symptom | Likely cause | Action |
|---|---|---|
| No pattern on screen | `[TBC]` | `[TBC]` |
| Pattern very faint | `[TBC]` | `[TBC]` |
| Pattern smeared or asymmetric | `[TBC]` | `[TBC]` |
| Extra unexpected spots | `[TBC]` | `[TBC]` |
| Source won't power on | `[TBC]` | `[TBC]` |

---

### B. Sample mounting and centring

[PARAGRAPH: Detailed guidance on mounting samples for tomography, checking the sample is on the rotation axis, and correcting it if not — the single most common cause of a poor reconstruction.]

[IMAGE: Well-centred vs off-centre sample, with the resulting reconstructions beside each.]

---

### C, D, E...

---

### X. Contacts

| Situation | Contact | Hours |
|---|---|---|
| Controls / IOC problems | `[TBC]` | `[TBC]` |
| Optics and alignment | `[TBC]` | `[TBC]` |
| Samples | `[TBC]` | `[TBC]` |
| Safety incident | `[TBC]` | 24/7 |
| Guide corrections | `[TBC]` | — |

---

### Y. Change log

| Version | Date | Author | Change |
|---|---|---|---|
| `[X.Y]` | `[DATE]` | `[NAME]` | Initial draft |