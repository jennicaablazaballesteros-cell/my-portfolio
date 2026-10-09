# Jennica Marie A. Matias | Portfolio

A responsive, dependency-free portfolio built with semantic HTML, CSS, and JavaScript. Open `index.html` directly in a browser; the contact form hands the message to the visitor's email app.

## Personalize before publishing

- Review the skill list in `index.html` and remove technologies that do not reflect current experience.
- Replace the `X+` years-building stat with a verified value or another measurable result.
- Add direct repository and deployed-demo URLs to the `projects` data array. Until then, repository links lead to the public GitHub profile and project previews are described honestly.
- Add LinkedIn and other social profile URLs when available. Update the public contact details if they change.
- Replace `resume.txt` with a verified, current resume. The download button serves this text file.
- The DSWD project is a proposal, not a deployed agency system; keep privacy, security, and impact claims scoped accordingly.

## Claude Code / framework implementation notes

- **Reusable components:** map the current sections to `Hero`, `ProjectGrid`, `ProjectCard`, `CaseStudyPreview`, `SkillsCloud`, `ExperienceTimeline`, and `ContactCTA`. Keep portfolio content in the `projects`, `skills`, and `experience` arrays rather than embedding content decisions inside presentation components.
- **Case-study routing:** the standalone page uses `#case-study-{slug}` anchors. In Next.js, use `/projects/[slug]` with static params; in Astro, generate `/projects/{slug}/` pages from the project collection. Reuse the same project data and a shared case-study layout.
- **Images:** current project covers are lightweight CSS mockups, so there are no large screenshot downloads. For real screenshots, use responsive AVIF/WebP sources with explicit width/height, meaningful alt text, lazy loading below the fold, and a high-priority hero image only when one is added. In Next.js, use `next/image` and configure allowed image hosts.
- **Metadata:** the document includes title, description, keywords, Open Graph fields, and a theme color. For routed pages, generate a unique title, description, canonical URL, and Open Graph image per route; add a `sitemap.xml` and `robots.txt` before launch.
- **Responsive/accessibility:** mobile navigation has button state and Escape support; sections are semantic, focus-visible states and a skip link are present, and motion honors `prefers-reduced-motion`. Check keyboard-only operation and narrow screens after content changes.
- **Contact delivery:** the current form builds a `mailto:` link and does not store or send data itself. Use a server action or trusted form provider for a production form, add spam protection, and publish an appropriate privacy notice.
- **Deployment:** this static version can be deployed to GitHub Pages, Netlify, or Vercel as static files. Add the final domain, verify HTTPS and metadata, confirm all resume/repository/demo links, and test a production build or deployed preview.

## Local preview

Open `index.html` in a browser. No install or build step is required.

