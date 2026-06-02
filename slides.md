---
marp: true
author: 'Tom Hensel'
theme: default
size: 16:9
paginate: true
header: '![height:28px right](https://riat.at/wp-content/uploads/2023/11/RIAT-1-300x176.png)'
footer: 'RIAT Bootcamp — Home Automation — Tom Hensel'
style: |
  @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap');

  section {
    background: #ffffff;
    color: #000000;
    font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
    font-size: 22px;
    line-height: 1.5;
    padding: 70px 90px;
    letter-spacing: -0.01em;
  }

  section::after {
    color: #000;
    font-size: 11px;
    font-weight: 500;
  }

  header {
    right: 30px;
    top: 24px;
  }

  footer {
    left: 30px;
    bottom: 18px;
    color: #000;
    font-size: 11px;
    font-weight: 500;
    letter-spacing: 0.04em;
    text-transform: uppercase;
  }

  h1 {
    font-size: 56px;
    font-weight: 800;
    letter-spacing: -0.03em;
    line-height: 1.05;
    margin: 0 0 24px 0;
    color: #000;
  }

  h2 {
    font-size: 36px;
    font-weight: 700;
    letter-spacing: -0.02em;
    line-height: 1.15;
    border-bottom: 2px solid #000;
    padding-bottom: 10px;
    margin: 0 0 20px 0;
    color: #000;
  }

  h3 {
    font-size: 22px;
    font-weight: 600;
    letter-spacing: -0.01em;
    text-transform: uppercase;
    margin: 16px 0 8px 0;
    color: #000;
  }

  p { margin: 0 0 14px 0; }

  strong { font-weight: 700; }
  em { font-style: italic; font-weight: 400; }

  ul, ol { margin: 0 0 14px 0; padding-left: 1.4em; }
  li { margin-bottom: 8px; }
  li::marker { color: #000; font-weight: 600; }

  code {
    background: #f2f2f2;
    color: #000;
    font-family: 'SF Mono', Menlo, monospace;
    font-size: 0.78em;
    padding: 2px 6px;
    border-radius: 3px;
    border: 1px solid #e0e0e0;
  }

  pre {
    background: #fafafa;
    border: 1px solid #000;
    border-radius: 4px;
    padding: 18px 22px;
    margin: 12px 0;
  }

  pre code {
    background: transparent;
    border: 0;
    padding: 0;
    font-size: 0.72em;
    line-height: 1.55;
  }

  table {
    width: 100%;
    border-collapse: collapse;
    margin: 12px 0;
    font-size: 0.82em;
  }

  th {
    background: #000;
    color: #fff;
    padding: 8px 12px;
    text-align: left;
    font-weight: 600;
    letter-spacing: 0.02em;
  }

  td {
    padding: 8px 12px;
    border-bottom: 1px solid #000;
    vertical-align: top;
  }

  tr:nth-child(even) td { background: #f7f7f7; }

  blockquote {
    border-left: 3px solid #000;
    padding: 4px 0 4px 16px;
    margin: 12px 0;
    font-style: italic;
    color: #000;
  }

  a { color: #000; text-decoration: underline; text-underline-offset: 3px; }

  sup a {
    text-decoration: none;
    color: #000;
    font-weight: 600;
    font-size: 0.7em;
    vertical-align: super;
    margin: 0 2px;
    line-height: 0;
  }

  /* Title slide — inverted */
  section.title {
    background: #000;
    color: #fff;
    text-align: left;
  }

  section.title h1 {
    color: #fff;
    font-size: 72px;
    font-weight: 800;
    letter-spacing: -0.03em;
    line-height: 1.0;
    margin-bottom: 18px;
  }

  section.title h2 {
    color: #fff;
    border-bottom: 2px solid #fff;
    font-size: 28px;
    font-weight: 500;
    text-transform: none;
    letter-spacing: 0;
    margin-bottom: 0;
    padding-bottom: 8px;
  }

  section.title p { color: #fff; }
  section.title footer { color: #fff; }
  section.title::after { color: #fff; }

  /* Section divider slides */
  section.act {
    background: #000;
    color: #fff;
    text-align: left;
  }

  section.act h1 {
    color: #fff;
    font-size: 80px;
    font-weight: 800;
    letter-spacing: -0.04em;
    line-height: 1.0;
  }

  section.act h2 {
    color: #fff;
    border-bottom: 1px solid #fff;
    font-size: 24px;
    font-weight: 400;
    text-transform: uppercase;
    letter-spacing: 0.08em;
  }

  section.act footer { color: #fff; }
  section.act::after { color: #fff; }

  /* Q&A / end slide */
  section.end {
    background: #000;
    color: #fff;
  }

  section.end h1 { color: #fff; font-size: 96px; font-weight: 800; }
  section.end h2 { color: #fff; border-color: #fff; }
  section.end p { color: #fff; }
  section.end footer { color: #fff; }
  section.end::after { color: #fff; }

  /* Invert header logo on dark slides (logo is black-on-transparent) */
  section.title header img,
  section.act header img,
  section.end header img {
    filter: invert(1);
  }
---

<!-- _class: title -->

# Home Automation

## Context and History of Home Assistant and ESPHome

**RIAT Bootcamp**

A case study in open-source governance, sustainability, and local-first design.

<!--
Welcome. Land the threat model early.
-->

---

# What is Home Assistant?

A **free, open-source** smart home controller and integration platform. **One point of control** for devices from **any manufacturer**, running **locally on your hardware** without cloud services.

Web browser, Android, or iOS. Voice commands via Google Assistant, Amazon Alexa, Apple Siri, or Home Assistant's own local "**Assist**" assistant.

<!--
Land this: local-first is the architecture, not a feature. Pause on 'no cloud services'.
-->

---

# What is ESPHome?

A **free, open-source** system to control your **ESP32, ESP8266, BK72xx, RP2040, and other microcontrollers** with simple, powerful configuration files — and to control them remotely through home automation systems.

Firmware is generated, compiled, and flashed from a single **YAML file**. **Over-the-air updates** are built in. **No IDE, no build tools, no opaque binary**.

<!--
Frame: user writes YAML, gets a working device. That's it.
-->

---

<!-- _class: act -->

# Act I

## A script that turned on some lights

<!--
Brief. Don't linger.
-->

---

# Act I — The founding

On **September 17, 2013**, **Paulus Schoutsen**, a Dutch software engineer, started a personal project to interface with Philips Hue lights. He published it on GitHub in November 2013 as **Home Assistant**. The Apache 2.0 license was chosen from the start <sup>[1](https://en.wikipedia.org/wiki/Home_Assistant)</sup>.

2013 is the moment the Internet of Things (IoT) became a marketing category. Every sensor and thermostat was acquiring a proprietary cloud account.

Schoutsen's founding principle — ***local control and privacy first*** — was not a business decision. It was an **architectural response to a threat model**:

> *What happens to your home automation when the vendor shuts down, gets acquired, or changes its API?*

<!--
Threat model first. Apache 2.0 returns in Act IV.
-->

---

# Act I — Empirical answers

That question has been answered multiple times:

- **Revolv** — acquired by Nest (Google) in October 2014 for an undisclosed sum. Sold for $299 with a "lifetime subscription." Nest shut down the cloud on **May 15, 2016**. All hardware permanently inoperable. The U.S. Federal Trade Commission (FTC) investigated but chose not to pursue enforcement <sup>[2](https://thenextweb.com/google/2016/04/04/nest-revolv-shutdown/)</sup><sup>[3](https://www.ftc.gov/system/files/documents/closing_letters/nid/160707nestrevolvletter.pdf)</sup>.
- **Insteon** — shut down servers abruptly on **April 15, 2022** without notice, while the status page still read "All Services Online." The HA integration page now carries a permanent warning <sup>[4](https://www.theregister.com/2022/04/19/insteon_cloud_shutdown/)</sup>.
- **Wink** — with one week's notice in May 2020, imposed a **$4.99/month subscription** on hardware sold with "no monthly fees" printed on the box <sup>[5](https://www.consumerreports.org/smart-home/wink-tells-users-pay-up-or-we-will-disable-smart-home-hub/)</sup>.

<!--
Optional: read the Insteon warning aloud if time.
-->

---

<!-- _class: act -->

# Act II

## Hass.io and the usability problem

<!--
Transition.
-->

---

# Act II — Solving installation

Home Assistant grew rapidly as a do-it-yourself (DIY) project, but had a real barrier: running it required Linux administration skills.

In **July 2017**, the team released **Hass.io** — a managed operating system (OS) image for single-board computers (Raspberry Pi) — reducing setup time to minutes <sup>[1](https://en.wikipedia.org/wiki/Home_Assistant)</sup>.

> *This is a recurring pattern in open source: software gets built by those who can compile from source, and the community scales when someone solves the installation problem. Hass.io was that solution.*

<!--
Hass.io dropped hours to minutes. That's the unlock.
-->

---

<!-- _class: act -->

# Act III

## A student builds the missing piece

<!--
Transition: now the firmware side.
-->

---

# Act III — Otto Winter

**Otto Winter** is an Austrian computer science student at the **Technische Universität Wien**.

- Competed in the Austrian Olympiad in Informatics from 2015 onwards
- Qualified for the **International Olympiad in Informatics in Tsukuba, Japan (2018)** <sup>[6](https://www.linkedin.com/in/otto-winter-03644517b/)</sup>
- Around that time, created what would become **ESPHome**

The project started as two repositories:

- `esphomelib` — a C++ framework for ESP microcontrollers
- `esphomeyaml` — a Python tool to generate C++ from YAML

With **version 1.10.0**, both were merged and rebranded as **ESPHome** <sup>[7](https://esphome.io/changelog/v1.10.0/)</sup>. The YAML interface had become the primary way to use the project; the original names were "too technical."

<!--
Stop on the rename. The user surface won.
-->

---

# Act III — The problem ESPHome solved

ESP32, ESP8266, BK72xx, RP2040, and others are inexpensive (**under €5 per chip**), Wi-Fi capable, and programmable. But using them required:

- Writing C++ code from scratch
- Setting up the build tools yourself
- Wiring up over-the-air (OTA) update logic yourself

ESPHome replaced that. You describe the sensor, the pin, the name in a text file — ESPHome turns that into a working program and installs it on the device.

> *The result: no IDE, no build tools, no closed firmware from the manufacturer.*

<!--
The user wants a temperature sensor, not a build environment. Stop on that line.
-->

---

# The declarative paradigm

```yaml
sensor:
  - platform: dht
    pin: D2
    temperature:
      name: "Living room temperature"
    humidity:
      name: "Living room humidity"
```

ESPHome reads this file, converts it into the program that runs on the chip, and installs it on the device. Over-the-air updates (pushing new code over Wi-Fi) are built in.

> *Mental model: describe what you want, not how the machine should do it. The declarative layer is the contribution.*

<!--
Read the YAML out loud. Stop.
-->

---

# The reproducibility dimension

The YAML file is the **complete, human-readable specification** of everything running on the device.

Given the same YAML and the same ESPHome version, you can:

- **Reproduce** the firmware
- **Audit** it
- **Diff** it
- **Version-control** it

This is the structural opposite of consumer IoT firmware, distributed as signed binaries with no published source and silently updated.

> *For work on verifiable and reproducible systems, this is not a minor point — it is the core value proposition stated differently.*

<!--
Pause. The contrast is structural: a YAML in git vs. a signed binary blob.
-->

---

<!-- _class: act -->

# Act IV

## The commercial question

<!--
Transition.
-->

---

# Act IV — Nabu Casa, Inc.

**Nabu Casa, Inc.** was founded in **2018** in Irvine, California, by **Paulus Schoutsen** and **Pascal Vizeli** — two of the principal founders of Home Assistant <sup>[8](https://www.nabucasa.com/about/)</sup>.

Stated motivation: fund ongoing development through a cloud service that put privacy first — not through data brokerage or advertising.

The model:

- Home Assistant core remains **Apache 2.0** — free, open, permissive
- Nabu Casa sells one service: **Home Assistant Cloud** — remote access, encrypted voice relay, off-site backups <sup>[9](https://www.home-assistant.io/cloud/)</sup>
- No investors, no advertising, no data monetisation — funded entirely by user subscriptions <sup>[8](https://www.nabucasa.com/about/)</sup>
- Nabu Casa cannot retroactively relicense the existing open source code

> *This is the "open core plus services" model — the project stays free and open-source, a single paid service funds further development.*

<!--
Pose: can any company fork HA? That's the trade-off the Foundation addresses next.
-->

---

<!-- _class: act -->

# Act V

## An acquisition to preserve, not to monetize

<!--
Transition: the single-maintainer problem.
-->

---

# Act V — The acquisition

In **March 2021**, Nabu Casa acquired ESPHome from Otto Winter <sup>[10](https://www.home-assistant.io/blog/2021/03/18/nabu-casa-has-acquired-esphome/)</sup>.

Stated reason: **continuity**. ESPHome had become critical infrastructure for the Home Assistant ecosystem, and a solo student maintainer is a single point of failure.

Winter had started the project roughly three years earlier. The acquisition ensured it would outlast any single person's available time.

Conditions of the sale:

- ESPHome remained **free and open source**
- Winter **stayed on** as a contributor
- **No revenue stream was gained**, no user base was monetised
- Only motivation stated: **preventing abandonment**

<!--
Pose: what alternative institutional model could have prevented both abandonment and acquisition?
-->

---

<!-- _class: act -->

# Act VI

## Governance as a legal constraint

<!--
Transition: governance as a legal fact, not a promise.
-->

---

# Act VI — The Open Home Foundation

In **April 2024**, Home Assistant, ESPHome, and 250+ related projects were transferred to the **Open Home Foundation (OHF)**, a non-profit <sup>[11](https://www.openhomefoundation.org/projects/)</sup>.

Apache 2.0 alone could not prevent a new owner from closing APIs, adding telemetry, or deprecating local control. The Foundation is the structural firewall against that.

Projects under OHF include Music Assistant, Zigbee2MQTT, Z-Wave JS, Rhasspy, WLED, and Piper.

> *A non-profit structure is the only governance model that makes "it can never be bought, it can never be sold" a legal reality rather than a promise* <sup>[12](https://www.home-assistant.io/blog/2024/11/18/event-wrapup-github-universe-24/)</sup>.

<!--
The legal firewall. Necessary but not sufficient: prevents acquisition, not drift or stagnation.
-->

---

# Act VI — The cloud badge sunset

The OHF also discontinued the **"Works with Home Assistant" cloud certification** badge in August 2024, stating publicly:

> *"All cloud-based products are always doomed to stop working, some sooner than others"* <sup>[13](https://www.home-assistant.io/blog/2024/08/08/works-with-home-assistant-becomes-part-ohf/)</sup>

**This is the threat model, made operational:** the OHF retired a revenue-adjacent program because certifying cloud products would dilute the local-first commitment. The decision is the principle.

<!--
Structural commitment over short-term partnership revenue.
-->

---

# The reverse engineering dimension

A significant portion of HA's integration library was **not built from published documentation**. It was built by reverse engineering proprietary protocols — analysing network traffic, decoding Zigbee and Bluetooth Low Energy (BLE) frames, reconstructing undisclosed device APIs.

Most manufacturers — Tuya is the canonical example — do not publish local APIs. Cloud routing is the business model. Interoperability has to be reconstructed by the community.

**Concrete example: LocalTuya** — a community integration enabling local control of hundreds of cheap Tuya-based smart home products. Built by community members who reverse engineered Tuya's local network protocol. The project's own documentation traces its code back to contributors who decoded the protocol through traffic analysis <sup>[14](https://github.com/rospogrigio/localtuya/)</sup>.

> *The Home Assistant community has functioned, in part, as a distributed reverse engineering apparatus, using the method to create interoperability that manufacturers declined to provide.*

<!--
Pause. Let the room react. LocalTuya is the concrete example.
-->

---

# The open standard question — Matter

Home Assistant has been a vocal advocate for **Matter** — a smart home connectivity standard.

**Timeline:**

- December 2019: announced as "Project Connected Home over IP" (CHIP) by **Amazon, Apple, Google, Samsung SmartThings, Zigbee Alliance** <sup>[15](https://graphsearch.epfl.ch/concept/62658923)</sup>
- October 4, 2022: Matter 1.0 published <sup>[15](https://graphsearch.epfl.ch/concept/62658923)</sup>
- Royalty-free, with the software development kit (SDK) open source under Apache License

> *The governance tension: Matter's development was led by companies with strong interests in keeping smart home data flowing through their ecosystems. The spec is open; its principal backers each operate competing platforms.*

<!--
Standard is open. Governance is not.
-->

---

# Scale — Home Assistant by the numbers

- **2 million** active installations (2025) <sup>[16](https://www.home-assistant.io/blog/2025/04/16/state-of-the-open-home-recap/)</sup>
- **21,000** GitHub contributors in 2024 alone <sup>[12](https://www.home-assistant.io/blog/2024/11/18/event-wrapup-github-universe-24/)</sup>
- **#1** on GitHub Octoverse in 2023 and 2024 <sup>[17](https://github.blog/news-insights/company-news/celebrating-the-github-awards-2024-recipients/)</sup><sup>[12](https://www.home-assistant.io/blog/2024/11/18/event-wrapup-github-universe-24/)</sup>; **#6** in 2025 as AI projects dominate <sup>[18](https://selfh.st/weekly/2025-10-31/)</sup>
- **3,000+** brands supported <sup>[19](https://github.blog/open-source/maintainers/the-local-first-rebellion-how-home-assistant-became-the-most-important-project-in-your-house/)</sup>
- **250+** projects under Open Home Foundation governance <sup>[11](https://www.openhomefoundation.org/projects/)</sup>
- **Apache 2.0** license <sup>[1](https://en.wikipedia.org/wiki/Home_Assistant)</sup>

In 2024, HA out-contributed VS Code (Microsoft) and Flutter (Google) — projects with large dedicated engineering teams <sup>[19](https://github.blog/open-source/maintainers/the-local-first-rebellion-how-home-assistant-became-the-most-important-project-in-your-house/)</sup>.

> *The scale is the distribution: 2 million independent installations, each running locally, each operator controlling their own data. There is no central fleet management, and the architecture intentionally makes wide-scale centralised deployment difficult.*

<!--
Headline is contributor count. #6 in 2025 is an AI-list artefact, not decline.
-->

---

# The stack

**Three languages, three layers:**

- **Python** — core runtime, ~3,000 integrations
- **TypeScript** — frontend, runs in the browser
- **C++** — firmware, via ESPHome (YAML generates C++)

One runs on a server. One in a browser. One on a €5 chip.

<!--
Read the three bullets. Stop on the YAML line.
-->

---

# Local-first by design

**Protocols** (no mandatory cloud routing)
- Zigbee, Z-Wave, Matter, Thread, Wi-Fi, Bluetooth LE — all local-first

**Voice** (fully offline)
- Whisper for speech recognition, Piper for speech synthesis — both local

**Governance** (license and structure)
- Apache 2.0
- Open Home Foundation (non-profit steward)

<!--
Tie back to Act I. Voice runs offline. Governance is the firewall.
-->

---

# Discussion hooks

Four questions for this audience.

1. **Reproducibility and verifiability** — Is the ESPHome build itself reproducible in the strict technical sense, bit-for-bit across build environments? What would full supply-chain verifiability look like for a consumer IoT device?
2. **Reverse engineering as method** — How should an open source project relate to RE contributions? Is RIAT's framing of RE as a cultural method a useful lens here?
3. **The sustainability trap** — Otto Winter built critical infrastructure alone, then had to sell it. What institutional models could have prevented that? Does the OHF model solve this, or just delay it?
4. **Apache 2.0 and the commons** — The permissive license enables Nabu Casa's model but also enables proprietary forks. The GPL copyleft license would prevent the latter but might have prevented the former. Is there a license that better matches OHF's stated values?
<!--
Plan ~20 min. Let the room pick. #2 and #3 usually land best with RIAT.
-->

---

# Sources

1. [Home Assistant — Wikipedia](https://en.wikipedia.org/wiki/Home_Assistant)
2. [Revolv shutdown (April 2016) — The Next Web](https://thenextweb.com/google/2016/04/04/nest-revolv-shutdown/)
4. [Insteon shutdown (April 2022) — The Register](https://www.theregister.com/2022/04/19/insteon_cloud_shutdown/)
6. [Otto Winter — GitHub](https://github.com/OttoWinter)
10. [Nabu Casa acquires ESPHome (March 2021) — HA blog](https://www.home-assistant.io/blog/2021/03/18/nabu-casa-has-acquired-esphome/)
11. [Open Home Foundation projects](https://www.openhomefoundation.org/projects/)
12. [GitHub Universe 2024 wrap-up — HA blog](https://www.home-assistant.io/blog/2024/11/18/event-wrapup-github-universe-24/)
14. [LocalTuya — community RE integration](https://github.com/rospogrigio/localtuya/)
16. [State of the Open Home 2025 — HA blog](https://www.home-assistant.io/blog/2025/04/16/state-of-the-open-home-recap/)
19. [GitHub — "The local-first rebellion"](https://github.blog/open-source/maintainers/the-local-first-rebellion-how-home-assistant-became-the-most-important-project-in-your-house/)

<!--
Top-10 handout.
-->

---

<!-- _class: end -->

## Thank you

**RIAT Bootcamp**

<!--
Open the floor. If silence, start with #1.
-->
