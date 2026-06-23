<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Zooming Into The School of Athens</title>
  <meta name="description" content="A classroom applet that zooms into Raphael's School of Athens to reveal Plato and Aristotle near the vanishing point.">
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <main class="app">
    <section class="hero">
      <div>
        <p class="eyebrow">Perspective and philosophy</p>
        <h1>Zoom Into the Vanishing Point</h1>
        <p class="lede">Students explore Raphael's <i>The School of Athens</i> by zooming toward the central vanishing point. As the architecture converges, Plato and Aristotle become the focus.</p>
      </div>
      <aside class="readout" aria-live="polite">
        <span>Zoom level</span>
        <strong id="zoomReadout">1.0x</strong>
        <em id="stageReadout">Full fresco view</em>
      </aside>
    </section>

    <section class="viewer-panel">
      <div class="viewer-toolbar">
        <label for="zoomSlider">
          Zoom toward the vanishing point
          <input id="zoomSlider" type="range" min="1" max="8" step="0.01" value="1">
        </label>
        <div class="buttons">
          <button type="button" data-zoom="1">Full view</button>
          <button type="button" data-zoom="2.6">Find the lines</button>
          <button type="button" data-zoom="5.2">Approach center</button>
          <button type="button" data-zoom="8">Reveal Plato and Aristotle</button>
        </div>
      </div>

      <div class="viewer lines-hidden" id="viewer">
        <div class="painting-layer" id="paintingLayer">
          <img id="painting" alt="Raphael's The School of Athens" src="assets/school-of-athens.jpg">
          <svg class="overlay" viewBox="0 0 1920 1339" preserveAspectRatio="none" aria-hidden="true">
            <g id="perspectiveLines">
              <line x1="115" y1="1195" x2="1000" y2="815"></line>
              <line x1="555" y1="1195" x2="1000" y2="815"></line>
              <line x1="935" y1="1295" x2="1000" y2="815"></line>
              <line x1="1350" y1="1195" x2="1000" y2="815"></line>
              <line x1="1810" y1="1195" x2="1000" y2="815"></line>
              <line x1="420" y1="690" x2="1000" y2="815"></line>
              <line x1="1490" y1="690" x2="1000" y2="815"></line>
            </g>
            <circle id="vanishingPoint" cx="1000" cy="815" r="18"></circle>
            <text x="1035" y="790">vanishing point</text>
          </svg>
          <div class="person-label plato">Plato</div>
          <div class="person-label aristotle">Aristotle</div>
        </div>
      </div>

      <div class="caption-row">
        <p id="prompt">Start with the whole painting. What architectural lines seem to point toward the center?</p>
        <button type="button" id="toggleLines">Show guide lines</button>
      </div>
    </section>

    <section class="lesson-grid">
      <article>
        <h2>What Students Should Notice</h2>
        <ul>
          <li>The ceiling, floor, and walls create a one-point perspective system.</li>
          <li>The lines converge near the center of the composition.</li>
          <li>Plato and Aristotle stand close to that visual focus.</li>
          <li>Perspective is being used to organize attention, not just space.</li>
        </ul>
      </article>
      <article>
        <h2>Discussion Prompt</h2>
        <p id="discussion">Why might Raphael place Plato and Aristotle near the visual center of the painting?</p>
      </article>
      <article>
        <h2>Deploy Notes</h2>
        <p>This app is static HTML, CSS, and JavaScript. Upload the files to a GitHub repository root and enable GitHub Pages.</p>
      </article>
    </section>
  </main>

  <script src="script.js"></script>
</body>
</html>
