# Workplace Monitor — React Presentation

Frontend-only React presentation based on the supplied IMRAD. No backend, API keys, sensor connection or paid services are required.

## Present immediately, offline

Extract the ZIP, then double-click **OPEN_PRESENTATION.html** in Chrome, Edge or Firefox. This single file embeds the React app, stylesheet and Blynk screenshot. No installation or internet is required. Website reference links need internet.

## Updated presentation

- 13 slides, ending with “We will now demonstrate the actual project.”
- No separate Demo tab, demo steps or checklists.
- References lists only the five website sources in IEEE style.
- Each slide has its own transition and staged content animation.
- Cover: cinematic reveal and unfolding system diagram.
- Environmental conditions: staggered perspective reveals.
- Objectives: sequential row reveals.
- Architecture: sensors, controller and outputs appear in order, with moving signal paths.
- Processing: an illustrative noisy-to-stable signal trace draws before the explanations.
- Risk: levels rise sequentially and cumulative LEDs light in order.
- Normal results: recorded metrics come into focus, followed by the output summary.
- Test results: rows sweep in with a brief highlight.
- MQ-135: recorded recovery stages reveal in sequence.
- Blynk: the actual screenshot reveals with a perspective transition.
- Limitations: the two explanations arrive from opposite sides.
- Conclusion: a focus reveal leads into the demonstration.
- Demonstration: a curtain-style reveal with a simple announcement.

All numerical values are documented static observations, not live sensor readings. The filtering trace is an illustration, not measured data.

## Controls

- Left / Right arrows, Page Up / Page Down, or Space: navigate.
- Home / End: first / final slide.
- F: fullscreen (or use the browser fullscreen command).
- N: toggle presenter notes. They appear on the same screen and will be visible to the audience.
- G: slide overview. Escape closes it.
- R or Replay: replay the current slide's animation sequence.
- Motion on/off: enable or reduce animation. The initial setting respects your device's reduced-motion preference. Clicking Replay explicitly enables motion.
- On-screen controls also work with touch.

Allow about 2–4 seconds for the staged content on each slide to finish revealing. Content remains visible after the sequence. Transitions do not advance slides automatically.

## Edit the React source

Install Node.js 22.12 or later, then run from this folder:

```sh
npm ci
npm run dev
```

Vite prints the local address. The first dependency installation requires internet. The application itself has no network dependency.

After editing:

```sh
npm run build
node scripts/standalone.mjs
```

`dist/` contains the static build. The second command updates the offline HTML file. Edit slide copy and citations in `src/content.js`, React layouts in `src/main.jsx`, and visual styles and animations in `src/style.css`.

## Sources and verification

Content follows the supplied `Group#-CSELECT3_MIDTERMS (1).pdf`. The image is the actual Figure 2 Blynk screenshot. Earlier V4.1.5 MQ-135 observations remain distinguished from the final V4.1.6 recovery design. The IMRAD recommends a final V4.1.6 recovery regression check. Website citations use the bibliographic details reported in the IMRAD.

The production build and offline package were checked. Interactive browser preview was blocked in the authoring environment, so browser rendering and animation timing could not be visually verified there.
