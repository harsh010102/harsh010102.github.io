---
title: "Betting on the Bottom of the Stack: An Investable Case for Analog & Photonic Compute"
date: 2026-08-29
permalink: /posts/2026/08/investable-compute-thesis/
excerpt: "How I'd underwrite the next compute moat: the value-chain logic (value is captured and kept at the bottom of the stack), Ulu Ventures' decision-analysis discipline, why only analog and photonics are shippable today (TRL 7–9), the deals my radar surfaces, and how the tool sources lab-origin companies before the market prices them."
tags:
  - Deep Tech
  - Venture Capital
  - Next-Gen Computing
  - Photonics
  - Analog Computing
  - Investment Thesis
---

*I evaluate the technology, not the pitch deck. This is how I would underwrite the next
compute moat — the value-chain logic, the decision discipline, the two layers that are
actually shippable today, and a tool I built to source the companies before the market
sees them.*

Most "AI infrastructure" pitches I read at NXP fail the same way: a real physical
advantage is wrapped in a story that quietly migrates the value somewhere the team can't
defend. My job — scouting 380+ deep-tech startups across 14 verticals — is to find where
the advantage is *real and kept*. This post is that filter, written down.

The thesis in one line: **in compute, value is captured and kept at the bottom of the
stack — but only where the physics is manufacturable today.** Everything below follows
from taking both halves of that sentence seriously.

---

## 1. The value chain decides who keeps the money

