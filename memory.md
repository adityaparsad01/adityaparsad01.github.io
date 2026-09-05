# TechNotes Website Memory

## 1. Project Identity

- **Project:** TechNotes
- **Repository:** `adityaparsad01/adityaparsad01.github.io`
- **Branch:** `main`
- **Owner:** Aditya
- **Purpose:** A lightweight personal technology publication focused on practical technology, AI, software development, GitHub, Linux, web development, and electrical engineering.
- **Architecture:** Static HTML/CSS website hosted with GitHub Pages.
- **Runtime:** No server-side application is required for the current site.

## 2. Current Website Structure

The current repository contains the following important website files:

```text
/
├── index.html
├── roman-space-telescope.md
├── robots.txt
├── sitemap.xml
└── memory.md
```

`memory.md` is documentation for maintaining the project. It is not intended to be displayed as a public article.

## 3. Homepage Working

`index.html` is the main entry point of the website.

The page contains:

1. A header with the TechNotes brand.
2. Navigation links for Articles and About.
3. A hero section explaining the purpose of the website.
4. A Latest Articles section.
5. A card for the Roman Space Telescope article.
6. An About TechNotes section.
7. A footer.

The design is contained directly inside `index.html` using HTML and CSS. There is currently no JavaScript framework or build process.

### Responsive behavior

The CSS uses a mobile breakpoint at approximately 760px. On smaller screens:

- Navigation links are hidden.
- Article cards change from a three-column grid to a single column.
- The hero spacing is reduced.

## 4. Article System

The website currently uses a simple static-file article approach.

The Roman Space Telescope article exists as:

```text
roman-space-telescope.md
```

The homepage currently links to:

```text
/roman-space-telescope.html
```

### Important implementation note

A normal GitHub Pages site does **not automatically convert a standalone Markdown file into an HTML page** when the repository is being served as plain static HTML.

Therefore, before publishing more articles, the project should either:

- convert each Markdown article to an HTML page manually, or
- migrate the site to Jekyll, or
- implement another static-site generator/build workflow.

For the current design, the cleanest long-term approach is to use a small static-site structure where every published article has a generated `.html` page and the homepage links to that page.

## 5. Article Publishing Workflow

When adding a new article:

1. Choose a useful topic relevant to the TechNotes audience.
2. Research the subject and verify important facts.
3. Define the primary search keyword.
4. Define related search terms naturally.
5. Create a clear SEO title.
6. Create a concise meta description.
7. Use one H1 heading.
8. Organize the article with descriptive H2/H3 headings.
9. Add useful tables, lists, examples, or FAQs where appropriate.
10. Avoid keyword stuffing.
11. Create the final HTML page.
12. Add the article to the homepage.
13. Add the article URL to `sitemap.xml`.
14. Verify internal links.
15. Commit the changes to `main`.

## 6. SEO System

The homepage currently contains:

- `<title>`
- meta description
- meta keywords
- author metadata
- canonical URL
- semantic headings

The SEO system should prioritize:

- Search intent
- Helpful original content
- Clear page titles
- Accurate meta descriptions
- Descriptive URLs
- One logical H1 per page
- Strong H2/H3 hierarchy
- Internal linking
- Fast page loading
- Mobile usability
- Accessible HTML
- Correct canonical URLs
- XML sitemap coverage
- Crawlable pages

Do not rely on the `meta keywords` tag as an important ranking mechanism. It may remain for compatibility, but article quality and page structure are more important.

## 7. Homepage Article Cards

The homepage should only show real, published articles.

Do not add placeholder or dummy articles such as:

- Fake tutorials
- Generic sample posts
- Unpublished article titles
- Placeholder descriptions

When an article is not actually published, it should not appear in the Latest Articles section.

## 8. Roman Space Telescope Article

Current article topic:

**Roman Space Telescope: NASA’s Next-Generation Observatory**

Main topics covered:

- What the Roman Space Telescope is
- NASA's mission
- Dark energy
- Exoplanets
- Gravitational microlensing
- Infrared astronomy
- Roman vs. Hubble vs. James Webb
- Scientific importance
- Frequently asked questions
- Conclusion

The article is intended to be a technology/space-science publication rather than a fictional or placeholder article.

## 9. Sitemap

`sitemap.xml` tells search engines which pages should be crawled.

Current sitemap behavior should be maintained as the site grows.

Whenever a new article becomes a real HTML page, add its canonical public URL to `sitemap.xml`.

Example structure:

```xml
<url>
  <loc>https://adityaparsad01.github.io/roman-space-telescope.html</loc>
</url>
```

