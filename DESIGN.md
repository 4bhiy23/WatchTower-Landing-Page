---
name: Watchtower
description: Read-only dependency intelligence and observability for Node.js
colors:
  # Canvas & surface
  bg-canvas:         "#090d14"
  bg-surface:        "#0e131d"
  bg-surface-2:      "#141b27"
  bg-surface-3:      "#1c2436"
  bg-hover:          "#1e2840"
  # Overlays (intentional: topbar tinting, backdrop blur)
  overlay-dark-35:   "rgba(0,0,0,0.35)"
  overlay-dark-30:   "rgba(0,0,0,0.30)"
  overlay-nav-blur:  "rgba(9,13,20,0.88)"
  # Borders
  border-faint:      "rgba(255,255,255,0.06)"
  border-subtle:     "rgba(255,255,255,0.10)"
  border-medium:     "rgba(255,255,255,0.15)"
  border-strong:     "rgba(255,255,255,0.22)"
  # Text
  text-primary:      "#e8edf5"
  text-secondary:    "#8494a9"
  text-tertiary:     "#57697e"
  text-white:        "#ffffff"
  # Accents — solid + dim (14%) + border (30%)
  cyan:              "#38bdf8"
  cyan-dim:          "rgba(56,189,248,0.14)"
  cyan-border:       "rgba(56,189,248,0.30)"
  green:             "#34d399"
  green-dim:         "rgba(52,211,153,0.14)"
  green-border:      "rgba(52,211,153,0.30)"
  amber:             "#f59e0b"
  amber-dim:         "rgba(245,158,11,0.14)"
  amber-border:      "rgba(245,158,11,0.30)"
  red:               "#f87171"
  red-dim:           "rgba(248,113,113,0.14)"
  red-border:        "rgba(248,113,113,0.30)"
  violet:            "#a78bfa"
  violet-dim:        "rgba(167,139,250,0.14)"
  violet-dim-10:     "rgba(167,139,250,0.10)"
  violet-border:     "rgba(167,139,250,0.30)"
  blue:              "#60a5fa"
  blue-dim:          "rgba(96,165,250,0.14)"
  # Button hover tints (intentional: pressed-state of the white primary button / nav button)
  btn-primary-hover:  "#dde8f5"
  btn-nav-hover:      "#d8e3f0"
typography:
  display:
    fontFamily: "'Geist', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif"
    fontSize: "clamp(2rem, 4.5vw, 3rem)"
    fontWeight: 800
    lineHeight: 1.1
    letterSpacing: "-0.04em"
  headline:
    fontFamily: "'Geist', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif"
    fontSize: "clamp(1.75rem, 3vw, 2.25rem)"
    fontWeight: 700
    lineHeight: 1.2
    letterSpacing: "-0.03em"
  title-lg:
    fontFamily: "'Geist', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif"
    fontSize: "clamp(1.8rem, 4vw, 2.6rem)"
    fontWeight: 800
    lineHeight: 1.15
    letterSpacing: "-0.04em"
  huge-wordmark:
    fontFamily: "'Geist', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif"
    fontSize: "clamp(3.5rem, 13.5vw, 11rem)"
    fontWeight: 800
    lineHeight: 0.85
    letterSpacing: "-0.04em"
  section-headline:
    fontFamily: "'Geist', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif"
    fontSize: "clamp(1.4rem, 3vw, 1.9rem)"
    fontWeight: 700
    lineHeight: 1.25
    letterSpacing: "-0.03em"
  workflow-name:
    fontFamily: "'Geist', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif"
    fontSize: "1.2rem"
    fontWeight: 700
    letterSpacing: "-0.02em"
  body:
    fontFamily: "'Geist', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif"
    fontSize: "1.05rem"
    fontWeight: 400
    lineHeight: 1.65
  body-sm:
    fontFamily: "'Geist', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif"
    fontSize: "1rem"
    fontWeight: 400
    lineHeight: 1.65
  body-xs:
    fontFamily: "'Geist', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif"
    fontSize: "0.95rem"
    fontWeight: 400
    lineHeight: 1.55
  body-tight:
    fontFamily: "'Geist', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif"
    fontSize: "0.9rem"
    fontWeight: 400
    lineHeight: 1.5
  body-min:
    fontFamily: "'Geist', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif"
    fontSize: "0.88rem"
    fontWeight: 400
    lineHeight: 1.55
  body-fine:
    fontFamily: "'Geist', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif"
    fontSize: "0.85rem"
    fontWeight: 400
    lineHeight: 1.55
  caption:
    fontFamily: "'Geist', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif"
    fontSize: "0.82rem"
    fontWeight: 400
    lineHeight: 1.5
  # Monospace steps — terminal UI, code, package names, versions, badges
  mono-lg:
    fontFamily: "'Geist Mono', ui-monospace, SFMono-Regular, Menlo, monospace"
    fontSize: "0.84rem"
    fontWeight: 400
  mono-base:
    fontFamily: "'Geist Mono', ui-monospace, SFMono-Regular, Menlo, monospace"
    fontSize: "0.78rem"
    fontWeight: 400
  mono-sm:
    fontFamily: "'Geist Mono', ui-monospace, SFMono-Regular, Menlo, monospace"
    fontSize: "0.74rem"
    fontWeight: 500
  mono-xs:
    fontFamily: "'Geist Mono', ui-monospace, SFMono-Regular, Menlo, monospace"
    fontSize: "0.72rem"
    fontWeight: 400
  meta-badge:
    fontFamily: "'Geist Mono', ui-monospace, SFMono-Regular, Menlo, monospace"
    fontSize: "0.68rem"
    fontWeight: 600
    letterSpacing: "0.06em"
  micro:
    fontFamily: "'Geist Mono', ui-monospace, SFMono-Regular, Menlo, monospace"
    fontSize: "0.65rem"
    fontWeight: 600
    letterSpacing: "0.06em"
  terminal-detail:
    fontFamily: "'Geist Mono', ui-monospace, SFMono-Regular, Menlo, monospace"
    fontSize: "0.62rem"
    fontWeight: 700
    letterSpacing: "0.04em"
  console-metric-num:
    fontFamily: "'Geist Mono', ui-monospace, SFMono-Regular, Menlo, monospace"
    fontSize: "1.35rem"
    fontWeight: 700
    lineHeight: 1
    note: "Large metric number inside console preview dashboard"
