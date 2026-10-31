# Alto Cirra Seeding Go/No-Go Dashboard

A single-page decision tool for winter cloud seeding operations near Woodward Park City, Utah. It walks an operator through five decision gates and shows whether conditions support seeding, need watching, or rule it out.

**Live demo:** _add your GitHub Pages link here_

## What it does

- **Five gates:** model candidates, soundings, radar, surface sites, and uncrewed aircraft measurements. Each criterion is scored Pass, Watch or Fail, and the overall status is No-go if any criterion fails, Go only if all pass, and Hold otherwise.
- **Storm replay:** choose one of three 2025 Wasatch storms (Jan 1-2, Mar 17-18, Dec 4-7) and scrub through time to watch the gates change as the storm crosses the site.
- **Forecast briefing:** an hourly grid shows which hours are seedable, marginal or unsuitable, with the best window outlined.
- **Justification for every criterion:** each row has a dropdown giving the reason for its pass range and how the value would be measured, with numbered links to the source list at the bottom.

## Using it

1. Pick a storm in the left rail.
2. Press Play or drag the time slider.
3. Click a gate to see its criteria. Values can also be adjusted by hand.
4. Open **Justification** under any criterion for the range and measurement notes.

## About the data and ranges

- Storm names, dates and snowfall come from National Weather Service alerts.
- The hourly values are **reconstructed profiles** shaped to each storm's character, not archived model, sounding or radar data. Surface temperature, Froude number and radar values are derived from those profiles.
- Where a published criterion exists (for example Utah operator limits, the atmospheric river scale, the rain-snow temperature threshold), the range follows it and is cited. Where none was found, the justification says so and gives a reasonable range instead. Those values are starting points to calibrate against operational data.
- Not covered: natural ice concentration, low-level inversions, and hard stops such as permits, airspace, snowpack and flood limits.

## Files

- `index.html` is the whole application (HTML, CSS and JavaScript, no build step). It loads the Archivo font from Google Fonts.

## Running locally

Open `index.html` in a browser.
