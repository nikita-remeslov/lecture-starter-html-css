# Binary Academy of Rock — Homework

Hi! Welcome to the Academy! You’re about to build something that matters —
not just a webpage, but a stage. This homework asks you to create a
**single-page landing page** for **Binary Academy of Rock**: a school where
students learn to ship code and shred guitar. Think School of Rock,
but with pull requests.

You are limited to **HTML and CSS only**. No scripts. No frameworks. Just
you, the browser, and your craft.

---

## Design Reference

This is what the finished page looks like. Your layout must match — sections,
structure, and proportions. Colors, fonts, and spacing come from the token
set below.

| Mobile                                      | Desktop                                          |
| ------------------------------------------- | ------------------------------------------------ |
| ![Mobile view](./assets/screenshot-mob.png) | ![Desktop view](./assets/screenshot-desktop.png) |

---

## The Design System

The visual identity is predefined — implement it faithfully and use it
consistently throughout. Create `assets/css/global/tokens.css` and copy
this token set exactly:

```css
:root {
  /* Colors */
  --color-primary: #f0f0f0;
  --color-primary-light: #ffffff;
  --color-accent: #f0f0f0;
  --color-cta: #7d0000;

  --color-surface: #080808;
  --color-surface-raised: #101010;
  --color-surface-subtle: #1a1a1a;

  --color-text: #f0f0f0;
  --color-text-muted: #888888;

  --color-border: #2e2e2e;
  --color-border-bold: #f0f0f0;

  /* Spacing */
  --space-xs: 0.5rem; /*  8px */
  --space-s: 0.75rem; /* 12px */
  --space-m: 1rem; /* 16px */
  --space-l: 1.5rem; /* 24px */
  --space-xl: 2rem; /* 32px */
  --space-2xl: 3rem; /* 48px */
  --space-3xl: 5rem; /* 80px */

  /* Radius - sharp corners, rock aesthetic */
  --radius-s: 0px;
  --radius-m: 0px;
  --radius-l: 0px;
  --radius-full: 0px;

  /* Shadows */
  --shadow-m: 0 4px 24px rgba(0, 0, 0, 0.5);

  /* Typography */
  --font-display: 'Bebas Neue', 'Impact', sans-serif;
  --font-body: 'Inter', system-ui, -apple-system, sans-serif;

  /* Layout */
  --wrapper-max: 1200px;
  --gutter: clamp(1rem, 4vw, 2rem);
  --header-height: 6rem;
}
```

Load the fonts by adding these three lines inside `<head>` **before** the
stylesheet link:

```html
<link rel="preconnect" href="https://fonts.googleapis.com" />
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
<link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet" />
```

**Reference font sizes** — use these `clamp()` values for the matching
elements:

| Element               | Value                                    |
| --------------------- | ---------------------------------------- |
| Base body text        | `clamp(1rem, 0.9rem + 0.5vw, 1.125rem)`  |
| Hero title            | `clamp(2.5rem, 1.5rem + 4vw, 6rem)`      |
| Section headings (h2) | `clamp(2rem, 1.5rem + 2vw, 3.5rem)`      |
| Stat values           | `clamp(2rem, 1.5rem + 2vw, 3.5rem)`      |
| Logo                  | `clamp(1.25rem, 0.8rem + 0.8vw, 1.5rem)` |

**Rules:**

- No hardcoded hex or rgb values outside `tokens.css`
- No magic spacing numbers — `padding: 23px` or `margin: 17px` is forbidden.
  Every padding, margin, and gap must reference a spacing token
- No hardcoded border-radius values outside tokens
- Minimum 4.5:1 contrast ratio between `--color-text` and `--color-surface`

---

## Layout Constraints

The page must be usable and visually intact at **375px**, **768px**, and **1440px**

---

## Provided Assets

All images are in `assets/img/`. Use them as listed — do not rename the files.

### Images

All files live in `assets/img/`. Do not rename them.

