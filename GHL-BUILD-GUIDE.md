# FlowOpz — GHL Build Guide (poora page)

`index.html` browser mein khol kar design dekhein, phir GHL mein isi tarah build karein.
Sab kuch GHL ke drag-and-drop builder se banega. Code sirf ek jagah hai: Step 1 mein CSS paste karna.
Saara text flowopz.com se liya gaya hai (5 Nov 2026).

> GHL ke menu names version ke hisaab se thore alag ho sakte hain. Koi field na mile to screenshot bhej dein.

---

## Design system

| Cheez | Value |
|---|---|
| Background | `#FFFFFF`, soft section `#F3F3F0`, dark section `#111111` |
| Text | `#111111`, secondary `#5F5F5F`, dark par secondary `#B5B5B5` |
| Accent (sirf ek) | `#E63B19` red. flowopz.com ke brand colors fetch nahi ho sake. Agar brand color alag hai to batayein, CSS mein `--fo-accent` badal dunga |
| Heading font | **Archivo** 800 (ExtraBold) / 700 |
| Body font | **Instrument Sans** 400 / 500. List mein na ho to **Public Sans** |
| Buttons | Black `#111`, white text, radius 0, height 52px, padding left/right 26px |
| Spacing | 8 · 16 · 24 · 32 · 64 · 104 · 120 px |
| Content width | Row width ~1240px (GHL row setting "Wide"/full ke andar max width) |

---

## Step 1 — Page settings (ek dafa)

1. Page > **Edit** > **Settings** (gear) > **Custom CSS** > `ghl-custom-css.css` ka poora content paste > Save.
2. **Typography**: Headline font = Archivo, Content font = Instrument Sans, text color `#111111`.
3. Page background `#FFFFFF`.

**Custom Class lagana:** element/row/column select karein > **Advanced** > **Custom Class** (ya "Class Name") > naam likhein, jaise `fo-btn`. Dot (.) nahi lagana.
**Section ID:** section select > Advanced > **ID / Element ID** field (menu links ke liye).

---

## Section 1 — Header
Section: padding 14/14, border bottom 1px `#111`.
Row: **3 columns 25 / 50 / 25**, vertical center. Row class **`fo-header`**.

| Column | Element |
|---|---|
| 1 | Headline "FlowOpz" (Archivo 800, 24px) ya logo image [PLACEHOLDER: logo file] |
| 2 | **Nav Menu**: Services `#services`, Process `#process`, Pricing `#pricing`, FAQ `#faq`. 15px/500, right aligned. Class **`fo-nav`** |
| 3 | Button "Book a call" → `https://flowopz.com/book/`, height 44, padding 18. Class **`fo-btn`**. **Visibility: mobile par hide** |

## Section 2 — Hero
Section: padding top 80, bottom 0 (mobile 48 / 0).

| Row | Columns | Elements |
|---|---|---|
| 1 | 1 col | Headline H1, 3 lines (Shift+Enter): `Clean systems.` / `Flawless automations.` / `Scaled operations.` Teesri line color `#E63B19`. Class **`fo-display`** (size CSS khud set karegi) |
| 2 | 1 col, margin top 64 (mobile 40) | Divider 1px `#111`. Class **`fo-rule`** |
| 3 | 2 cols **58 / 42**, margin top 28 | Col 1: Paragraph 20px: "**GoHighLevel & Workflow Automation Specialists.** We build GoHighLevel snapshots, workflows and integrations that capture, follow up with and book your leads automatically, from a flat $10/hour." Col 2 (left padding ~8%): Button "Book a Free Consultation →" → `https://flowopz.com/book/` class **`fo-btn`**; Paragraph link "View Our Offers & Rates" → `#pricing` class **`fo-link`**; Paragraph 15px grey, top border 1px `#DCDCD8`: "**Top Rated, 100% Job Success** / 5.0 rating from real Upwork clients. HighLevel Certified Admin." |
| 4 | 1 col, margin top 80 | Paragraph 15px grey: "Every lead tracked, with a live KPI dashboard so you always see what's happening." |
| 5 | **5 cols** equal, column gap 0, row border 1px `#111`, har column ke beech border 1px | Har column mein Paragraph (Archivo 700, 22px, padding 22/20): `New →`, `Contacted →`, `Quoted →`, `Booked →`, `Won`. Classes **`fo-s1`**, **`fo-s2`**, **`fo-s3`**, **`fo-s4`**, **`fo-s5`** (har ek par alag). Red highlight khud ek stage se doosre par chalta rahega |