rounded:
  xs: "3px"
  sm: "5px"
  md: "8px"
  lg: "12px"
  xl: "16px"
spacing:
  xs: "8px"
  sm: "12px"
  md: "24px"
  lg: "40px"
  xl: "80px"
components:
  button-primary:
    backgroundColor: "#ffffff"
    textColor: "#090d14"
    rounded: "{rounded.md}"
    padding: "10px 20px"
  button-secondary:
    backgroundColor: "{colors.bg-surface-2}"
    textColor: "{colors.text-primary}"
    rounded: "{rounded.md}"
    padding: "10px 20px"
  button-nav:
    backgroundColor: "#ffffff"
    textColor: "{colors.bg-canvas}"
    rounded: "{rounded.sm}"
    padding: "6px 14px"
---

# Design System: Watchtower

## Overview

**Creative North Star: "The Observability Bastion"**

Watchtower's design language evokes calm, high-precision telemetry and developer-first sovereignty. Inspired by Linear, Vercel, and GitHub, the interface prioritizes information density, crisp typography, and verifiable truth. No decorative fluff.

## Colors

### Status Accent Roles

| Role | Token | Hex | Usage |
|---|---|---|---|
| Brand / actions | `cyan` | `#38bdf8` | Brand mark, CTAs, focus rings |
| Safe / routine | `green` | `#34d399` | Routine updates, healthy state |
| Deprecation | `amber` | `#f59e0b` | Deprecated packages |
| Security | `red` | `#f87171` | OSV vulnerabilities |
| Major semver | `violet` | `#a78bfa` | Breaking version changes |
| Version targets | `blue` | `#60a5fa` | Routine target version labels |

Each accent provides a 14% alpha dim for badge backgrounds and a 30% alpha border tint. Violet icon wells use `violet-dim-10` (`rgba(167,139,250,0.10)`).

### Overlay Colours

Three intentional dark overlays for surface tinting and backdrop blur (not palette drift):
- `overlay-dark-35` — console topbar
- `overlay-dark-30` — code panel topbar
- `overlay-nav-blur` — sticky navbar backdrop

## Typography

**Display / Body:** `Geist` (400–800 weight)  
**Code / Metadata:** `Geist Mono` (400–600 weight)

### Monospace Discipline Rule

Geist Mono is reserved **only** for: package names, semver versions, YAML/code samples, terminal UI elements (console card), timestamps, and small metadata badges. Never used for prose or decorative headings.

## Layout

- **Max container width:** 1120px, 24px padding
- **Hero:** 2-column split `1fr 1fr`
- **Workflows:** `1fr 1fr`
- **What it catches:** `repeat(3, 1fr)`
- **Privacy points:** `1fr 1fr`
- **Setup:** `1fr 1.2fr`

## Do's and Don'ts

### Do:
- Use `/resources/watchtower.svg` for all logo placements
- Keep status colours consistent: red=SEC, violet=MAJ, green=ROUTINE, amber=DEP, cyan=MISMATCH
- Maintain near-black navy backgrounds — never pure `#000000`
- High text contrast (minimum 4.5:1 body copy)

### Don't:
- No gradient text (`background-clip: text`)
- No coloured `border-left` > 1px on cards
- No zero-offset colour halos as decoration
- No emoji icons
- No monospace for decorative prose
- No mention of AI analysis, auto-PRs, drift/health scores