| Preview                                                                         | File                                   | Section                                      |
| ------------------------------------------------------------------------------- | -------------------------------------- | -------------------------------------------- |
| ![Hero](./assets/ab99b20227f3b18848fc92a236b67350.jpg)                         | `ab99b20227f3b18848fc92a236b67350.jpg` | Hero                                         |
| ![Electric Guitar & Algorithms](./assets/86b0fe01cbbe5bc7839a346c0df437b6.jpg) | `86b0fe01cbbe5bc7839a346c0df437b6.jpg` | Course card 1 — Electric Guitar & Algorithms |
| ![Drums & Data Structures](./assets/8bd2c378e6433c8310a6429bcae85633.jpg)      | `8bd2c378e6433c8310a6429bcae85633.jpg` | Course card 2 — Drums & Data Structures      |
| ![Bass & Backend](./assets/ad36adca2a63b95ebaec55be5ffb2079.jpg)               | `ad36adca2a63b95ebaec55be5ffb2079.jpg` | Course card 3 — Bass & Backend               |
| ![Vocals & Version Control](./assets/3924deb0b982681fd168b66f9326781f.jpg)     | `3924deb0b982681fd168b66f9326781f.jpg` | Course card 4 — Vocals & Version Control     |
| ![Mick Jagger](./assets/7d1fa43d6c3e9795ca8445a625d5ced3.jpg)                  | `7d1fa43d6c3e9795ca8445a625d5ced3.jpg` | Alumni — slide 1 (Mick Jagger)               |
| ![Thom Yorke](./assets/6ef8f82220bdc9fdeffcded0200e5917.jpg)                   | `6ef8f82220bdc9fdeffcded0200e5917.jpg` | Alumni — slide 2 (Thom Yorke)                |
| ![Bob Dylan](./assets/7bfd2760bea5e4f97ed9f954dd4fa2cf.jpg)                    | `7bfd2760bea5e4f97ed9f954dd4fa2cf.jpg` | Alumni — slide 3 (Bob Dylan)                 |
| ![Join Us illustration](./assets/3b359f698acd440f7a6ff9b7f0deb255.png)         | `3b359f698acd440f7a6ff9b7f0deb255.png` | Join Us section                              |

### Alumni Content

Use this content verbatim for the three alumni slides:

**Slide 1**

- Name: Mick Jagger · Cohort: Previous Year Class
- Quote: “I came in as a junior dev who couldn’t tune a guitar. I left as a
  senior engineer who played their first gig at graduation. Best six months
  of my life.”

**Slide 2**

- Name: Thom Yorke · Cohort: Previous Year Class
- Quote: “I thought the coding and music tracks would compete for my
  attention. Instead they feed each other. My solos have structure. My
  code has rhythm.”

**Slide 3**

- Name: Bob Dylan · Cohort: Previous Year Class
- Quote: “The bands you form here become your engineering team. We
  graduated, started a company, and still practice on Thursdays.”

### Schedule Content

Use these 9 items for the Schedule section, one per `.schedule__item`:

| #   | `datetime`   | Display | Title                        | Type  |
| --- | ------------ | ------- | ---------------------------- | ----- |
| 01  | `2026-06-17` | Jun 17  | Riff Sprint                  | Music |
| 02  | `2026-06-21` | Jun 21  | Debug Jam                    | Code  |
| 03  | `2026-06-25` | Jun 25  | Acoustic Algorithms          | Music |
| 04  | `2026-06-29` | Jun 29  | Bass Drop Bootcamp           | Music |
| 05  | `2026-07-03` | Jul 3   | API & Amplifier Workshop     | Code  |
| 06  | `2026-07-07` | Jul 7   | Open Mic + Open Source       | Code  |
| 07  | `2026-07-11` | Jul 11  | Backstage Wiring             | Code  |
| 08  | `2026-07-15` | Jul 15  | Silent Shredder              | Music |
| 09  | `2026-07-19` | Jul 19  | Reactive Road Tour: Advanced | Music |

### FAQ Content

Use these five questions for the FAQ section:

1. **Do I need any prior coding experience?** — No. We start from zero on
   both tracks. If you can count to four (musically speaking), you can
   learn to write a for loop.

2. **Do I need to own an instrument?** — All instruments are available in
   our studio spaces. Once you know what you want to play, we’ll help you
   find the right gear at the right price.

3. **How long is the programme?** — The core curriculum is 6 months,
   full-time. We also offer a 12-month part-time track for working
   professionals. Both lead to the same capstone: a shipped project and a
   live performance.

