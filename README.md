# Kasturi Baag — Mango Manager
### A real ops tool for a real family farm. Built with love, a little code, and some AI.

---

## The backstory

My father Dagaji spent 35 years as a schoolteacher in a small town near Nashik. When he retired, he didn't slow down — he started farming. Today, our family owns 3+ acres in Chandwad, Nashik, with 2,000+ trees: mango, coconut, chickoo, papaya, custard apple, mahogani, avocado, litchi, banana. No chemicals. No pesticides. Just soil, patience, and my mother Suman tending to it like a second home.

In 2026, I decided to sell the mangoes — Chandwad Hapus, one of the most prized Alphonso varieties — to my network: IIM Lucknow alumni, friends, and colleagues. It started as a casual thing. It became a small operation that needed real tooling.

---

## The problem

Orders came in through WhatsApp. Dozens of them, in every format imaginable.

> *"Bhai 2 boxes 3kg each, Powai, same address as last time"*  
> *"Hi Jayesh! Can I get 5kg for my mom in Pune? She prefers no ripe ones."*  
> *"1 box 5kg, IIMA alumni pricing please"*

I was copying these into a notebook, losing track of who paid, who got delivery, who wanted a repeat next week. A notebook doesn't scale. A spreadsheet felt wrong. I needed something built exactly for this.

So I built it.

---

## What this is

**Mango Manager** is a single-page web app that handles the full order lifecycle for a small direct-to-consumer farm business.

### Core features

- **AI-powered WhatsApp parser** — Paste any message and the app calls Claude (Anthropic) to extract customer name, quantity, variety, delivery address, and special notes into a structured order. One click, no transcription.
- **Customer CRM with autocomplete** — Returning customers are recognized and auto-filled. Repeat order in two clicks.
- **Two pricing tiers** — IIM-L Alumni (₹xxx/5kg, ₹xxxx/7kg) and Standard (₹xxx/5kg). Pricing is configurable in Settings.
- **Order lifecycle tracking** — Each order tracks delivery status and payment status with inline dropdowns. No external tool needed.
- **Summary analytics** — Season totals by customer group. Revenue, boxes, average order size.
- **Export** — Full order data as CSV or XLSX. Import CSV for bulk loads.
- **Runs entirely in the browser** — No server, no database. Data lives in IndexedDB on the device.

### The AI piece (specifically)

The WhatsApp parser isn't decorative. It solves a real friction point: unstructured text → structured record, in under 2 seconds. Without it, every order requires manual field entry and the risk of a typo in a delivery address or wrong quantity. With it, the cognitive load drops to "read the message, confirm the parse, save."

That's what good AI integration looks like in a small product: invisible when it works, obviously valuable when you've lived without it.

---

## Season 2026 — what actually happened

- Sold to customers across two groups: IIM-L alumni network and personal contacts
- Every order tracked from WhatsApp → delivery → payment in the app
- Zero missed payments, zero lost orders
- Included a handwritten-style note card with every delivery — the [Kasturi Baag chit](chit/kasturi-baag-chit.md) — a small story about the farm and the family behind it

---

## Where this could go (v3 thinking)

A few things I'd build next if I ran this as a real product:

**Demand forecasting** — Two seasons of order data tells you a lot. What quantity to expect, which customer segment reorders, which week peaks. A small model on top of the order history could inform how many boxes to prep before the season starts.

**Proactive outreach drafts** — "Based on last year, 12 customers haven't ordered yet. Here's a draft WhatsApp message for each." AI-generated, human-sent.

**Pre-season waitlist + allocation** — Supply is fixed. Trees produce what they produce. A waitlist system that allocates fairly (loyal customers first, new requests queued) would be valuable when demand exceeds supply — which it did.

**Auto-generated order confirmations** — Parse the order, confirm it back in WhatsApp format with all details. Copy-paste, no composition needed.

**Farm story CMS** — The Kasturi Baag chit resonated. Building a simple way to update the seasonal story and regenerate the printable card would make that part scalable.

---

## Why this is on GitHub

Partly because the code is worth sharing. Mostly because this project taught me something I try to apply at work too: the best products are built for problems you've actually lived, not problems you've imagined.

The same instinct that made me build this — "I have a real problem, what's the minimum viable solution, where does AI actually help?" — is how I approach product work in industrial AI at Haber.

This is Kasturi Baag. It was never a business plan. It was a calling.

---

## Tech

- Vanilla HTML/CSS/JS — single file, no build step
- [Anthropic Claude API](https://www.anthropic.com) — WhatsApp message parsing
- IndexedDB — client-side persistence
- SheetJS — Excel export
- DM Serif Display + DM Sans — because it should feel good to look at

---

## The family

**Dagaji Bachhav** — retired schoolteacher, farmer, the reason any of this exists.  
**Suman Bachhav** — retired teacher, keeps the farm running day to day.  
**Prerana Bachhav** — VIT Vellore, future engineer, occasional packing assistant.  
**Jayesh Bachhav** — CoEP + IIM Lucknow, built the app, handled sales, ate too many mangoes.

---

*Chandwad, Nashik · Season 2026*
