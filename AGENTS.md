---
# AGENTS.md - GottigWeb CV

## Agent Profile
- **Role:** Frontend Web Developer (Static Sites)
- **Responsibilities:** Maintain and update static HTML/CSS CV website, ensure bilingual consistency (EN/ES), optimize for accessibility and SEO
- **Decision Authority:** Can update CV content, fix styling issues, and make minor structural changes independently

## Tech Stack & Tooling
- **Language/Runtime:** HTML5, CSS3
- **Frameworks:** Bootstrap 4.0.0 (CDN)
- **Package Manager:** None (static site)
- **Infrastructure:** GitHub Pages (static hosting)
- **CI/CD:** None (manual deployment via git push)
- **Local Dev:** fish shell

## Coding Standards
- **Style:** Standard HTML5 with semantic elements where appropriate
- **CSS:** Organized in `styles/styles.css`
- **Typing:** Not applicable (HTML/CSS)
- **Error Handling:** Validate HTML structure, ensure all images have alt attributes

## Testing Requirements
- **Coverage Minimum:** Not applicable (static site)
- **Test Types:** Manual verification, HTML validation
- **Framework:** None
- **Utilities:** W3C HTML validator, accessibility checks (alt tags, semantic structure)

## Security Requirements
- No sensitive personal data (phone, address) hardcoded in public HTML
- External CDN links use integrity attributes for Bootstrap
- All external links use appropriate `rel` attributes
- No inline JavaScript or styles

## Workflow & Git
- **Version Control:** git
- **Commit Format:** Conventional Commits (feat, fix, docs, style)
- **Branch Strategy:** Simple master pushes (no feature branches)
- **Code Review:** Not required (single developer)
- **Release:** Manual deployment via `git push origin master`
- **Remote:** git@github.com:gottigjavier/gottigweb.git

## Local Development
- **Automation:** None (simple static site)
- **Convenience:** fish shell for git operations
- **Dev Mode:** Open `index.html` or `index_es.html` directly in browser, or use local server (`python -m http.server`)

## Guardrails
### Forbidden
- Inline styles (`style=` attributes)
- Inline JavaScript (`<script>` in HTML body)
- Hardcoding sensitive contact information
- Breaking bilingual structure (EN: index.html, ES: index_es.html)
- Removing Bootstrap CDN integrity attributes
- Using deprecated HTML elements

### Mandatory
- Alt attributes on all `<img>` tags
- Semantic HTML5 structure (`<header>`, `<main>`, `<footer>` where appropriate)
- Maintain parallel structure between `index.html` and `index_es.html`
- Keep styles in `styles/styles.css` (not inline)
- Update both language versions when changing CV content
- Use `language_text/languaje.json` for text content management

## Review Triggers
This file must be updated when:
- New framework or library added
- Change in hosting platform
- New team member joins
- Major restructuring of HTML/CSS architecture
- Adding JavaScript functionality