4. **What happens at the graduation concert?** — You play a 20-minute set
   with your band and demo your final project to an audience of hiring
   managers and music industry contacts.

5. **Is the curriculum remote-friendly?** — The coding track is fully
   remote. The music track requires in-person attendance at least twice
   a week — you can’t rehearse through a screen. We have studios in
   Lviv, Kyiv, Kharkiv, and Odessa.

---

## The Quest System

This homework is structured as a quest system. Complete the Core Quest to pass.
Add Advanced or Rockstar quests to raise your mark.

---

### Core Quest — 70%

#### Header

- Stays at the top of the window at all times, even when scrolling
- Logo on the left, navigation on the right
- Each nav link has class `menu__link` with an animated underline on hover
- The last nav link is a **Join Us** CTA button (also has `menu__link` class)
- On mobile and tablet: nav links are hidden, a burger icon (`menu__button` class)
  appears — the menu does not need to open yet (that is an Advanced quest)

#### Hero Section

- A content block (`hero__content`) and image block (`hero__image`)
- `hero__content` contains:
  - title `hero__title` — must use `text-wrap: balance`
  - tagline `hero__tagline`
  - two CTA buttons `hero__button` (primary: “Join the Band”, secondary: “Watch Us Play”)
- `hero__image` is hidden on mobile
- The hero title font size uses `clamp()`

#### Stats Section

- Three items inside the container, each with class `stat__item`
- Each `stat__item` contains `stat__item-title`, `stat__item-icon`,
  and `stat__item-value`
- Values: “1,200+ Students”, “87 Bands Formed”, “340 Projects Shipped”
- Stacks vertically on mobile, sits in a row on desktop

#### Courses Section

- Title `courses__title` and subtitle `courses__subtitle`
- Exactly 4 cards, each with class `course`, containing:
  - `course__image` — use the provided image for each card
  - `course__badge` — difficulty label with a `data-track` attribute
    (`foundation`, `intermediate`, or `advanced`)
  - `course__title` (Electric Guitar & Algorithms · Drums & Data Structures ·
    Bass & Backend · Vocals & Version Control)
  - `course__description`
- Cards arrange in a responsive grid using `auto-fill` + `minmax()` —
  no fixed column counts

#### Schedule Section

- Title `schedule__title`
- A `schedule__list` containing one `schedule__item` per row from the
  provided schedule table
- Each `schedule__item` must include:
  - `<time class="schedule__date" datetime="YYYY-MM-DD">` — use the exact
    `datetime` values from the table
  - `schedule__num` — the two-digit number (01, 02 …)
  - `schedule__title-text` — the lecture title
  - `schedule__type` with `data-type="music"` or `data-type="code"` — the
    two types must be visually distinct via the attribute selector

#### FAQ Section

- Title `faq__title`
- A `faq__list` containing `faq__item` elements
- Each `faq__item` is a `<details>` element; the question is a `<summary>`
  with class `faq__question`; the answer lives inside `faq__answer`
- Use the five provided questions and answers verbatim

#### Join Us Section

- Title `join__title` and subtitle `join__subtitle`
- Email input `join__email` and submit button `join__button`
- Image `join__image` — use `canvas.png`
- Form stacks on mobile, sits inline on tablet and up

#### Footer

- Always at the bottom of the page, even with no content above it
- 3 social icon links (GitHub, YouTube, Instagram), each with class `social__link`
- 4 navigation links, each with class `footer__link`

---

### Advanced Quest — 20%

1. **Container query on course cards**
   The `course` card switches from stacked to side-by-side layout based on its
   **own width**, not the viewport. Requires `container-type: inline-size` on
   the card wrapper.

2. **Alumni slider with scroll snap**
   3 slides using the provided alumni content, each `alumni__slide` containing
   `alumni__image`, `alumni__quote`, `alumni__name`, and `alumni__cohort`.
   `scroll-snap-type` on the container, `scroll-snap-align` on each slide.
   Visible navigation dots with class `alumni__dots`. **No radio button hack.**

---

### Rockstar Quest — 10%

1. **Add your personal section**
   The Canvas placeholder (`id="canvas"`) is yours to fill. Design a section
   that is completely original — your content, your layout, your CSS. No
   constraints on what it contains. Evaluated on creative use of CSS,
   visual quality, and originality.
