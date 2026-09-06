# Portfolio Review — HR/Recruiter Lens

Review date: 2026-09-06. Perspective: an HR/recruiter at a large company doing a
first pass (~30 seconds) on `ui_kits/portfolio/index.html`, followed by a closer
technical read.

## Biggest gap: no résumé anywhere
No CV/résumé file exists in the project, no work-history/"Experience" section.
Big companies rarely hire off a portfolio alone — they need a standard résumé
for ATS and internal sharing. Without one, the site reads as early-career by
default regardless of actual experience.
- [ ] Add a prominent "Download Résumé" button in the nav/hero.
- [ ] Add an Experience section (company, role, dates, outcomes) if there's
      paid work history to show.

## Credibility risks (fix before a technical reviewer notices)
- [ ] **GitHub contribution graph is fake** — the script uses `Math.random()`
      to color cells; it's not real GitHub data. Anyone who views source will
      see this. Either wire up real contribution data or remove the section.
- [ ] **"0 ML models used" as a headline stat** undercuts the ML/DS
      positioning at a glance. The rationale (explainable, rule-based,
      evidence-motivated thresholds) is a legitimate and sophisticated choice,
      but it isn't legible in a fast skim — only in a paragraph most
      recruiters won't read.
- [ ] **"Machine Learning" is listed both as an established skill (Data
      Science category) and under "Currently learning."** Pick one.
- [ ] **Say/do gap on ML:** Scikit-learn, Statistics, and Model Evaluation are
      listed as skills, but no project demonstrates a trained model or an
      evaluation metric. One small project with real metrics would close
      this gap.

## Positioning/copy
- [ ] "Software Engineer *exploring* Data Science & Machine Learning" reads as
      tentative. Consider a more confident lead, e.g. "Software Engineer
      building end-to-end, data-driven products" — let the About section
      carry the transition story (already well-written, keep it).
- [ ] Only one finished project ("Coming soon" for the second). Consider
      adding at least one more finished, smaller project for breadth —
      ideally one that also demonstrates applied ML with metrics.

## UX/presentation issues on the site
- [ ] The three Finance Analytics screenshots (1280×2856 phone screens) are
      squeezed into a 1/3-width row and cropped top-only via
      `object-fit: cover`. Text is illegible at that size with no
      click-to-expand. Show one larger hero screenshot with captions, or make
      them clickable/lightbox.
- [ ] No live demo or video walkthrough — it's an Android app + FastAPI
      backend, so a recruiter can't try it. A short Loom/GIF walkthrough
      would help more than the stats row.
- [ ] No `<meta name="description">`, no Open Graph tags, no favicon — link
      previews (LinkedIn, Slack, email) will show nothing. Cheap fix.
- [ ] Deployment path is nested (`ui_kits/portfolio/index.html`) — confirm the
      final hosted URL is clean and doesn't expose that scaffolding.
- [ ] Double-check the footer contact email (`fonsecamariainesf@gmail.com`)
      is the one actually monitored.

## What's working — keep it
- About section narrative (software engineering → curiosity about data → EDA
  → end-to-end products) is coherent and genuinely strong.
- "247 automated tests" + the explicit engineering pipeline (CSV → Enrichment
  → Anomaly Detection → ... → Android App) signal real engineering rigor —
  lean into this more.
- Visual design (typography, spacing, single-accent color system) is clean
  and above average for a personal portfolio.

## Top 3 for this week
1. Add a résumé download + a line on experience/openness to opportunities.
2. Fix or remove the fake GitHub contribution graph.
3. Add one project that shows an actual trained model with evaluation
   metrics, to back up the ML positioning.
