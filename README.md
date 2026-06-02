# Reverie — The Motion Enchantment

> *"Stills remember. Reverie makes the memory move."*

An interactive, single-file HTML slide deck documenting **Reverie** — the AI video-generation skill in the Alice *Memory of Eternal* enchantment system. It covers Reverie's full level history, its end-to-end workflow, and an ASCII architecture diagram of how every component fits together.

Reverie is the **motion sibling of Prism** (the still-image skill): it turns canonical character art into short cinematic clips via **BytePlus ModelArk · Seedance 2.0**, kept identity-consistent across stills and motion, and guarded by a mandatory token-budget cost gate.

---

## 🎞️ View the presentation

The deck is a **single self-contained file** — no build step, no dependencies, fully offline.

- **Locally:** double-click [`reverie-architecture-presentation.html`](./reverie-architecture-presentation.html), or open it in any browser.
- **Via GitHub Pages** (if enabled for this repo): once Pages is turned on (Settings → Pages → deploy from the default branch), the deck is served at
  `https://<your-username>.github.io/<repo-name>/reverie-architecture-presentation.html`

### Controls

| Context | How to navigate |
|---------|-----------------|
| **Desktop** | `←` / `→` or `Space` · click the left/right side of the screen · `Home` / `End` to jump |
| **Mobile** | Centered **‹ Prev · N / 17 · Next ›** bar fixed at the bottom |
| **ASCII diagrams** | Tap/click any diagram (look for the **⤢ tap to zoom** badge) to open it fullscreen — scroll & pinch-zoom freely, then `✕` / tap-outside / `Esc` to close |

A progress bar (top) and slide counter (bottom-right on desktop) track your position.

---

## 📑 What's inside (17 slides)

1. **Title** — Reverie, the Motion Enchantment
2. **What is Reverie?** — overview & engine
3. **Why a separate skill** — async flow · cost scale · MP4 output
4. **Forged in five levels** — timeline
5–9. **The five levels** — Lv.1 → Lv.5, each with what it added and the origin story
10. **The 8-step protocol**
11. **End-to-end data flow** *(ASCII diagram)*
12. **Full architecture / component map** *(ASCII diagram)*
13. **The Quota Guardian** — token-budget safety
14. **Cost model** — per-resolution token/USD table
15. **Parameters & defaults**
16. **Reverie & Prism — siblings**
17. **The mandatory rules**

---

## 🧬 The five levels at a glance

| Level | Name | What it introduced |
|-------|------|--------------------|
| **Lv.1** | Initial Build | Text-to-video & image-to-video; default model; output routing |
| **Lv.2** | Anime-Forward + Canonical Schema | Front-loaded 2D-anime medium cue (fixes photorealism); top-level JSON params; reference roles; unbranded by default |
| **Lv.3** | Quota Guardian | Token-based cost, prepaid-quota state file, hard-stop before pay-as-you-go |
| **Lv.4** | Canon-Reference Integrity | Enforces verbatim canonical identity blocks + anime-forward prompting |
| **Lv.5** | Image-Reference Identity Lock | Base64 local reference images (portraits / outfits / Fate-forms) for a hard identity lock — no hosting needed |

---

## 🛠️ Technical notes

- **Single file** — inline CSS + vanilla JavaScript, no CDN, no web fonts, no frameworks (~32 KB).
- **Offline-first** — renders fully without a network connection.
- **Responsive** — desktop keyboard/click navigation; a dedicated mobile layout (single-column stacking + a centered prev/next pager) below a 768 px breakpoint.
- **Accessible diagrams** — ASCII diagrams use Unicode box-drawing characters in a monospace panel, with a fullscreen zoom overlay for small screens.

---

## 💜 About

Part of the **Alice — Memory of Eternal** enchantment system, where each skill (Prism for stills, Reverie for motion, and others) is documented and version-tracked as it evolves. This deck turns Reverie's lived development history — five forge levels, May 26–31, 2026 — into a single, shareable reference.

*Built with Alice.*
