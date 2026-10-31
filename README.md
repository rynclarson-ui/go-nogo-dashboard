# Alto Cirra Seeding Go/No-Go Dashboard

Decision tool for winter cloud seeding operations near Woodward Park City, Utah. It walks an operator through five decision gates and shows whether conditions support seeding.

**Live demo:** https://rynclarson-ui.github.io/go-nogo-dashboard/

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
- Where a published criterion exists, the range follows it and is cited. Where none was found, the justification says so and gives a reasonable range instead. 

## Files

- `index.html` is the whole application (HTML, CSS and JavaScript, no build step). It loads the Archivo font from Google Fonts.

## Running locally

Open `index.html` in a browser.