## Section 3 — Stats
Section padding 96/96. Row: **4 cols** equal. Har **column** ki class **`fo-stat`** (left border CSS lagati hai, mobile par top border).
Har column: Headline (number) class **`fo-num`** + Paragraph 15px grey.
`$10/hr` Flat, transparent base rate · `< 60 sec` Automated first reply to new leads · `100%` Fully documented client handoffs · `24/7` Systems that work while you sleep

## Section 4 — Tools patti (marquee)
Section: background `#111`, padding 28/28, **full width** (row bhi full width).
1 col > Paragraph: Archivo 800, 84px desktop / 40px mobile, white. Class **`fo-marquee`**.
Text **do dafa likhein** (warna loop jhatka khayega):
`GoHighLevel · n8n · Make · Zapier · Stripe · Klaviyo · VAPI · Conversation AI · GoHighLevel · n8n · Make · Zapier · Stripe · Klaviyo · VAPI · Conversation AI · `

## Section 5 — What we do (ID `services`)
Section padding 120/120 (mobile 72).

| Row | Columns | Elements |
|---|---|---|
| 1 | 2 cols 50/50, align bottom | H2 "What we do." class **`fo-h2`** · Paragraph 18px grey "Pick a single targeted fix or hire us by the hour to build and maintain your entire tech stack." |
| 2 | 2 cols **42 / 58**, margin top 72, padding 36/56. **Row** class **`fo-item`** | H3 "GoHighLevel setup and snapshots" (Archivo 800, 48px / mobile 30px) · Paragraph 19px (site text) + link "Ask about this →" → `/book/` class **`fo-link`** |
| 3 | 2 cols 50/50 | Har **column** class **`fo-item`**, padding 32/48: H3 28px + Paragraph grey + "Ask about this →". Speed-to-lead and follow-up automation · Integrations with n8n, Make and Zapier |
| 4 | 2 cols 50/50 | Same: AI agents for chat, calls and your website · Pipelines, calendars and reporting |

(Har service ka poora text `index.html` mein hai, wahan se copy karein.)

## Section 6 — Process (ID `process`), dark
Section background `#111`, text white, padding 120/120.

| Row | Columns | Elements |
|---|---|---|
| 1 | 2 cols 42/58, align bottom | H2 "How does a custom build work?" class **`fo-h2`** · Paragraph 18px `#B5B5B5` ("You work directly with the builders…") |
| 2 | **4 cols**, margin top 80 | Har **column** class **`fo-step`**, padding top 28: Paragraph 14px grey "Step 1" + Paragraph Archivo 700 24px. Steps: Book a discovery/audit call. · We review your current process and goals. · You receive a clear proposal with scope, estimated hours, and price. · Work starts only after approval. |
| 3 | 2 cols 42/58, margin top 104 | Col 1: Paragraph Archivo 500 26px "You work directly with technical builders, led by Muhammad Umar, a Top Rated GoHighLevel and automation expert on Upwork with 100% Job Success." + link "View Upwork profile →" → `https://www.upwork.com/freelancers/muhammadu649` (class `fo-link`). Col 2: Paragraph "Certifications" 14px grey + 4 Paragraphs (har ek top border 1px white 25%): HighLevel Certified Admin · Make Advanced · Airtable Builder · ClickUp Expert |

## Section 7 — Pricing (ID `pricing`)
Section padding 120/120.