If the site later moves to a custom domain, all canonical URLs, sitemap URLs, and robots.txt sitemap references must be updated consistently.

## 10. Robots.txt

Current `robots.txt` allows normal crawling:

```text
User-agent: *
Allow: /
Sitemap: https://adityaparsad01.github.io/sitemap.xml
```

Do not block the entire site with:

```text
Disallow: /
```

unless intentionally taking the website out of search indexing.

## 11. Domain Configuration

The repository previously contained a `CNAME` file pointing to:

```text
techfeed.me
```

That `CNAME` file has been removed.

The repository is therefore currently configured for the standard GitHub Pages hostname rather than the previous custom-domain configuration.

If a custom domain is added again in the future, update all of these consistently:

- GitHub Pages custom-domain setting
- `CNAME`
- canonical URLs
- sitemap URLs
- robots.txt sitemap URL
- internal absolute URLs, if any

## 12. GitHub Pages Deployment Model

The website is designed to work as a GitHub Pages static site.

The basic flow is:

```text
Edit files
   ↓
Commit to main
   ↓
GitHub Pages publishes the repository
   ↓
Browser requests the static files
   ↓
HTML/CSS is rendered by the browser
```

There is no application server required for the current implementation.

## 13. Design Rules

Keep the visual style:

- Dark background
- High-contrast text
- Blue accent color
- Rounded content cards
- Responsive layout
- Minimal navigation
- Clean typography
- No unnecessary animations

The website should remain lightweight and readable rather than becoming a heavy JavaScript application.

## 14. Content Rules

Every article should:

- Provide genuine informational value.
- Have a clear target audience.
- Avoid unnecessary repetition.
- Use accurate technical terminology.
- Explain difficult concepts in understandable language.
- Use short paragraphs.
- Include useful headings.
- Link to related TechNotes articles when relevant.
- Avoid fabricated statistics or claims.
- Clearly distinguish established facts from predictions or speculation.

## 15. Future Recommended Architecture

As the number of articles grows, migrate from manually maintained static cards to a small content system.

Recommended structure:

```text
/
├── index.html
├── articles/
│   ├── roman-space-telescope.html
│   ├── article-2.html
│   └── article-3.html
├── assets/
│   ├── images/
│   └── css/
├── robots.txt
├── sitemap.xml
└── memory.md
```

A future Jekyll implementation could instead use:

```text
_layouts/
_posts/
assets/
_config.yml
index.html
robots.txt
sitemap.xml
memory.md
```

The Jekyll approach would make Markdown articles practical because GitHub Pages can generate their HTML pages automatically.

## 16. Future Article Template

Every future article should conceptually follow this structure:

```text
SEO title
Meta description
Canonical URL

H1: Main article title

Introduction

H2: Main topic
H2: How it works
H2: Important details
H2: Practical applications
H2: Comparison or examples
H2: FAQ
H2: Conclusion
```

The exact structure should change according to the topic. Do not force headings into an article when they do not improve understanding.

## 17. Maintenance Checklist

Before publishing an article:

- [ ] Facts checked
- [ ] Title optimized for search intent
- [ ] Meta description written
- [ ] Canonical URL correct
- [ ] H1 present
- [ ] Headings logically ordered
- [ ] Internal links checked
- [ ] Mobile layout checked
- [ ] Images optimized if used
- [ ] Image alt text added where appropriate
- [ ] Homepage card added
- [ ] Sitemap updated
- [ ] No dummy content
- [ ] No broken links
- [ ] Commit completed

## 18. Important Rule for Future Changes

Do not delete or overwrite existing production files blindly.

Before changing an existing file:

1. Read the current file.
2. Understand what it currently does.
3. Make the smallest safe change.
4. Preserve working functionality.
5. Verify links and references after the change.
6. Commit with a descriptive message.

For article deletion, remove the article from both the article directory and all homepage/sitemap references.

## 19. Current State Summary

The current TechNotes website is a lightweight GitHub Pages project with:

- A responsive static homepage.
- One real featured article: Roman Space Telescope.
- Dummy homepage articles removed.
- A documentation file named `memory.md`.
- `robots.txt` configured for crawling.
- `sitemap.xml` present but requiring article URLs to be kept synchronized.
- The previous `techfeed.me` CNAME removed.

## 20. Long-Term Goal

The goal is to turn TechNotes into a clean, technically credible technology publication where every article is useful, searchable, internally linked, mobile-friendly, and backed by a maintainable publishing workflow.

The site should grow through **real technical content**, not placeholder articles.
