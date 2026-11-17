# Happy 19th, Keshav

A three-page personal website. Butter yellow, cappuccino brown, pale sky. Photographic, editorial, no cartoon anything.

```
keshav-19/
├── index.html            the birthday home
├── gpt.html              Lakshita GPT
├── temple.html           Vrindavan · Radha Raman
├── css/
│   ├── styles.css        shared design system
│   ├── gpt.css           the ChatGPT-style layout
│   └── temple.css        the temple + train journey
├── js/
│   ├── config.js   ←←←   ALL YOUR WORDS GO HERE
│   ├── main.js           home page behaviour
│   ├── gpt.js            Lakshita GPT behaviour
│   └── temple.js         temple + journey behaviour
└── assets/photos/        the 12 generated photographs
```

---

## Put it on GitHub Pages (free, about 3 minutes)

1. Create a **new public repository**, e.g. `keshav-19`.
2. Drag the **contents** of the `keshav-19` folder in (not the folder itself — `index.html` must sit at the top level) and commit.
3. **Settings → Pages → Source: Deploy from a branch → `/ (root)` → Save.**
4. Wait a minute. Your site is `https://<your-username>.github.io/keshav-19/`.

No build step, no dependencies, no framework. It is plain HTML/CSS/JS, which is exactly why it deploys free.

---

## The three things you still need to do

### 1. The Google Drive link
Open `js/config.js`, line 8:

```js
driveLink: "PASTE-YOUR-GOOGLE-DRIVE-LINK-HERE",
```

Paste the shareable link (make sure it's set to *Anyone with the link*). It appears at the end of the Lakshita GPT birthday answer. Until you do it, the card is shown but does nothing.

### 2. Your two home-page photos
Rename your two real photos to `photo-1.jpg` and `photo-2.jpg` and drop them into `assets/photos/`.
The frames automatically switch from "slot one" placeholders to the real pictures — nothing else to change.

### 3. Your own words
Every sentence lives in `js/config.js`, grouped exactly like the site:

| In `config.js` | What it controls |
|---|---|
| `SITE.home` | birthday headline paragraph, the day counter, photo captions |
| `SITE.gpt.threads` | the seven conversations in the Lakshita GPT sidebar |
| `SITE.gpt.fallback` | what Lakshita GPT says to anything not in the list |
| `SITE.temple.chapters` | Belgaum / the no phase / the 16th of March — the scene text |
| `SITE.temple.journey.stops` | the five breakdowns on the train track |
| `SITE.temple.journey.finalText` | the smooth stretch and the "I love you" ending |
| `SITE.temple.fun` | the beach, the ice cream, the fruit salad captions |

Anything I wrote for you is a placeholder in the right voice — replace it with yours. The spots I know I invented are marked with `[Replace this with ...]` so you can find them with a search.

`SITE.home.sinceDate` is `2025-12-05` (Belgaum) and drives the "N days of us" counter under the clock. Change it if you want the count to start somewhere else.

---

## What each page does

**Home.** Big editorial headline, a brass pendulum clock hanging from a chain that actually swings, the two open photo frames, the coffee-and-cookie pairing, an elderflower strip, and disco-light refractions drifting in the top two corners of every page.

**Lakshita GPT.** A real ChatGPT layout — sidebar with seven recent conversations, the composer pinned to the bottom, answers that type themselves out. The floating question above the input box is *"What does my 19th birthday mean to you?"*; clicking it sends it and answers with the Drive link at the end. The most recent thread, *What to do after a fight?*, answers in bold capitals and nothing else.

**Vrindavan.** You start outside the temple door and press *step in* — the doorway photograph opens into the sanctum. *Lalji, tell us the story* opens the register of three dates; each one dissolves the screen into that real place (the back seats of the bus, the canteen table, the train) with the narration over it. The 16th of March hands you the train: press *move ahead* and it runs, hits five breakdowns — hover any signal to read what went wrong there — and after the fifth one the line goes clear and the last panel opens.

---

## Small notes

- Fonts come from Google Fonts (Fraunces, Instrument Serif, Manrope). Needs internet on first load, which GitHub Pages has.
- Everything respects "reduce motion" if the visitor asks for it.
- To change a photograph, replace the file with the same name in `assets/photos/`.
- To add a sixth story date, add one object to `SITE.temple.chapters` — the list builds itself.
