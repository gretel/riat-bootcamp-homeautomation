# RIAT Bootcamp — Home Automation

Marp slide deck for the **Home Automation** session at
[RIAT Bootcamp](https://riat.at).

A case study in open-source governance, sustainability, and local-first
design — tracing Home Assistant and ESPHome from their origins through
Nabu Casa, the Open Home Foundation, and the broader ecosystem.

## Deck

[**View slides**](https://gretel.github.io/riat-bootcamp-homeautomation/) · 
[PDF](https://gretel.github.io/riat-bootcamp-homeautomation/slides.pdf)

### Topics

- What is Home Assistant? What is ESPHome?
- Cloud vs local-first architecture
- History: founding, the Revolv incident, the Wink paywall
- Otto Winter and the ESPHome origin story
- Nabu Casa, the acquisition, and the Open Home Foundation
- Reverse engineering, standards (Matter), and scale
- Discussion hooks

## Build

```bash
npm install -g @marp-team/marp-cli
marp --no-stdin --html slides.md -o index.html
```

Deployed via GitHub Actions → GitHub Pages.
