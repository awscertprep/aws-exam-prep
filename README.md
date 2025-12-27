# AWS Exam Prep 🚀

Modern, scenario-first drills for AWS certification prep. Built with Astro; decks are JSON-backed and easy to extend.

**Why this exists:** I built AWS Exam Prep while studying for AWS certifications. I take structured notes and wanted a faster way to rehearse concepts and tradeoffs. This project turns those notes into quick drills and flashcards so others can learn faster too.

## Site 🌐

- Live site: https://awsexamprep.live

## Getting Started 🛠️

```bash
npm install
npm run dev
```

## Content Structure 📂

- MCQs live in `site/content/aws/<exam>/mcqs/*.json`.
- Pages live in `site/src/pages/aws/<exam>/<topic>.astro` and import the matching JSON.
- Service notes live in `site/src/pages/services/` (start with `site/src/pages/services/ec2.astro`).
- Shared layout and styling: `site/src/layouts/BaseLayout.astro`.

To add a new deck:
1) Add a JSON file under `site/content/aws/<exam>/mcqs/`.
2) Copy an existing page in `site/src/pages/aws/<exam>/` and point it to the new JSON.
3) (Optional) Add a changelog entry in `site/content/updates.json` so it appears on the homepage sidebar.
4) Update the relevant exam index page under `site/src/pages/aws/<exam>/index.astro`.

## Flashcards 🧠

- Flashcards live in `site/content/aws/<exam>/flashcards/*.json`.
- Flashcard pages live in `site/src/pages/aws/<exam>/flashcards.astro` and import the matching JSON.
- To update cards, edit `site/content/aws/<exam>/flashcards/overview.json` (front/back per card).

## Internal Linking 🔗

- Related deck links are defined within each deck page near the bottom.
- SAP-C02 pages: `site/src/pages/aws/sap-c02/*.astro`
- DOP-C02 pages: `site/src/pages/aws/dop-c02/*.astro`
- Update the “Related decks” section in those files when you add new topics.

## Policies & Contact 📜

- Privacy: `/privacy`
- Terms: `/terms`
- Contact: `/contact` (Formspree endpoint set in `site/src/pages/contact.astro`).
- Exam integrity: Do not post or share actual exam questions. This site is for strengthening AWS concepts, terminology, and use-case judgment—not for disclosing live or recalled exam items.
- Any similarity to real exam questions is coincidental.
- Note: Some service pages may be AI-formatted from author notes; the author reviews them, but if you spot inaccuracies, please open a PR.

## Navigation Structure 🧭

- Global header is defined in `site/src/layouts/BaseLayout.astro`.
- Exams are grouped under the Exams dropdown in the header.
- Services sit next to Exams and link to `/services`.

## Contributing 🤝

- Open pull requests via the GitHub link in the footer—please collaborate here rather than copying the app elsewhere.
- Keep MCQ explanations concise and source-aligned with official AWS guidance.

## Building & Preview 🧱

```bash
npm run build
npm run preview
```
