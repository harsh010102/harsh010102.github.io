---
title: "Betting on the Bottom of the Compute Stack"
date: 2026-08-29
permalink: /posts/2026/08/investable-compute-thesis/
excerpt: "How I would underwrite the next compute moat. Where value is captured and kept in the AI value chain, the decision discipline I borrow from Ulu Ventures, why only analog and photonics can ship today, the pre-seed and seed deals my radar surfaces, and one of them run through the model."
tags:
  - Deep Tech
  - Venture Capital
  - Next-Gen Computing
  - Photonics
  - Analog Computing
  - Investment Thesis
---

Before I get started with yet another compute moat underwriting problem, I should mention what I'm going to cover. In this post, I lay out the value-chain logic and decision discipline that should be run before making any bet, identify the two layers in the compute stack you should be watching, and explain how the tool I built can help you find companies early.

The number one failure pattern I have seen in first-round AI infrastructure pitches lately is the same, a real physical advantage sits wrapped in a story that moves the value somewhere the team cannot defend and keep. Although my job is to scout new ventures in the deep-tech universe, the goal is to find where the advantage is real and where it stays. That's the idea I write down next.

In compute, value is captured and kept at the bottom of the stack, but only where the physics is manufacturable today. Everything below takes both halves of that sentence seriously.

---

## 1. The value chain decides who keeps the money

