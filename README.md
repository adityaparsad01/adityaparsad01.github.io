# TechNotes

A lightweight personal technology publication focused on practical technology, AI, software development, GitHub, Linux, web development, space science, and electrical engineering.

🌐 **Live site:** https://adityaparsad01.github.io/

## About

TechNotes is built around a simple idea:

> Learn something, build something, test it, and document what worked.

The site focuses on clear, practical explanations rather than generic or heavily promotional technology content.

## Current Articles

- **[GPT-6 Astra Explained](gpt-6-astra-explained.html)**
  How AI agents are moving beyond traditional chatbots toward computer use and multi-step task completion.

- **[Computer-Use AI Explained](computer-use-ai-explained.html)**
  How AI agents interact with browsers and software, how this differs from traditional automation, and why permissions and verification matter.

- **[Roman Space Telescope](roman-space-telescope.html)**
  An explanation of NASA's Roman Space Telescope, its wide field of view, dark-energy research, exoplanet science, and relationship to Hubble and Webb.

## Technology Stack

- HTML5
- CSS3
- GitHub Pages
- Static site architecture
- Google Analytics 4
- Schema.org structured data
- XML sitemap
- `robots.txt`

No server-side application or JavaScript framework is required for the current site.

## Repository Structure

```text
/
├── index.html
├── gpt-6-astra-explained.html
├── computer-use-ai-explained.html
├── roman-space-telescope.html
├── tech-notes-blog-writing-framework.md
├── memory.md
├── robots.txt
└── sitemap.xml
```

### Important files

| File | Purpose |
|---|---|
| `index.html` | Main TechNotes homepage and article listing |
| `gpt-6-astra-explained.html` | GPT-6 Astra article |
| `computer-use-ai-explained.html` | Computer-use AI article |
| `roman-space-telescope.html` | Roman Space Telescope article |
| `tech-notes-blog-writing-framework.md` | Writing methodology for future articles |
| `memory.md` | Project maintenance documentation |
| `robots.txt` | Search-engine crawling rules |
| `sitemap.xml` | Public page discovery for search engines |

## Design

The current design is intentionally lightweight and responsive:

- Dark interface
- High-contrast typography
- Blue accent color
- Rounded article cards
- Responsive mobile layout
- Minimal navigation
- No unnecessary JavaScript framework

The goal is fast loading, readable content, and a simple publication experience.

## SEO

Published pages use standard SEO elements including:

- Descriptive page titles
- Meta descriptions
- Canonical URLs
- Open Graph metadata
- Twitter metadata
- Semantic H1/H2/H3 structure
- Article Schema.org structured data where appropriate
- XML sitemap
- Crawlable URLs
- Internal links

The canonical site URL is:

`https://adityaparsad01.github.io/`

The previous custom-domain `CNAME` configuration has been removed.

## Analytics

Google Analytics 4 is installed on the website using measurement ID:

`G-BV5E0CN1W`

When modifying existing pages, preserve the analytics implementation unless it is intentionally being changed.

## Writing Framework

Future TechNotes articles should follow the project's writing framework in:

`tech-notes-blog-writing-framework.md`

The framework emphasizes:

1. A strong reader-focused topic
2. Clear understanding of the target reader
3. A specific working headline
4. A logical outline
5. Critical review before drafting
6. A strong introduction
7. Useful and technically accurate body sections
8. A conclusion with one clear CTA
9. Helpful visuals, examples, tables, or sources where appropriate
10. A separate editing and fact-checking pass

Articles should be original, useful, conversational, technically precise, and optimized for search without keyword stuffing.

## Publishing Workflow

For a new article:

1. Choose a useful topic.
2. Identify the reader's question or problem.
3. Research and verify important facts.
4. Define the search intent.
5. Create the article outline.
6. Write the article using the TechNotes framework.
7. Add SEO metadata and structured data.
8. Create the final `.html` page.
9. Add the article to `index.html`.
10. Add its canonical URL to `sitemap.xml`.
11. Check internal and external links.
12. Check the mobile layout.
13. Commit the changes to `main`.

## Content Principles

TechNotes articles should:

- Explain difficult concepts clearly.
- Provide genuine reader value.
- Use accurate technical terminology.
- Explain jargon when needed.
- Prefer concrete examples over vague claims.
- Distinguish confirmed facts from predictions and interpretation.
- Use authoritative primary sources for current or technical claims.
- Avoid fabricated statistics.
- Avoid unnecessary repetition and filler.
- Avoid excessive hype and corporate buzzwords.

## GitHub Pages

The site is deployed as a static GitHub Pages website from the `main` branch.

```text
Edit HTML/CSS
      ↓
Commit to main
      ↓
GitHub Pages publishes the files
      ↓
Browser loads the static site
```

No application server is required for the current architecture.

## Maintenance Rules

Before modifying an existing production file:

1. Read the current version.
2. Understand what it currently does.
3. Make the smallest safe change.
4. Preserve working functionality, analytics, navigation, and SEO.
5. Verify affected links and references.
6. Commit with a descriptive message.

Do not add placeholder or dummy articles to the public homepage.

Whenever a published article is added, removed, or renamed, keep the homepage and `sitemap.xml` synchronized.

## Future Direction

As the number of articles grows, the site can be migrated to a small static-site generator or Jekyll-based structure. That would make article publishing easier while retaining the lightweight GitHub Pages deployment model.

Until then, published articles use standalone HTML files so that they work reliably as static GitHub Pages content.