| Row | Columns | Elements |
|---|---|---|
| 1 | 2 cols 50/50, align bottom | H2 "Straightforward, accessible pricing." class **`fo-h2`** · Paragraph grey |
| 2 | **3 cols**, gap 24, margin top 72 | Har **column** class **`fo-plan`**, padding 32/28/40. H3 plan name 22px · Headline price class **`fo-price`** ("$10" + chhota "/hr") · Paragraph grey · bullets (Paragraphs with top border `#DCDCD8`) · Button "Get Started Today" → `/book/` class **`fo-btn`** |
| 3 | 2 cols 33/67, margin top 96 | H3 "Output estimates at $10/hour" · 3 Paragraphs with top border: 2–4 hours / 5–10 hours / 15–25 hours (text index.html mein) |

Plans: **Hourly On-Demand** $10/hr · **Weekly Sprint** $200/week, 20 hrs · **Agency Dedicated** $400/week, 40 hrs.

## Section 8 — FAQ (ID `faq`)
Section background `#F3F3F0`, padding 120/120.
Row 2 cols 42/58: Col 1 H2 "Questions, answered." (`fo-h2`) + "Something else on your mind? Email info@flowopz.com".
Col 2: GHL ka native **FAQ** element. Question font Archivo 700 22px, divider lines `#111`, icon "+". 6 sawal (text index.html mein): cost, snapshot, audit, setup time, tools, project finish.

## Section 9 — CTA (ID `contact`), red
Section background `#E63B19`, padding 120/120.
Row 1: Headline "Book a free / consultation." white, class **`fo-display`**.
Row 2: 2 cols 58/42, margin top 56: Paragraph 20px `#111` ("We respond to new enquiries within 1 hour…") · Button "Book a Free Consultation →" black, class **`fo-btn-ink`** (hover par white fill hota hai) + link `info@flowopz.com`.

## Section 10 — Footer, dark
Section `#111`, padding 80/32.
Row 1: 3 cols 50/25/25: "FlowOpz" + "High-efficiency GHL architecture and automated backend infrastructure." · Page links (`fo-link`) · Contact: info@flowopz.com, LinkedIn, Instagram, Upwork.
Row 2: top border `#333`, 2 cols: "© 2026 FlowOpz. All rights reserved." · Privacy Policy / Terms of Service (flowopz.com/privacy/, /terms/).

---

## Entrance animations (native, koi code nahi)
Element > **Entrance Animation** > **Fade Up** > Adjust: Duration **0.8s**, Easing **Ease Out**.

| Element | Delay |
|---|---|
| Hero headline | 0.7s |
| Hero paragraph | 0.95s |
| Hero button + link | 1.05s |
| Hero proof text | 1.15s |
| Pipeline caption / strip | 1.2s / 1.25s |
| Baaqi sab headings | 0s |
| Unke saath wale paragraphs | 0.1s |
| 3–4 columns wali rows (stats, steps, plans) | 0s, 0.08s, 0.16s, 0.24s (left se right) |

**Ye na karein:** buttons, `fo-s1–5` stages, marquee aur divider par entrance animation na lagayein. Un ki apni CSS animation hai, dono takra jayengi.

## Teen screens par check
- **Desktop:** bilkul index.html jaisa.
- **Tablet (768–1023px):** GHL desktop columns rakhta hai. Headline, H2, stats aur prices ke sizes CSS khud chhote karti hai.
- **Mobile:** GHL columns stack karta hai. Mobile view mein check karein:
  1. Logo + hamburger ek line mein hon. Na hon to batayein (`fo-header` CSS GHL ke andar ke class names par depend karti hai).
  2. Section paddings upar diye gaye mobile numbers par hon.
  3. Marquee paragraph mobile par 40px.

Reduce-motion wale users ke liye saari animations CSS khud band kar deti hai.

## Jo abhi missing hai
- [PLACEHOLDER] FlowOpz logo file aur brand colors (site se nahi mil sake)
- Booking button abhi `flowopz.com/book/` par jata hai. Agar GHL calendar ka direct link chahiye to bata dein
- Testimonials aur projects nahi daale, kyunki site par review ka text nahi mila (sirf naam the). Asal reviews dein to section bana dunga
