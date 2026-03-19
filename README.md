# Q-Shield: AI-Powered Parametric Income Insurance for Q-Commerce Delivery Workers

> **Guidewire DEVTrails 2026 | Phase 1 Submission**  
> Protecting the last-mile workforce — one week at a time.

---

## Table of Contents

1. [The Problem](#the-problem)
2. [Our Persona](#our-persona)
3. [Solution Overview](#solution-overview)
4. [Weekly Premium Model](#weekly-premium-model)
5. [Parametric Triggers](#parametric-triggers)
6. [Application Workflow](#application-workflow)
7. [AI/ML Integration Plan](#aiml-integration-plan)
8. [Adversarial Defense & Anti-Spoofing Strategy](#adversarial-defense--anti-spoofing-strategy)
9. [Architecture Overview](#architecture-overview)
10. [Tech Stack](#tech-stack)
11. [Platform Choice: Web (PWA)](#platform-choice-web-pwa)

---

## The Problem
India's 2M q-commerce riders (Zepto, Blinkit, Swiggy Instamart) live paycheck-to-paycheck. One flood, curfew, or AQI spike wipes out 20-30% of their weekly earnings. No backup exists.

When orders stop, earnings stop. There is no employer backup, no union protection, and no insurance product designed for their reality.

<p align="center">
  <img width="856" height="384" alt="Screenshot 2026-03-19 at 10 24 05 PM" src="https://github.com/user-attachments/assets/1abb22ba-d7cb-482a-b46a-76de916c4679" />
</p>
 
 **The Opportunity:** 2M q-commerce workers × ₹100/week premium = ₹10,400Cr annual market
 
---
## Our Persona

### Arjun, 26 — Zepto Delivery Partner, Bengaluru

<div align="center">

| Attribute | Detail |
|-----------|--------|
| Platform | Zepto (primary), Blinkit (secondary) |
| City | Bengaluru (operates across Koramangala, HSR Layout, Indiranagar) |
| Weekly Earnings | ₹4,500 – ₹6,000 |
| Work Hours | 8–10 hrs/day, 6 days/week |
| Vehicle | Electric two-wheeler |
| Risk Exposure | Bengaluru monsoon floods, traffic lockdowns, AQI spikes (Oct–Nov) |

</div>

**The scenario that breaks Arjun:**

It's a Tuesday evening in July. Heavy rain triggers a red alert in 3 zones. Orders are suspended by the platform. Arjun loses ₹800–₹1,200 that day — with no recourse. This happens 6–8 times per monsoon season. Q-Shield pays out automatically, within minutes, with no claim form required.

---

## Solution Overview

Q-Shield is a **parametric income insurance platform** — meaning payouts are triggered by verifiable external events (weather, zone status, pollution data), not subjective loss assessments. No paperwork. No adjuster. No waiting.

**Coverage scope (strictly income loss only):**
- Lost earnings due to weather disruptions
- Lost earnings due to zone/area closures or curfews
- Lost earnings due to severe pollution (AQI > 300)
- Vehicle repairs (excluded)
- Health/accident/life insurance (excluded)

---

## Weekly Premium Model

Premiums are structured on a **weekly basis** to match the typical earnings cycle of a gig worker. Workers pay weekly, and coverage resets each Monday.

### Base Premium Table

<div align="center">

<table>
  <thead>
    <tr>
      <th style="padding:8px; border:1px solid #ddd;">Coverage Tier</th>
      <th style="padding:8px; border:1px solid #ddd;">Weekly Premium</th>
      <th style="padding:8px; border:1px solid #ddd;">Max Weekly Payout</th>
      <th style="padding:8px; border:1px solid #ddd;">Best For</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="padding:8px; border:1px solid #ddd;">Basic Shield</td>
      <td style="padding:8px; border:1px solid #ddd;">₹35/week</td>
      <td style="padding:8px; border:1px solid #ddd;">₹500</td>
      <td style="padding:8px; border:1px solid #ddd;">Part-time workers (&lt;5 hrs/day)</td>
    </tr>
    <tr>
      <td style="padding:8px; border:1px solid #ddd;">Standard Shield</td>
      <td style="padding:8px; border:1px solid #ddd;">₹65/week</td>
      <td style="padding:8px; border:1px solid #ddd;">₹1,000</td>
      <td style="padding:8px; border:1px solid #ddd;">Regular workers (5–8 hrs/day)</td>
    </tr>
    <tr>
      <td style="padding:8px; border:1px solid #ddd;">Pro Shield</td>
      <td style="padding:8px; border:1px solid #ddd;">₹99/week</td>
      <td style="padding:8px; border:1px solid #ddd;">₹1,800</td>
      <td style="padding:8px; border:1px solid #ddd;">Full-time workers (8+ hrs/day)</td>
    </tr>
  </tbody>
</table>

</div>

### Dynamic Risk Multipliers (AI-Adjusted)

The base premium is adjusted weekly by our ML risk engine based on:

<div align="center">

<table>
  <thead>
    <tr>
      <th style="padding:8px; border:1px solid #ddd;">Risk Factor</th>
      <th style="padding:8px; border:1px solid #ddd;">Adjustment</th>
      <th style="padding:8px; border:1px solid #ddd;">Rationale</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="padding:8px; border:1px solid #ddd;">Monsoon season (Jun–Sep)</td>
      <td style="padding:8px; border:1px solid #ddd;">+15%</td>
      <td style="padding:8px; border:1px solid #ddd;">Higher disruption probability</td>
    </tr>
    <tr>
      <td style="padding:8px; border:1px solid #ddd;">Worker's zone has flood history</td>
      <td style="padding:8px; border:1px solid #ddd;">+10%</td>
      <td style="padding:8px; border:1px solid #ddd;">Zone-level historical risk</td>
    </tr>
    <tr>
      <td style="padding:8px; border:1px solid #ddd;">Worker's zone is flood-safe</td>
      <td style="padding:8px; border:1px solid #ddd;">-8%</td>
      <td style="padding:8px; border:1px solid #ddd;">Reward low-risk zones</td>
    </tr>
    <tr>
      <td style="padding:8px; border:1px solid #ddd;">New worker (&lt; 4 weeks)</td>
      <td style="padding:8px; border:1px solid #ddd;">+5%</td>
      <td style="padding:8px; border:1px solid #ddd;">Limited behavioral baseline</td>
    </tr>
    <tr>
      <td style="padding:8px; border:1px solid #ddd;">Worker with 0 claims (3+ months)</td>
      <td style="padding:8px; border:1px solid #ddd;">-5%</td>
      <td style="padding:8px; border:1px solid #ddd;">Loyalty/low-risk bonus</td>
    </tr>
    <tr>
      <td style="padding:8px; border:1px solid #ddd;">Predicted high-disruption week (weather model)</td>
      <td style="padding:8px; border:1px solid #ddd;">+12%</td>
      <td style="padding:8px; border:1px solid #ddd;">Forward-looking risk pricing</td>
    </tr>
  </tbody>
</table>

</div>

**Example:** Arjun (Standard Shield, Koramangala zone, July monsoon season):  
`₹65 × 1.15 (monsoon) × 1.10 (flood-prone zone) = ₹82/week`

---

## Parametric Triggers

Q-Shield monitors **3 disruption categories** in real time using external APIs. When a threshold is crossed in a worker's active delivery zone, a claim is initiated automatically — no worker action required.

### Trigger 1: Extreme Weather (Rain / Flood)

<div align="center">

<table>
  <thead>
    <tr>
      <th style="padding:8px; border:1px solid #ddd;">Parameter</th>
      <th style="padding:8px; border:1px solid #ddd;">Source</th>
      <th style="padding:8px; border:1px solid #ddd;">Threshold</th>
      <th style="padding:8px; border:1px solid #ddd;">Payout</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="padding:8px; border:1px solid #ddd;">Rainfall intensity</td>
      <td style="padding:8px; border:1px solid #ddd;">OpenWeather API</td>
      <td style="padding:8px; border:1px solid #ddd;">> 15mm/hr OR Red Alert issued</td>
      <td style="padding:8px; border:1px solid #ddd;">50–100% of daily coverage</td>
    </tr>
    <tr>
      <td style="padding:8px; border:1px solid #ddd;">Flood zone activation</td>
      <td style="padding:8px; border:1px solid #ddd;">IMD / mock civic API</td>
      <td style="padding:8px; border:1px solid #ddd;">Zone flagged as flooded</td>
      <td style="padding:8px; border:1px solid #ddd;">100% of daily coverage</td>
    </tr>
  </tbody>
</table>

</div>

**Example:** IMD issues a Red Alert for Bengaluru South. All active Q-Shield workers in that zone receive an automatic payout notification within 10 minutes.

---

### Trigger 2: Zone/Area Closure

<div align="center">

<table>
  <thead>
    <tr>
      <th style="padding:8px; border:1px solid #ddd;">Parameter</th>
      <th style="padding:8px; border:1px solid #ddd;">Source</th>
      <th style="padding:8px; border:1px solid #ddd;">Threshold</th>
      <th style="padding:8px; border:1px solid #ddd;">Payout</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="padding:8px; border:1px solid #ddd;">Curfew / Section 144</td>
      <td style="padding:8px; border:1px solid #ddd;">Government API / mock</td>
      <td style="padding:8px; border:1px solid #ddd;">Zone closure confirmed</td>
      <td style="padding:8px; border:1px solid #ddd;">80% of daily coverage</td>
    </tr>
    <tr>
      <td style="padding:8px; border:1px solid #ddd;">Platform-side surge suspension</td>
      <td style="padding:8px; border:1px solid #ddd;">Mock platform API</td>
      <td style="padding:8px; border:1px solid #ddd;">Delivery suspension > 2 hrs</td>
      <td style="padding:8px; border:1px solid #ddd;">60% of daily coverage</td>
    </tr>
  </tbody>
</table>

</div>

---

### Trigger 3: Severe Air Pollution

<div align="center">

<table>
  <thead>
    <tr>
      <th style="padding:8px; border:1px solid #ddd;">Parameter</th>
      <th style="padding:8px; border:1px solid #ddd;">Source</th>
      <th style="padding:8px; border:1px solid #ddd;">Threshold</th>
      <th style="padding:8px; border:1px solid #ddd;">Payout</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="padding:8px; border:1px solid #ddd;">AQI index</td>
      <td style="padding:8px; border:1px solid #ddd;">CPCB API / OpenAQ</td>
      <td style="padding:8px; border:1px solid #ddd;">AQI > 300 (Hazardous)</td>
      <td style="padding:8px; border:1px solid #ddd;">50% of daily coverage</td>
    </tr>
    <tr>
      <td style="padding:8px; border:1px solid #ddd;">AQI + heat index combined</td>
      <td style="padding:8px; border:1px solid #ddd;">Composite score</td>
      <td style="padding:8px; border:1px solid #ddd;">Score > threshold</td>
      <td style="padding:8px; border:1px solid #ddd;">70% of daily coverage</td>
    </tr>
  </tbody>
</table>

</div>

---

## Application Workflow

![application-workflow](https://github.com/user-attachments/assets/69d7c33d-e64a-4c5e-8139-25eb0530efb1)


---

## AI/ML Integration Plan

<img width="1169" height="451" alt="AI-System" src="https://github.com/user-attachments/assets/6cdf9aef-6ecb-4d18-89b4-5ade6daacc9d" />


---

## Adversarial Defense & Anti-Spoofing Strategy

> This section directly addresses the **Market Crash Scenario** (March 2026): a 500-worker GPS-spoofing syndicate that drained a competitor's liquidity pool via coordinated false claims.

### 1. The Differentiation: Real Worker vs GPS Spoofer

<p align="center">
<b>Simple GPS verification is obsolete.</b> Q-Shield uses a <b>multi-signal verification stack</b> that cross-validates every claim against 6 independent signals simultaneously, making GPS spoofing alone completely ineffective.
</p>

<div align="center">

<table>
  <thead>
    <tr>
      <th style="padding:8px; border:1px solid #ddd;">Signal</th>
      <th style="padding:8px; border:1px solid #ddd;">What We Check</th>
      <th style="padding:8px; border:1px solid #ddd;">Why It's Hard to Fake</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="padding:8px; border:1px solid #ddd;"><b>Coarse IP Location</b></td>
      <td style="padding:8px; border:1px solid #ddd;">City/district from IP + carrier data</td>
      <td style="padding:8px; border:1px solid #ddd;">GPS can be faked; carrier cell-tower location cannot easily be spoofed remotely</td>
    </tr>
    <tr>
      <td style="padding:8px; border:1px solid #ddd;"><b>Device Fingerprint</b></td>
      <td style="padding:8px; border:1px solid #ddd;">OS version, screen resolution, dev mode status, rooted device flag</td>
      <td style="padding:8px; border:1px solid #ddd;">Spoofers typically use emulators or developer tools with detectable signatures</td>
    </tr>
    <tr>
      <td style="padding:8px; border:1px solid #ddd;"><b>Network Stability Pattern</b></td>
      <td style="padding:8px; border:1px solid #ddd;">WiFi vs mobile data, signal drop frequency</td>
      <td style="padding:8px; border:1px solid #ddd;">Real workers in a flood zone show unstable-but-consistent mobile data; a home spoofer shows stable WiFi</td>
    </tr>
    <tr>
      <td style="padding:8px; border:1px solid #ddd;"><b>Weather Coherence</b></td>
      <td style="padding:8px; border:1px solid #ddd;">API-reported weather at claimed location vs worker's claim</td>
      <td style="padding:8px; border:1px solid #ddd;">If the worker claims "heavy rain, zone A" but OpenWeather shows clear skies at that GPS coordinate — instant red flag</td>
    </tr>
    <tr>
      <td style="padding:8px; border:1px solid #ddd;"><b>Trip History Consistency</b></td>
      <td style="padding:8px; border:1px solid #ddd;">Historical delivery routes, average speed, zone frequency</td>
      <td style="padding:8px; border:1px solid #ddd;">Real workers have organic, consistent routes; GPS spoofers show unnatural teleportation or perfect grid patterns</td>
    </tr>
    <tr>
      <td style="padding:8px; border:1px solid #ddd;"><b>Behavioral Velocity</b></td>
      <td style="padding:8px; border:1px solid #ddd;">Time-delta between location pings vs physically possible travel speed</td>
      <td style="padding:8px; border:1px solid #ddd;">Claiming to be in two zones within an impossible timeframe is an automatic flag</td>
    </tr>
  </tbody>
</table>

</div>

**Scoring logic:**

Each signal produces a risk score between 0 and 1. The total fraud score is a **weighted average** of all six signals:

```
fraud_score = (
  0.20 × ip_mismatch_score +
  0.20 × device_anomaly_score +
  0.15 × network_pattern_score +
  0.25 × weather_coherence_score +
  0.10 × trip_history_score +
  0.10 × velocity_score
)
```

### Fraud Detection: Claim Scoring
<div align="center">

<table>
  <thead>
    <tr>
      <th style="padding:8px; border:1px solid #ddd;">Fraud Score</th>
      <th style="padding:8px; border:1px solid #ddd;">Decision</th>
      <th style="padding:8px; border:1px solid #ddd;">% of Claims (estimated)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="padding:8px; border:1px solid #ddd;">&lt; 0.3</td>
      <td style="padding:8px; border:1px solid #ddd;">Auto-approve + instant payout</td>
      <td style="padding:8px; border:1px solid #ddd;">~70%</td>
    </tr>
    <tr>
      <td style="padding:8px; border:1px solid #ddd;">0.3 – 0.7</td>
      <td style="padding:8px; border:1px solid #ddd;">Fast verification required</td>
      <td style="padding:8px; border:1px solid #ddd;">~20%</td>
    </tr>
    <tr>
      <td style="padding:8px; border:1px solid #ddd;">&gt; 0.7</td>
      <td style="padding:8px; border:1px solid #ddd;">Reject / manual review</td>
      <td style="padding:8px; border:1px solid #ddd;">~10%</td>
    </tr>
  </tbody>
</table>

</div>

---


### 2. The Data: Detecting Coordinated Fraud Rings

**500-worker syndicates** evade individual fraud scores. *Ring detection catches collusion.*

### Key Signals (Beyond GPS)
- **Temporal clustering:** 50+ claims/zone in 15 min *(normal: 0–2)*
- **Shared fingerprints:** Same OS/screen/carrier across accounts
- **IP overlap:** Same subnet claims city-wide disruption
- **Onboarding spikes:** 50+ accounts in 72 hrs
- **Claim velocity:** 10× historical baseline/zone

### DBSCAN Cluster Detection
```python
claims = get_claims(zone=X, time_bucket="15min")

if len(claims) > 10:
    if mean_fraud(claims) > 0.4 or shared_devices(claims) > 0.3:
        flag_ring(claims)
        suspend_payouts(zone=X)
        alert_admin()
```

**Real scenario:** 500 workers claiming "flood in Koramangala" at 8:47 PM while OpenWeather API shows clear skies → weather coherence score spikes to 0.95 for all claims → ring flag triggers immediately → entire batch suspended within seconds.

---

### 3. The UX Balance: Protecting Honest Workers

A Bengaluru delivery worker in an actual flood faces real compounding problems: poor GPS signal near dark stores, unstable 4G in waterlogged zones, and legitimate location anomalies (taking shelter in a different zone than their delivery route).

**Q-Shield's progressive verification flow ensures honest workers are never unfairly penalized:**

<img width="551" height="338" alt="Screenshot 2026-03-19 at 3 42 38 PM" src="https://github.com/user-attachments/assets/b170ff6e-9154-45a8-bcdc-b86208ba0ec2" />


**Key fairness principles baked into the system:**

1. **Never block an honest claim longer than 5 minutes** — the fast verification path is designed to be completable on a 2G connection with one hand while sheltering from rain.
2. **Network drops are not penalised** — we use "last known good location" + weather API correlation as the primary truth source, not real-time GPS lock.
3. **Zone-level context awareness** — if a disruption trigger (Red Alert) has already fired for that zone, the bar for individual claim approval is lowered, since the event is already independently verified.
4. **Human escalation is always available** — no worker is permanently rejected by an algorithm alone. Every fraud score > 0.7 goes to a human reviewer.
5. **Transparent feedback** — if a claim is flagged, the worker sees a plain-language explanation ("We're verifying your location — tap here to confirm") rather than a cryptic denial.

---

## Architecture Overview

![WhatsApp Image 2026-03-19 at 3 38 01 PM](https://github.com/user-attachments/assets/f4599732-5bf8-4de5-a50e-ee6015cb0962)


**Core data flows:**
1. **Onboarding:** Worker registers → ML service risk-scores profile → weekly premium quote generated → policy created on payment.
2. **Trigger monitoring:** Cron job polls weather + AQI + zone APIs every 5 minutes → disruption detected → auto-claim initiated for all active policyholders in affected zone.
3. **Claim processing:** Claim created → ML fraud service scores it → auto-approve or flag → payout dispatched via mock UPI.
4. **Admin dashboard:** Real-time claims map, fraud ring alerts, loss ratio analytics, manual review queue.

---

### Tech Stack

<div align="center">

<table>
  <thead>
    <tr>
      <th style="padding:8px; border:1px solid #ddd;">Layer</th>
      <th style="padding:8px; border:1px solid #ddd;">Technology</th>
      <th style="padding:8px; border:1px solid #ddd;">Rationale</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="padding:8px; border:1px solid #ddd;">Frontend</td>
      <td style="padding:8px; border:1px solid #ddd;">Next.js 15 (React + TypeScript)</td>
      <td style="padding:8px; border:1px solid #ddd;">PWA support, fast rendering, easy Vercel deploy</td>
    </tr>
    <tr>
      <td style="padding:8px; border:1px solid #ddd;">Backend API</td>
      <td style="padding:8px; border:1px solid #ddd;">Node.js + Express (TypeScript)</td>
      <td style="padding:8px; border:1px solid #ddd;">Familiar, fast to build, good ecosystem</td>
    </tr>
    <tr>
      <td style="padding:8px; border:1px solid #ddd;">ML Service</td>
      <td style="padding:8px; border:1px solid #ddd;">Python + FastAPI + scikit-learn</td>
      <td style="padding:8px; border:1px solid #ddd;">Isolated ML service, easy to iterate model</td>
    </tr>
    <tr>
      <td style="padding:8px; border:1px solid #ddd;">Database</td>
      <td style="padding:8px; border:1px solid #ddd;">PostgreSQL (Supabase)</td>
      <td style="padding:8px; border:1px solid #ddd;">Reliable, free tier, real-time subscriptions</td>
    </tr>
    <tr>
      <td style="padding:8px; border:1px solid #ddd;">Weather Data</td>
      <td style="padding:8px; border:1px solid #ddd;">OpenWeather API</td>
      <td style="padding:8px; border:1px solid #ddd;">Free tier, reliable, covers Indian cities well</td>
    </tr>
    <tr>
      <td style="padding:8px; border:1px solid #ddd;">Pollution Data</td>
      <td style="padding:8px; border:1px solid #ddd;">OpenAQ API</td>
      <td style="padding:8px; border:1px solid #ddd;">Free, covers Bengaluru AQI stations</td>
    </tr>
    <tr>
      <td style="padding:8px; border:1px solid #ddd;">Maps / Zones</td>
      <td style="padding:8px; border:1px solid #ddd;">Mapbox GL JS</td>
      <td style="padding:8px; border:1px solid #ddd;">Free tier sufficient for zone visualisation</td>
    </tr>
    <tr>
      <td style="padding:8px; border:1px solid #ddd;">Deployment</td>
      <td style="padding:8px; border:1px solid #ddd;">Vercel (frontend) + Railway (API + ML)</td>
      <td style="padding:8px; border:1px solid #ddd;">Free tiers, auto-deploy from GitHub</td>
    </tr>
  </tbody>
</table>

</div>

---

## Platform Choice: Web (PWA)

We chose a **Progressive Web App (PWA)** over a native mobile app for the following reasons:

1. **Zero install friction** — delivery workers can access Q-Shield via a link in WhatsApp without going to the app store. Adoption is everything.
2. **Works on low-end Android devices** — the majority of q-commerce workers use budget Android phones. A PWA with offline support handles poor network conditions better than a heavy native app.
3. **Faster to build and iterate** — one codebase (Next.js) serves both mobile web and desktop (admin view), maximising our small team's velocity.
4. **Push notifications supported** — PWAs on Android support push notifications, enabling real-time claim alerts to workers.

---

*Built for India's last-mile workforce.*  
*DEVTrails 2026 | Team Q-Shield*