Start with the map. [FourWeekMBA's AI value chain](https://fourweekmba.com/ai-value-chain-2026/)
and the [AI Data Center Explained](https://www.youtube.com/watch?v=ckoi0RTEgcY) bird's-eye view make the same structural point, and it is
the one that matters for an investor:

> Margin shows who captures value today. Defensibility shows who keeps it tomorrow.

Applications and models earn the loudest revenue and hold the weakest defence, because the
layer beneath them can be swapped, cloned, or commoditised by the next model release. The
substrate and systems layers, meaning the chips, the interconnect, and the power and thermal
envelope, stay quiet on the P&L and are far harder to displace. Durable moats live there.
NVIDIA proves the point. Its lock-in comes less from the GPU than from CUDA and the generation
of developers trained on it. A moat is physics plus an ecosystem that makes the physics the
standard.

<div class="fig" markdown="0">
<svg viewBox="0 0 720 320" width="100%" style="max-width:720px;height:auto;font-family:system-ui,Segoe UI,Arial,sans-serif" role="img" aria-label="AI value chain stack">
  <defs>
    <linearGradient id="marg" x1="0" x2="0" y1="0" y2="1">
      <stop offset="0" stop-color="#b56576"/><stop offset="1" stop-color="#10656b"/>
    </linearGradient>
  </defs>
  <text x="12" y="20" font-size="13" font-weight="700" fill="#111">The compute value chain, from loud margin to deep moat</text>
  <g font-size="12.5">
    <rect x="120" y="40"  width="470" height="34" rx="5" fill="#f2e0e4" stroke="#b56576"/>
    <text x="130" y="62" fill="#7d3a4a" font-weight="600">Applications &amp; agents</text>
    <rect x="150" y="80"  width="410" height="34" rx="5" fill="#f3e0d6" stroke="#bf5a3c"/>
    <text x="160" y="102" fill="#8a3d22" font-weight="600">Foundation models</text>
    <rect x="180" y="120" width="350" height="34" rx="5" fill="#f4e9c8" stroke="#c79212"/>
    <text x="190" y="142" fill="#6f5210" font-weight="600">Frameworks / developer ecosystem (the CUDA moat)</text>
    <rect x="150" y="160" width="410" height="34" rx="5" fill="#dbeee3" stroke="#3f8f6b"/>
    <text x="160" y="182" fill="#2b6b4f" font-weight="600">Systems: interconnect · power &amp; thermal · packaging</text>
    <rect x="120" y="200" width="470" height="40" rx="5" fill="#d3e6e4" stroke="#10656b"/>
    <text x="130" y="225" fill="#3b2d4f" font-weight="700">Substrate: the compute device itself (transistor → photon → analog)</text>
  </g>
  <line x1="40" y1="44" x2="40" y2="236" stroke="url(#marg)" stroke-width="8" stroke-linecap="round"/>
  <text x="16" y="52" font-size="11" fill="#7d3a4a" font-weight="600">margin</text>
  <text x="16" y="236" font-size="11" fill="#3b2d4f" font-weight="600">moat</text>
  <text x="612" y="52" font-size="11" fill="#7d3a4a">easy to clone</text>
  <text x="612" y="228" font-size="11" fill="#3b2d4f" font-weight="700">hardest to displace</text>
  <text x="612" y="242" font-size="10" fill="#555">↑ deploy conviction here</text>
</svg>
</div>

That gives me the first screen. Does the advantage sit at a layer that can be defended, and
does the team have a credible path to becoming the standard there? A model wrapper fails it.
A device with real physics passes.

---

## 2. How Ulu Ventures strips the guesswork out of a decision

Knowing where to look does not tell you how to choose. For that I borrow the decision-analysis
method that [Ulu Ventures](https://uluventures.com/working-with-ulu/) (Miriam Rivera and Clint
Korver) adapted from Stanford, the approach the Stanford GSB case study calls the
["Moneyball of venture capital"](https://www.gsb.stanford.edu/faculty-research/case-studies/ulu-ventures-moneyball-venture-capital).
Instead of pattern-matching and gut feel, Ulu treats human judgment as data. It converts
qualitative assessments into explicit probabilities and computes a probability-weighted
multiple on invested capital (PWMOI). The process, distilled from Korver's
[Kauffman Fellows write-up](https://www.kauffmanfellows.org/journal/applying-decision-analysis-to-venture-investing),
runs like this:

1. Assess the investment (visionary founder, home-run market, risk and reward).
2. **Early-stage risk.** Assign probabilities to market, product, team and financial risk, then multiply them.
3. **Life-stage risk.** Estimate the odds of crossing the chasm, then of mass-market success, on a decision tree.
4. **Market share.** Leader, challenger, or also-ran, based on sustainable differentiation.
5. **Blend it.** Diagram the value drivers, set low, base and high ranges, run sensitivity and scenario analysis, and reduce it to one PWMOI.

The machinery is not there for false precision. It exists to separate a great story from a
great expected return, and to force the chasm into the maths instead of the pitch.

<div class="fig" markdown="0">
<svg viewBox="0 0 720 330" width="100%" style="max-width:720px;height:auto;font-family:system-ui,Segoe UI,Arial,sans-serif" role="img" aria-label="Ulu Ventures decision analysis pipeline">
  <defs><marker id="ua" markerWidth="8" markerHeight="8" refX="6" refY="3" orient="auto"><path d="M0,0 L6,3 L0,6 Z" fill="#888"/></marker></defs>
  <text x="12" y="20" font-size="13" font-weight="700" fill="#111">Judgment → probabilities → a probability-weighted return (PWMOI)</text>
  <g font-size="11">
    <rect x="12"  y="40" width="118" height="40" rx="6" fill="#e6efee" stroke="#10656b"/><text x="71" y="58" text-anchor="middle" fill="#3b2d4f">Market ·80</text><text x="71" y="72" text-anchor="middle" fill="#3b2d4f">Product ·80</text>
    <rect x="140" y="40" width="118" height="40" rx="6" fill="#e6efee" stroke="#10656b"/><text x="199" y="58" text-anchor="middle" fill="#3b2d4f">Team ·95</text><text x="199" y="72" text-anchor="middle" fill="#3b2d4f">Financial ·95</text>
    <rect x="286" y="40" width="150" height="40" rx="6" fill="#d3e6e4" stroke="#3b2d4f"/><text x="361" y="58" text-anchor="middle" font-weight="700" fill="#3b2d4f">Early-stage success</text><text x="361" y="73" text-anchor="middle" font-weight="700" fill="#3b2d4f">= 58%</text>
  </g>
  <g font-size="11">
    <rect x="12"  y="120" width="150" height="46" rx="6" fill="#e4f0e8" stroke="#3f8f6b"/><text x="87" y="140" text-anchor="middle" fill="#2b6b4f" font-weight="600">Cross the chasm</text><text x="87" y="156" text-anchor="middle" fill="#2b6b4f">×24% → 14%</text>
    <rect x="186" y="120" width="150" height="46" rx="6" fill="#e4f0e8" stroke="#3f8f6b"/><text x="261" y="140" text-anchor="middle" fill="#2b6b4f" font-weight="600">Mass market</text><text x="261" y="156" text-anchor="middle" fill="#2b6b4f">×37% → 5%</text>
    <rect x="360" y="120" width="150" height="46" rx="6" fill="#f6efd6" stroke="#c79212"/><text x="435" y="140" text-anchor="middle" fill="#6f5210" font-weight="600">Market-leader share</text><text x="435" y="156" text-anchor="middle" fill="#6f5210">×25% → ~1%</text>
    <rect x="540" y="108" width="168" height="70" rx="8" fill="#3b2d4f"/><text x="624" y="135" text-anchor="middle" fill="#fff" font-size="13" font-weight="700">PWMOI</text><text x="624" y="162" text-anchor="middle" fill="#fff" font-size="22" font-weight="800">≈ 9×</text>
  </g>
  <g stroke="#888" stroke-width="1.5" fill="none">
    <line x1="130" y1="60" x2="138" y2="60" marker-end="url(#ua)"/>
    <line x1="258" y1="60" x2="284" y2="60" marker-end="url(#ua)"/>
    <line x1="162" y1="143" x2="184" y2="143" marker-end="url(#ua)"/>
    <line x1="336" y1="143" x2="358" y2="143" marker-end="url(#ua)"/>
    <line x1="510" y1="143" x2="538" y2="143" marker-end="url(#ua)"/>
  </g>
  <text x="12" y="200" font-size="10.5" fill="#555">Worked example (Inkling): the market-leader "home run" is only ~1% likely,</text>
  <text x="12" y="214" font-size="10.5" fill="#555">yet blended across all scenarios the deal still pencils to a 9× probability-weighted return.</text>
  <text x="12" y="240" font-size="11" font-weight="700" fill="#111">Biases the process is built to counter:</text>
  <g font-size="11">
    <rect x="12"  y="252" width="180" height="30" rx="15" fill="#f2e0e4" stroke="#b56576"/><text x="102" y="271" text-anchor="middle" fill="#7d3a4a">representativeness (pattern-match)</text>
    <rect x="202" y="252" width="150" height="30" rx="15" fill="#f3e0d6" stroke="#bf5a3c"/><text x="277" y="271" text-anchor="middle" fill="#8a3d22">confirmation bias</text>
    <rect x="362" y="252" width="120" height="30" rx="15" fill="#f4e9c8" stroke="#c79212"/><text x="422" y="271" text-anchor="middle" fill="#6f5210">anchoring</text>
  </g>
</svg>
</div>

The most useful idea here is that the chasm is a technology-readiness question dressed as a
go-to-market question. A device that works in a paper but still needs three material-science
miracles to ship is a research grant.

---

## 3. Why readiness beats novelty

This is where I part ways with the usual next-gen-compute enthusiasm. I recently mapped the
alternative-compute landscape (biological, quantum, analog, photonic), scoring each paradigm's
energy-efficiency claim against its technology-readiness level (TRL). The efficiency headlines
are large. DNA compute claims roughly a billion times the efficiency of silicon and photonic
processors claim about 30× over CMOS. Headlines do not ship.


<div class="fig" markdown="0">
<svg viewBox="0 0 720 300" width="100%" style="max-width:720px;height:auto;font-family:system-ui,Segoe UI,Arial,sans-serif" role="img" aria-label="TRL by compute paradigm">
  <text x="12" y="20" font-size="13" font-weight="700" fill="#111">Energy-efficient compute paradigms, by technology readiness (TRL 1–9)</text>
  <rect x="540" y="40" width="160" height="220" fill="#e4f0e8"/>
  <text x="545" y="34" font-size="10.5" fill="#2b6b4f" font-weight="700">TRL 7–9 · shippable</text>
  <g font-size="9" fill="#999">
    <line x1="60" y1="260" x2="700" y2="260" stroke="#ccc"/>
    <line x1="60" y1="40" x2="60" y2="260" stroke="#ccc"/>
    <text x="60" y="274">TRL 1</text><text x="516" y="274">TRL 7</text><text x="676" y="274">TRL 9</text>
  </g>
  <g font-size="12">
    <rect x="60" y="48"  width="140" height="26" rx="4" fill="#cdcae8"/><text x="208" y="66" fill="#4b4b8f">Biocomputing · TRL 2–4</text>
    <rect x="60" y="86"  width="220" height="26" rx="4" fill="#edc3a5"/><text x="288" y="104" fill="#8a3d22">Quantum · TRL 2–5</text>
    <rect x="60" y="124" width="460" height="26" rx="4" fill="#ecd68f"/><text x="70" y="142" fill="#5f4410" font-weight="700">Neuromorphic / analog · TRL 4–7</text>
    <rect x="60" y="162" width="540" height="26" rx="4" fill="#b9dccb"/><text x="70" y="180" fill="#2b6b4f" font-weight="700">Photonic compute · TRL 4–7</text>
    <rect x="60" y="200" width="640" height="26" rx="4" fill="#10656b"/><text x="70" y="218" fill="#fff" font-weight="700">Photonic data-centre I/O · TRL 9</text>
  </g>
</svg>
</div>

Bio and quantum are extraordinary science and, for my mandate, still pre-chasm. Analog and
photonics have reached TRL 7 to 9, with first products, real customers, and a manufacturable
process. I split the
investable surface into two theses.

- **Analog for edge AI inference.** In-memory and neuromorphic devices compute where the data
  is, at microwatts, tolerating the precision loss that edge workloads forgive. The moat is
  device physics. The risk is the software stack.
- **Photonics for data-centre I/O.** Moving bits as light instead of copper is the
  nearest-term, highest-TRL win, because the bottleneck in AI data centres has shifted from
  FLOPs to the interconnect and its power.

The second thesis now has hard market pull. In March 2026, NVIDIA committed USD 2 billion each
to Coherent and Lumentum, a USD 4 billion bet that silicon photonics is how you fix AI's copper
bottleneck.

Follow the capex inside an AI data centre and you see the same thing. As accelerators scale
out, a growing share of the bill moves off the chip and into the interconnect, the power
delivery, and the cooling, which are the systems layer. Photonic I/O attacks the interconnect
directly, and the power budget with it. 

---

## 4. The deals my radar surfaces

A thesis without a pipeline is just a blog post. Here are the newest European companies, all
pre-seed or seed, sitting at these two layers. The tool in the next section sourced and
classified every one. I then read each through the value-chain and readiness lens above. The
verdicts are mine.

<div class="deals" markdown="0">
<table style="width:100%;border-collapse:collapse;font-size:13px;font-family:system-ui,Segoe UI,Arial,sans-serif">
<thead><tr style="background:#3b2d4f;color:#fff;text-align:left">
<th style="padding:7px 9px">Company</th><th style="padding:7px 9px">Layer</th><th style="padding:7px 9px">Why it can be defended</th><th style="padding:7px 9px">Verdict</th></tr></thead>
<tbody>
<tr style="border-bottom:1px solid #e6e6e6"><td style="padding:7px 9px"><b>Finchetto</b> · UK · pre-seed</td><td style="padding:7px 9px">Photonic I/O</td><td style="padding:7px 9px">Fully-passive optical switch, no electronics in the fabric, 26–53× power cut and ~40 ns latency. Physics-level moat.</td><td style="padding:7px 9px;color:#2b6b4f;font-weight:700">SELECT</td></tr>
<tr style="border-bottom:1px solid #e6e6e6;background:#fafbfc"><td style="padding:7px 9px"><b>Salience Labs</b> · UK/DE · seed</td><td style="padding:7px 9px">Photonic compute</td><td style="padding:7px 9px">Photonic multi-chip processor with all-optical connectivity (Oxford / Münster). Strong physics, unproven software path.</td><td style="padding:7px 9px;color:#a5701a;font-weight:700">WATCH</td></tr>
<tr style="border-bottom:1px solid #e6e6e6"><td style="padding:7px 9px"><b>Linq Photonics</b> · DE · seed</td><td style="padding:7px 9px">Photonic I/O</td><td style="padding:7px 9px">Photonic integrated circuits and modules for data-centre links. Lab-origin, capital-efficient, very early.</td><td style="padding:7px 9px;color:#a5701a;font-weight:700">WATCH</td></tr>
<tr style="border-bottom:1px solid #e6e6e6;background:#fafbfc"><td style="padding:7px 9px"><b>Moon Photonics</b> · DE · seed</td><td style="padding:7px 9px">Photonic I/O</td><td style="padding:7px 9px">Photonic components for high-performance-computing links. Early university spinout.</td><td style="padding:7px 9px;color:#a5701a;font-weight:700">WATCH</td></tr>
<tr style="border-bottom:1px solid #e6e6e6"><td style="padding:7px 9px"><b>Aylight</b> · CH · pre-seed</td><td style="padding:7px 9px">Photonic I/O</td><td style="padding:7px 9px">Chip-scale multiwavelength laser (ETH Zürich): one photonic chip emitting the many wavelengths optical links need.</td><td style="padding:7px 9px;color:#a5701a;font-weight:700">WATCH</td></tr>
<tr style="border-bottom:1px solid #e6e6e6;background:#fafbfc"><td style="padding:7px 9px"><b>SteerLight</b> · FR · seed</td><td style="padding:7px 9px">Edge sensing</td><td style="padding:7px 9px">Silicon-photonic FMCW LiDAR for the sensor edge. Photonics reaching into edge perception, beyond the data centre.</td><td style="padding:7px 9px;color:#a5701a;font-weight:700">WATCH</td></tr>
<tr style="border-bottom:1px solid #e6e6e6"><td style="padding:7px 9px"><b>Neurobus</b> · DE · seed</td><td style="padding:7px 9px">Neuromorphic edge</td><td style="padding:7px 9px">Event-driven neuromorphic processing for space and industrial edge, built for low-power always-on sensing.</td><td style="padding:7px 9px;color:#a5701a;font-weight:700">WATCH</td></tr>
<tr style="border-bottom:1px solid #e6e6e6;background:#fafbfc"><td style="padding:7px 9px"><b>Rayd Technologies</b> · UK · pre-seed</td><td style="padding:7px 9px">Photonic-neuromorphic</td><td style="padding:7px 9px">Genuine architecture (photonic + neuromorphic), earliest stage, needs a software stack it does not yet have.</td><td style="padding:7px 9px;color:#6f5210;font-weight:700">CONDITIONAL</td></tr>
</tbody></table>
</div>

I select on defensible physics with a credible adoption path, watch
where the physics is real but the software moat is unproven, and stay conditional on
architectures that still need a stack. 



Explore the full live dataset on the
[Compute Radar dashboard](https://harsh010102.github.io/compute-radar-eu/dashboard/).

---

## 5. How the tool finds lab-origin deals early

Every company above came out of a system I built on one conviction. Deep tech is born in
university and PhD research, so the incubator is the earliest honest signal, well before the
funding announcement.

So the radar goes to the source. It does not scrape Crunchbase. It watches ~30 EU and North
American compute incubators and research-lab accelerators, enriches them from the regional
startup press those databases themselves ingest, and runs each candidate through a small
multi-agent pipeline.

<div class="fig" markdown="0">
<svg viewBox="0 0 720 250" width="100%" style="max-width:720px;height:auto;font-family:system-ui,Segoe UI,Arial,sans-serif" role="img" aria-label="Compute Radar architecture">
  <defs><marker id="ar" markerWidth="8" markerHeight="8" refX="6" refY="3" orient="auto"><path d="M0,0 L6,3 L0,6 Z" fill="#888"/></marker></defs>
  <g font-size="11.5">
    <rect x="10" y="60" width="130" height="70" rx="7" fill="#e6efee" stroke="#10656b"/>
    <text x="75" y="82" text-anchor="middle" font-weight="700" fill="#3b2d4f">Sources</text>
    <text x="75" y="100" text-anchor="middle" fill="#333">~30 incubators</text>
    <text x="75" y="115" text-anchor="middle" fill="#333">lab accelerators</text>
    <rect x="180" y="30" width="150" height="60" rx="7" fill="#f6e9e0" stroke="#bf5a3c"/>
    <text x="255" y="52" text-anchor="middle" font-weight="700" fill="#8a3d22">Scout agent</text>
    <text x="255" y="70" text-anchor="middle" fill="#333">Exa semantic search</text>
    <text x="255" y="84" text-anchor="middle" fill="#333">+ RSS / news</text>
    <rect x="180" y="100" width="150" height="60" rx="7" fill="#f6efd6" stroke="#c79212"/>
    <text x="255" y="122" text-anchor="middle" font-weight="700" fill="#6f5210">Analyst agent</text>
    <text x="255" y="140" text-anchor="middle" fill="#333">LLM classify →</text>
    <text x="255" y="153" text-anchor="middle" fill="#333">8-layer taxonomy</text>
    <rect x="370" y="65" width="150" height="60" rx="7" fill="#e4f0e8" stroke="#3f8f6b"/>
    <text x="445" y="87" text-anchor="middle" font-weight="700" fill="#2b6b4f">Patent verify</text>
    <text x="445" y="105" text-anchor="middle" fill="#333">EPO OPS check</text>
    <text x="445" y="118" text-anchor="middle" fill="#333">(is the IP real?)</text>
    <rect x="560" y="65" width="150" height="60" rx="7" fill="#e6efee" stroke="#3b2d4f"/>
    <text x="635" y="87" text-anchor="middle" font-weight="700" fill="#3b2d4f">Radar dashboard</text>
    <text x="635" y="105" text-anchor="middle" fill="#333">filter by layer,</text>
    <text x="635" y="118" text-anchor="middle" fill="#333">stage, geography</text>
  </g>
  <g stroke="#888" stroke-width="1.6" fill="none">
    <line x1="140" y1="90" x2="178" y2="62" marker-end="url(#ar)"/>
    <line x1="140" y1="100" x2="178" y2="128" marker-end="url(#ar)"/>
    <line x1="330" y1="60" x2="368" y2="88" marker-end="url(#ar)"/>
    <line x1="330" y1="130" x2="368" y2="100" marker-end="url(#ar)"/>
    <line x1="520" y1="95" x2="558" y2="95" marker-end="url(#ar)"/>
  </g>
  <text x="12" y="20" font-size="13" font-weight="700" fill="#111">Compute Radar, an incubator-first and patent-verified pipeline</text>
  <text x="12" y="230" font-size="10.5" fill="#666">Free / open tooling · runs on a schedule · every company classified against a fixed 8-layer compute taxonomy.</text>
</svg>
</div>

The design choices are the argument:

- **Incubator-first, not database-first.** Non-dilutive incubator money attaches months before a priced round. That is the sourcing alpha.
- **A fixed 8-layer taxonomy** (substrate, architecture, interconnect, power/thermal, packaging, co-design/EDA, sovereign edge, sovereign cloud). Classification stays testable and the dataset stays filterable in the fund's own language.
- **Patent verification via the EPO.** A patent family is harder to fake. This is the first automated pass of technical due diligence.
- **Provider-agnostic LLMs with fallback.** It runs on free, open tooling on a schedule, not a paid data subscription.

**Where it goes next.** The EPO check answers whether the IP exists. The next version should
answer whether the IP is any good, wiring the pipeline into full patent databases for claims
parsing and citation analysis so it can tell genuine device-level differentiation from
defensive filing. 

---

## 6. What I'm claiming

- **Back the bottom of the stack.** Substrate and systems keep their moats. Applications earn loud margin with thin defence.
- **Underwrite readiness, not novelty.** Of the exotic paradigms, only analog (edge AI) and photonics (data-centre I/O) have crossed into TRL 7 to 9. A fund can deploy conviction there now. Bio and quantum stay on the watch-list.
- **Follow the strategic pull.** NVIDIA's USD 4 billion into Coherent and Lumentum marks the photonic-I/O layer as where the next decade of AI-infra capex concentrates.
- **Source from the lab.** Track research-aligned incubators, verify with patents, and you see the defensible companies before the market prices them.

I am an AI researcher and venture scout who would rather ship
the tool that finds the deal than argue about it in the abstract. To see the person behind the
thesis, the projects, and the code, open my portfolio
[harsh-portfolio](https://harsh010102.github.io/harsh-portfolio/).

---

*Sources and method: [FourWeekMBA, AI Value Chain (2026)](https://fourweekmba.com/ai-value-chain-2026/);
Ulu Ventures decision analysis
([Kauffman Fellows](https://www.kauffmanfellows.org/journal/applying-decision-analysis-to-venture-investing),
[Stanford GSB case](https://www.gsb.stanford.edu/faculty-research/case-studies/ulu-ventures-moneyball-venture-capital));
NVIDIA's March 2026 investments of USD 2 billion each in Coherent and Lumentum (widely reported);
company facts and classifications from my own
[Compute Radar](https://harsh010102.github.io/compute-radar-eu/dashboard/) dataset (incubator
pages, EU-Startups, EPO filings); TRL assessment from my deep-dive on alternative-compute
paradigms. The Finchetto model uses my own illustrative estimates.*