Start with the map. [FourWeekMBA's AI value chain](https://fourweekmba.com/ai-value-chain-2026/)
and the "AI Data Center Explained" bird's-eye view both make the same structural point, and
it is the one that matters for an investor:

> **Margin shows who captures value today. Defensibility shows who keeps it tomorrow.**

Applications and models are where revenue is loudest — and where it is least defensible,
because the layer below can be swapped, cloned, or commoditised by the next model release.
The **substrate and systems layers** — the chips, the interconnect, the power and thermal
envelope — are quieter on the P&L and far harder to displace. That is where durable moats
live. NVIDIA is the proof by contradiction: its lock-in isn't the GPU alone, it's CUDA and
a generation of developers trained on it. A moat is physics *plus* an ecosystem that makes
the physics the standard.

<div class="fig" markdown="0">
<svg viewBox="0 0 720 320" width="100%" style="max-width:720px;height:auto;font-family:system-ui,Segoe UI,Arial,sans-serif" role="img" aria-label="AI value chain stack">
  <defs>
    <linearGradient id="marg" x1="0" x2="0" y1="0" y2="1">
      <stop offset="0" stop-color="#e87ba4"/><stop offset="1" stop-color="#2a78d6"/>
    </linearGradient>
  </defs>
  <text x="12" y="20" font-size="13" font-weight="700" fill="#111">The compute value chain — where margin is loud, where moats are deep</text>
  <!-- layers -->
  <g font-size="12.5">
    <rect x="120" y="40"  width="470" height="34" rx="5" fill="#fbe4ee" stroke="#e87ba4"/>
    <text x="130" y="62" fill="#8a2a52" font-weight="600">Applications &amp; agents</text>
    <rect x="150" y="80"  width="410" height="34" rx="5" fill="#fde3d6" stroke="#eb6834"/>
    <text x="160" y="102" fill="#9c3d13" font-weight="600">Foundation models</text>
    <rect x="180" y="120" width="350" height="34" rx="5" fill="#fdeecb" stroke="#eda100"/>
    <text x="190" y="142" fill="#8a6200" font-weight="600">Frameworks / developer ecosystem (the CUDA moat)</text>
    <rect x="150" y="160" width="410" height="34" rx="5" fill="#d9f2e8" stroke="#1baf7a"/>
    <text x="160" y="182" fill="#0d6b49" font-weight="600">Systems: interconnect · power &amp; thermal · packaging</text>
    <rect x="120" y="200" width="470" height="40" rx="5" fill="#d6e6fb" stroke="#2a78d6"/>
    <text x="130" y="225" fill="#164a8f" font-weight="700">Substrate: the compute device itself (transistor → photon → analog)</text>
  </g>
  <!-- axes arrows -->
  <line x1="40" y1="44" x2="40" y2="236" stroke="url(#marg)" stroke-width="8" stroke-linecap="round"/>
  <text x="16" y="52" font-size="11" fill="#8a2a52" font-weight="600">margin</text>
  <text x="16" y="236" font-size="11" fill="#164a8f" font-weight="600">moat</text>
  <text x="612" y="52" font-size="11" fill="#8a2a52">easy to clone</text>
  <text x="612" y="228" font-size="11" fill="#164a8f" font-weight="700">hardest to displace</text>
  <text x="612" y="242" font-size="10" fill="#555">↑ deploy conviction here</text>
</svg>
</div>

So the first screen writes itself: **does the advantage live at a layer that can be
defended, and does the team have a credible path to becoming the standard there?** A
brilliant model wrapper fails this test. A device with genuine physics and a developer
story passes it.

---

## 2. The decision discipline: how Ulu Ventures strips out the guesswork

Knowing *where* to look doesn't tell you *how* to choose. For that I borrow the
decision-analysis method that [Ulu Ventures](https://uluventures.com/working-with-ulu/)
(Miriam Rivera and Clint Korver) adapted from Stanford and made explicit — what the Stanford
GSB case study calls
["the Moneyball of venture capital"](https://www.gsb.stanford.edu/faculty-research/case-studies/ulu-ventures-moneyball-venture-capital).
Instead of pattern-matching and gut feel, Ulu treats human judgment as *data*: it converts
qualitative assessments into explicit probabilities and computes a **probability-weighted
multiple on invested capital (PWMOI)**. Their process, distilled from Korver's
[Kauffman Fellows write-up](https://www.kauffmanfellows.org/journal/applying-decision-analysis-to-venture-investing):

1. Assess the investment (visionary founder, home-run market, risk/reward).
2. **Early-stage risk** — assign probabilities to market, product, team and financial risk, and multiply them.
3. **Life-stage risk** — estimate the odds of *crossing the chasm* and then of mass-market success, on a decision tree.
4. **Market share** — leader, challenger, or also-ran, based on sustainable differentiation.
5. Build a **decision diagram** of the value drivers, structure **low/base/high** ranges, run **sensitivity** and **scenario** analysis, and blend to a single PWMOI.

The point of all that machinery is not false precision — it is to **separate a great story
from a great expected return**, and to force the chasm into the maths instead of the pitch.

<div class="fig" markdown="0">
<svg viewBox="0 0 720 330" width="100%" style="max-width:720px;height:auto;font-family:system-ui,Segoe UI,Arial,sans-serif" role="img" aria-label="Ulu Ventures decision analysis pipeline">
  <defs><marker id="ua" markerWidth="8" markerHeight="8" refX="6" refY="3" orient="auto"><path d="M0,0 L6,3 L0,6 Z" fill="#888"/></marker></defs>
  <text x="12" y="20" font-size="13" font-weight="700" fill="#111">Judgment → probabilities → a probability-weighted return (PWMOI)</text>
  <!-- row 1: four risk factors -->
  <g font-size="11">
    <rect x="12"  y="40" width="118" height="40" rx="6" fill="#eef3fb" stroke="#2a78d6"/><text x="71" y="58" text-anchor="middle" fill="#164a8f">Market ·80</text><text x="71" y="72" text-anchor="middle" fill="#164a8f">Product ·80</text>
    <rect x="140" y="40" width="118" height="40" rx="6" fill="#eef3fb" stroke="#2a78d6"/><text x="199" y="58" text-anchor="middle" fill="#164a8f">Team ·95</text><text x="199" y="72" text-anchor="middle" fill="#164a8f">Financial ·95</text>
    <rect x="286" y="40" width="150" height="40" rx="6" fill="#d6e6fb" stroke="#164a8f"/><text x="361" y="58" text-anchor="middle" font-weight="700" fill="#164a8f">Early-stage success</text><text x="361" y="73" text-anchor="middle" font-weight="700" fill="#164a8f">= 58%</text>
  </g>
  <!-- row 2: compounding gates -->
  <g font-size="11">
    <rect x="12"  y="120" width="150" height="46" rx="6" fill="#e8f6ef" stroke="#1baf7a"/><text x="87" y="140" text-anchor="middle" fill="#0d6b49" font-weight="600">Cross the chasm</text><text x="87" y="156" text-anchor="middle" fill="#0d6b49">×24% → 14%</text>
    <rect x="186" y="120" width="150" height="46" rx="6" fill="#e8f6ef" stroke="#1baf7a"/><text x="261" y="140" text-anchor="middle" fill="#0d6b49" font-weight="600">Mass market</text><text x="261" y="156" text-anchor="middle" fill="#0d6b49">×37% → 5%</text>
    <rect x="360" y="120" width="150" height="46" rx="6" fill="#fdf6e0" stroke="#eda100"/><text x="435" y="140" text-anchor="middle" fill="#8a6200" font-weight="600">Market-leader share</text><text x="435" y="156" text-anchor="middle" fill="#8a6200">×25% → ~1%</text>
    <rect x="540" y="108" width="168" height="70" rx="8" fill="#164a8f"/><text x="624" y="135" text-anchor="middle" fill="#fff" font-size="13" font-weight="700">PWMOI</text><text x="624" y="162" text-anchor="middle" fill="#fff" font-size="22" font-weight="800">≈ 9×</text>
  </g>
  <g stroke="#888" stroke-width="1.5" fill="none">
    <line x1="130" y1="60" x2="138" y2="60" marker-end="url(#ua)"/>
    <line x1="258" y1="60" x2="284" y2="60" marker-end="url(#ua)"/>
    <line x1="162" y1="143" x2="184" y2="143" marker-end="url(#ua)"/>
    <line x1="336" y1="143" x2="358" y2="143" marker-end="url(#ua)"/>
    <line x1="510" y1="143" x2="538" y2="143" marker-end="url(#ua)"/>
  </g>
  <text x="12" y="200" font-size="10.5" fill="#555">Worked example (Inkling): the market-leader "home run" is only ~1% likely —</text>
  <text x="12" y="214" font-size="10.5" fill="#555">yet blended across all scenarios the deal still pencils to a 9× probability-weighted return.</text>
  <!-- bias chips -->
  <text x="12" y="240" font-size="11" font-weight="700" fill="#111">Biases the process is built to counter:</text>
  <g font-size="11">
    <rect x="12"  y="252" width="180" height="30" rx="15" fill="#fbe4ee" stroke="#e87ba4"/><text x="102" y="271" text-anchor="middle" fill="#8a2a52">representativeness (pattern-match)</text>
    <rect x="202" y="252" width="150" height="30" rx="15" fill="#fde3d6" stroke="#eb6834"/><text x="277" y="271" text-anchor="middle" fill="#9c3d13">confirmation bias</text>
    <rect x="362" y="252" width="120" height="30" rx="15" fill="#fdeecb" stroke="#eda100"/><text x="422" y="271" text-anchor="middle" fill="#8a6200">anchoring</text>
  </g>
</svg>
</div>

The single most useful idea I take from it: **the chasm is a technology-readiness question
dressed up as a go-to-market question.** A device that works in a paper but needs three more
material-science miracles to ship isn't an early-stage deal — it's a research grant, and the
decision tree prices it as such. Which is exactly why the next section is about readiness,
not novelty.

---

## 3. The twist: novelty is cheap, readiness is the edge

Here is where I diverge from the usual "next-gen compute" enthusiasm. I recently went deep on
the alternative-compute landscape — biological, quantum, analog, and photonic — mapping each
paradigm's energy-efficiency claim against its **actual technology-readiness level (TRL)**.
The efficiency headlines are staggering (DNA compute ~10⁹× more efficient than silicon;
photonic processors claiming ~30× versus CMOS). But headlines don't ship.

When you plot readiness instead of press releases, the field splits cleanly:

<div class="fig" markdown="0">
<svg viewBox="0 0 720 300" width="100%" style="max-width:720px;height:auto;font-family:system-ui,Segoe UI,Arial,sans-serif" role="img" aria-label="TRL by compute paradigm">
  <text x="12" y="20" font-size="13" font-weight="700" fill="#111">Energy-efficient compute paradigms, by technology readiness (TRL 1–9)</text>
  <!-- deployable band: TRL 7–9 => x 540..700 -->
  <rect x="540" y="40" width="160" height="220" fill="#e8f6ef"/>
  <text x="545" y="34" font-size="10.5" fill="#0d6b49" font-weight="700">TRL 7–9 · shippable</text>
  <!-- grid: x scale 60..700 over TRL 1..9 => 80px per TRL -->
  <g font-size="9" fill="#999">
    <line x1="60" y1="260" x2="700" y2="260" stroke="#ccc"/>
    <line x1="60" y1="40" x2="60" y2="260" stroke="#ccc"/>
    <text x="60" y="274">TRL 1</text><text x="516" y="274">TRL 7</text><text x="676" y="274">TRL 9</text>
  </g>
  <g font-size="12">
    <rect x="60" y="48"  width="140" height="26" rx="4" fill="#c9b8e8"/><text x="208" y="66" fill="#4a3aa7">Biocomputing · TRL 2–4</text>
    <rect x="60" y="86"  width="220" height="26" rx="4" fill="#f6c6a0"/><text x="288" y="104" fill="#9c3d13">Quantum · TRL 2–5</text>
    <rect x="60" y="124" width="460" height="26" rx="4" fill="#f3d98a"/><text x="70" y="142" fill="#7a5600" font-weight="700">Neuromorphic / analog · TRL 4–7</text>
    <rect x="60" y="162" width="540" height="26" rx="4" fill="#a9d6c4"/><text x="70" y="180" fill="#0d6b49" font-weight="700">Photonic compute · TRL 4–7</text>
    <rect x="60" y="200" width="640" height="26" rx="4" fill="#2a78d6"/><text x="70" y="218" fill="#fff" font-weight="700">Photonic data-centre I/O · TRL 9</text>
  </g>
</svg>
</div>

Bio and quantum are extraordinary science and, for a fund with my mandate, still pre-chasm.
**Analog** and **photonics** are the two that have reached TRL 7–9 — meaning first products,
real customers, manufacturable process. That is not a small distinction; it is the entire
difference between a venture bet and a science project. So I split the investable surface
into two theses:

- **Analog → edge AI inference.** In-memory and neuromorphic devices compute where the data
  is, at microwatts, tolerating the precision loss that edge workloads forgive. The moat is
  device physics; the risk is the software stack.
- **Photonics → data-centre I/O.** Moving bits as light instead of copper is the nearest-term,
  highest-TRL win, because the bottleneck in AI data centres has shifted from FLOPs to the
  interconnect and its power.

And the second thesis now has undeniable **market pull**. In March 2026, NVIDIA committed
**\$2 billion each to Coherent and Lumentum** — a \$4B bet that silicon photonics is how you
fix AI's copper bottleneck. When the company that defines the workload starts vertically
integrating the optical layer, the layer is no longer speculative; it is strategic.

This is also visible if you take a bird's-eye view of an AI data centre and follow the
capex: as accelerators scale out, a fast-growing share of the bill moves off the chip and
into the **interconnect, the power delivery, and the cooling** — the systems layer. Photonic
I/O attacks the first of those directly, and the power budget with it. That is a structural
shift in *where* the money is spent, not a cyclical one.

---

## 4. The deals: what my radar surfaces at the shippable layers

Thesis without pipeline is a blog post. So here are early-stage European companies at exactly
these two layers — every one **sourced and classified by the tool described in the next
section**, then read through the value-chain + readiness lens above. Verdicts are mine.

<div class="deals" markdown="0">
<table style="width:100%;border-collapse:collapse;font-size:13px;font-family:system-ui,Segoe UI,Arial,sans-serif">
<thead><tr style="background:#164a8f;color:#fff;text-align:left">
<th style="padding:7px 9px">Company</th><th style="padding:7px 9px">Layer</th><th style="padding:7px 9px">Why it can be defended</th><th style="padding:7px 9px">Verdict</th></tr></thead>
<tbody>
<tr style="border-bottom:1px solid #e6e6e6"><td style="padding:7px 9px"><b>Scintil Photonics</b> · FR · Series B</td><td style="padding:7px 9px">Photonic I/O</td><td style="padding:7px 9px">Monolithic DWDM light engines on silicon — the exact interconnect layer NVIDIA just paid $4B to secure.</td><td style="padding:7px 9px;color:#0d6b49;font-weight:700">SELECT</td></tr>
<tr style="border-bottom:1px solid #e6e6e6;background:#fafbfc"><td style="padding:7px 9px"><b>Q.ANT</b> · DE · Series A</td><td style="padding:7px 9px">Photonic compute</td><td style="padding:7px 9px">Native photonic processor claiming ~30× energy efficiency; first commercial silicon + a data-centre customer.</td><td style="padding:7px 9px;color:#0d6b49;font-weight:700">SELECT</td></tr>
<tr style="border-bottom:1px solid #e6e6e6"><td style="padding:7px 9px"><b>Finchetto</b> · UK · pre-seed</td><td style="padding:7px 9px">Photonic I/O</td><td style="padding:7px 9px">Fully-passive optical switch — no electronics in the fabric; 26–53× power cut, ~40 ns latency. Physics-level moat.</td><td style="padding:7px 9px;color:#0d6b49;font-weight:700">SELECT</td></tr>
<tr style="border-bottom:1px solid #e6e6e6;background:#fafbfc"><td style="padding:7px 9px"><b>Salience Labs</b> · UK/DE · seed</td><td style="padding:7px 9px">Photonic compute</td><td style="padding:7px 9px">Photonic multi-chip processor + all-optical connectivity (Oxford / Münster). Strong physics, watch the software path.</td><td style="padding:7px 9px;color:#b06a00;font-weight:700">WATCH</td></tr>
<tr style="border-bottom:1px solid #e6e6e6"><td style="padding:7px 9px"><b>Linq / Moon Photonics</b> · DE · seed</td><td style="padding:7px 9px">Photonic I/O</td><td style="padding:7px 9px">Photonic-integrated-circuit modules for HPC/data-centre links — lab-origin, early, capital-efficient.</td><td style="padding:7px 9px;color:#b06a00;font-weight:700">WATCH</td></tr>
<tr style="border-bottom:1px solid #e6e6e6;background:#fafbfc"><td style="padding:7px 9px"><b>Axelera AI</b> · NL · Series B</td><td style="padding:7px 9px">Analog / edge</td><td style="padding:7px 9px">In-memory compute for edge inference; furthest-along European edge-AI silicon. Moat is real; competition is fierce.</td><td style="padding:7px 9px;color:#0d6b49;font-weight:700">SELECT</td></tr>
<tr style="border-bottom:1px solid #e6e6e6"><td style="padding:7px 9px"><b>SpiNNcloud</b> · DE · commercial</td><td style="padding:7px 9px">Neuromorphic</td><td style="padding:7px 9px">Brain-inspired supercompute (TU Dresden / Human Brain Project), EIC-backed. Market fit still forming.</td><td style="padding:7px 9px;color:#b06a00;font-weight:700">WATCH</td></tr>
<tr style="border-bottom:1px solid #e6e6e6;background:#fafbfc"><td style="padding:7px 9px"><b>Rayd Technologies</b> · UK · pre-seed</td><td style="padding:7px 9px">Photonic-neuromorphic</td><td style="padding:7px 9px">Genuine architecture (photonic + neuromorphic), earliest-stage; adoption rests on a software stack it doesn't yet have.</td><td style="padding:7px 9px;color:#8a6200;font-weight:700">CONDITIONAL</td></tr>
</tbody></table>
</div>

The pattern is deliberate: I **select** on defensible physics *with* a credible adoption
path, **watch** where the physics is real but the software moat is unproven, and hold
**conditional** on architectures that need a stack they haven't built. Same discipline as
the value chain — a device only counts if the layer above it can't route around it.

Explore the full, live dataset here:
[**the Compute Radar dashboard →**](https://harsh010102.github.io/compute-radar-eu/dashboard/)

---

## 5. The tool: sourcing lab-origin deals before the market prices them

Every company above came out of a system I built on one conviction: **deep tech is born in
university and PhD research, so the incubator — not the funding announcement — is the
earliest honest signal.** By the time a hardware company shows up in a funding database with
a priced round, you are late. The lead time *is* the edge.

So the radar goes to the source. It doesn't scrape Crunchbase; it watches ~30 EU and North
American **compute incubators and research-lab accelerators**, enriches them from the
regional startup press those databases themselves ingest, and runs each candidate through a
small **multi-agent pipeline**.

<div class="fig" markdown="0">
<svg viewBox="0 0 720 250" width="100%" style="max-width:720px;height:auto;font-family:system-ui,Segoe UI,Arial,sans-serif" role="img" aria-label="Compute Radar architecture">
  <defs><marker id="ar" markerWidth="8" markerHeight="8" refX="6" refY="3" orient="auto"><path d="M0,0 L6,3 L0,6 Z" fill="#888"/></marker></defs>
  <g font-size="11.5">
    <rect x="10" y="60" width="130" height="70" rx="7" fill="#eef3fb" stroke="#2a78d6"/>
    <text x="75" y="82" text-anchor="middle" font-weight="700" fill="#164a8f">Sources</text>
    <text x="75" y="100" text-anchor="middle" fill="#333">~30 incubators</text>
    <text x="75" y="115" text-anchor="middle" fill="#333">lab accelerators</text>

    <rect x="180" y="30" width="150" height="60" rx="7" fill="#fef1e9" stroke="#eb6834"/>
    <text x="255" y="52" text-anchor="middle" font-weight="700" fill="#9c3d13">Scout agent</text>
    <text x="255" y="70" text-anchor="middle" fill="#333">Exa semantic search</text>
    <text x="255" y="84" text-anchor="middle" fill="#333">+ RSS / news</text>

    <rect x="180" y="100" width="150" height="60" rx="7" fill="#fdf6e0" stroke="#eda100"/>
    <text x="255" y="122" text-anchor="middle" font-weight="700" fill="#8a6200">Analyst agent</text>
    <text x="255" y="140" text-anchor="middle" fill="#333">LLM classify →</text>
    <text x="255" y="153" text-anchor="middle" fill="#333">8-layer taxonomy</text>

    <rect x="370" y="65" width="150" height="60" rx="7" fill="#e8f6ef" stroke="#1baf7a"/>
    <text x="445" y="87" text-anchor="middle" font-weight="700" fill="#0d6b49">Patent verify</text>
    <text x="445" y="105" text-anchor="middle" fill="#333">EPO OPS check</text>
    <text x="445" y="118" text-anchor="middle" fill="#333">(is the IP real?)</text>

    <rect x="560" y="65" width="150" height="60" rx="7" fill="#eef3fb" stroke="#164a8f"/>
    <text x="635" y="87" text-anchor="middle" font-weight="700" fill="#164a8f">Radar dashboard</text>
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
  <text x="12" y="20" font-size="13" font-weight="700" fill="#111">Compute Radar — an incubator-first, patent-verified sourcing pipeline</text>
  <text x="12" y="230" font-size="10.5" fill="#666">Free / open tooling · runs on a schedule · every company classified against a fixed 8-layer compute taxonomy.</text>
</svg>
</div>

The design choices are the argument:

- **Incubator-first, not database-first** — because non-dilutive incubator money attaches
  months before a priced round. That is the sourcing alpha.
- **A fixed 8-layer taxonomy** (substrate, architecture, interconnect, power/thermal,
  packaging, co-design/EDA, sovereign edge, sovereign cloud) — so classification is
  testable and the dataset is filterable in the fund's own language.
- **Patent verification via the EPO** — the Analyst can be seduced by a good tagline; a
  patent family is harder to fake. This is the first, automated pass of technical
  due diligence.
- **Provider-agnostic LLMs with fallback** — it runs on free/open tooling on a schedule,
  not a paid data subscription.

**Where it goes next.** The EPO check today answers *"does the IP exist?"* The natural
extension is to answer *"is the IP any good?"* — wiring the pipeline into full patent
databases for **claims parsing and citation analysis**, so the tool can flag genuine
device-level differentiation from defensive filing. That turns the radar from a sourcing
engine into a first-pass technical-DD engine — the exact judgement I'd otherwise do by hand.

---

## 6. What I'm actually claiming

Strip it back to the decision:

- **Back the bottom of the stack** — substrate and systems, where moats are kept, not
  applications, where margin is loud but defensibility is thin.
- **Underwrite readiness, not novelty** — of the exotic paradigms, only **analog** (edge AI)
  and **photonics** (data-centre I/O) have crossed into TRL 7–9. That is where a fund can
  deploy conviction now; bio and quantum are a watch-list.
- **Follow the strategic pull** — NVIDIA's \$4B into Coherent and Lumentum is the clearest
  signal that the photonic I/O layer is where the next decade of AI-infra capex concentrates.
- **Source from the lab** — track research-aligned incubators and verify with patents, and
  you see the defensible companies before the market prices them.

I'm an AI researcher who builds the systems *and* reads the balance sheet — I'd rather ship
the tool that finds the deal than argue about the deal in the abstract. If you want to see
the person behind the thesis, the projects, and the code:
[**explore my desktop portfolio → harsh97**](https://harsh010102.github.io/harsh97/).

---

*Sources & method: [FourWeekMBA — AI Value Chain (2026)](https://fourweekmba.com/ai-value-chain-2026/);
[Ulu Ventures decision analysis](https://www.youtube.com/watch?v=Wi3PiZsIfBU);
["The AI Data Center Explained"](https://www.youtube.com/watch?v=ckoi0RTEgcY);
NVIDIA's March 2026 \$2B-each investments in Coherent and Lumentum (widely reported);
company facts and classifications from my own [Compute Radar](https://harsh010102.github.io/compute-radar-eu/dashboard/)
dataset (incubator pages, EU-Startups, EPO filings); TRL assessment from my deep-dive on
alternative-compute paradigms.*
