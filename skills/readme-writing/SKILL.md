---
name: readme-writing
description: Create, audit, rewrite, localize, and polish GitHub README files with clear information architecture, accurate setup instructions, concise examples, and GitHub-native visual design. Use for new README creation, README redesigns, bilingual README work, template generation, or documentation quality reviews.
---

# README Writing

Create README files that help a new visitor answer four questions quickly:

1. What is this project?
2. Why should I care?
3. How do I run or use it?
4. Where do I go next?

Optimize for clarity, accuracy, scanability, and maintainability before decoration.

## When to use this skill

Use this skill when asked to:

- create a README from scratch;
- improve or redesign an existing README;
- turn repository facts into polished project documentation;
- create a reusable README template;
- translate or localize a README;
- add badges, screenshots, navigation, examples, or contribution guidance;
- review a README for structure, correctness, or visual quality.

## Repository-first workflow

Before writing, inspect the repository whenever access is available. Do not invent project behavior that can be verified from files.

Look for:

- package manifests such as `package.json`, `pyproject.toml`, `Cargo.toml`, `go.mod`, or `pom.xml`;
- executable entry points and common scripts;
- `.env.example` or configuration files;
- license files;
- contribution, security, changelog, and documentation files;
- screenshots, logos, diagrams, and demo assets;
- CI workflows, package publishing, releases, and deployment configuration;
- existing README text that should be preserved.

If repository evidence conflicts with the current README, prefer repository evidence and clearly avoid unsupported claims.

## Choose the README mode

### New README

Build the document from verified repository information. Use the canonical templates hosted on GitHub as a starting point when appropriate:

- English: [`BLANK_README.md`](https://github.com/NakanoSanku/Best-README-Template/blob/main/BLANK_README.md)
- 简体中文: [`BLANK_README.zh-CN.md`](https://github.com/NakanoSanku/Best-README-Template/blob/main/BLANK_README.zh-CN.md)

These template URLs are intentionally absolute so this skill can be installed, copied, or distributed independently without requiring the rest of the template repository to be installed locally.

### README improvement

Preserve useful content, working links, important attribution, and project-specific instructions. Improve hierarchy and wording without silently removing critical information.

### Localization

Translate meaning rather than words mechanically. Keep commands, filenames, identifiers, API names, package names, code, and placeholders unchanged unless the localized project intentionally uses different values.

For bilingual READMEs, add a visible language switcher near the top and link both versions to each other.

### Template creation

Use obvious, searchable placeholders such as:

- `github_username`
- `repo_name`
- `project_title`
- `project_description`
- `project_license`
- `email`

Explain placeholders in a removable note or collapsible block. Do not leave project-specific claims inside a reusable template.

## Recommended information architecture

Use only the sections the project actually needs. A strong default order is:

1. Hero / project identity
2. Badges and primary links
3. About / problem and value
4. Highlights or features
5. Tech stack
6. Getting started
7. Usage
8. Configuration or API reference when needed
9. Roadmap
10. Contributing
11. License
12. Contact
13. Acknowledgments

For libraries and developer tools, prioritize installation and a minimal working example earlier. For end-user applications, prioritize screenshots, demo links, and user-facing value earlier.

## Hero section rules

The first screen should be understandable without scrolling through a badge wall.

Prefer:

- one logo or product image;
- one project title;
- one concise value proposition;
- one optional supporting sentence;
- one primary action and a few secondary links;
- only badges that communicate useful status.

Avoid:

- decorative badges with no information value;
- several competing calls to action;
- long marketing paragraphs before the project is explained;
- fragile layout tricks or custom CSS that GitHub will not render consistently.

## Writing style

Write for scanning first and deep reading second.

- Lead sections with the most useful fact.
- Prefer short paragraphs and meaningful bullets.
- Use concrete language instead of generic claims such as “awesome”, “powerful”, or “next-generation” unless evidence supports them.
- Explain benefits in user terms, not only implementation terms.
- Keep headings descriptive and predictable.
- Use terminology consistently throughout the document.
- Avoid repeating the same explanation in multiple sections.

## Installation rules

Installation instructions are high-risk documentation because incorrect commands immediately damage trust.

- Use commands verified from the repository whenever possible.
- Include the required runtime or tooling version when it materially affects setup.
- Show the correct working directory.
- Mention environment variables only when they actually exist.
- Never fabricate API keys, package names, script names, ports, or configuration files.
- Prefer a short successful path over documenting every possible setup variation.
- Link to dedicated docs when setup becomes too large for a README.

## Usage examples

Show the smallest useful example first.

A good example should be:

- realistic;
- copy-pasteable when possible;
- short enough to understand quickly;
- consistent with the repository's actual API or CLI;
- followed by a link to deeper documentation when needed.

Do not invent imports, functions, endpoints, flags, or output.

## Badges

Use badges intentionally.

Good badge categories include:

- build or CI status;
- package or release version;
- license;
- test coverage;
- supported runtime versions;
- downloads when relevant;
- contributors, stars, forks, or issues for community-oriented repository templates.

Keep badge styling consistent. Prefer `flat-square` unless the project already has a deliberate visual system.

## Images and visual design

Use visuals when they explain the project faster than text.

Good choices:

- one product screenshot;
- a short demo GIF;
- an architecture diagram;
- a workflow diagram;
- before/after examples.

Always include meaningful `alt` text. Prefer repository-relative image paths so forks and offline views remain robust.

Do not depend on unsupported HTML, JavaScript, or custom CSS.

## Links and navigation

- Prefer relative links for files inside the same repository.
- Use stable GitHub anchors; explicit HTML anchors are acceptable when heading-generated anchors may be ambiguous or localized.
- Check that branch names in links match the repository default branch.
- Keep external links purposeful and current.
- Use a compact navigation row or table of contents only when it meaningfully improves a long README.

## Bilingual and multilingual READMEs

For multiple languages:

- use predictable filenames such as `README.md`, `README.zh-CN.md`, or `BLANK_README.zh-CN.md`;
- add a language switcher near the top of every language version;
- keep section coverage approximately equivalent unless localization needs differ;
- keep code samples and commands synchronized across languages;
- update both versions when setup steps, links, or features change;
- avoid translating code identifiers and technical names that should remain exact.

## GitHub-native components

Use these sparingly when they improve comprehension:

- Markdown tables for compact comparisons or placeholder guides;
- `<details>` for optional or secondary material;
- GitHub callouts such as `[!NOTE]`, `[!TIP]`, `[!IMPORTANT]`, `[!WARNING]`, and `[!CAUTION]`;
- lightweight HTML for centered hero content and image sizing.

Do not turn every paragraph into a callout or every section into a collapsible block.

## Preserve attribution and licensing

When improving an existing template or fork:

- preserve required license notices;
- preserve meaningful upstream attribution;
- do not imply original authorship for inherited work;
- ensure displayed license information agrees with the repository license file.

## Quality checklist

Before finishing, verify:

- [ ] The title and description explain the project clearly.
- [ ] The first screen is not overcrowded.
- [ ] All project claims are supported by repository evidence or user-provided facts.
- [ ] Installation commands are correct.
- [ ] Usage examples match the real API, CLI, or workflow.
- [ ] Placeholder text is removed from project-specific READMEs.
- [ ] Internal links and image paths resolve correctly.
- [ ] External links point to the intended repository, docs, or service.
- [ ] Default branch names in URLs are correct.
- [ ] Badge styles are consistent and badges are useful.
- [ ] Images have alt text.
- [ ] Empty or irrelevant sections are removed.
- [ ] License and attribution information are accurate.
- [ ] Localized versions link to each other and remain structurally synchronized.
- [ ] The final README reads well on both desktop and narrow screens.

## Output behavior

When the user asks only for a README draft, return a complete ready-to-use Markdown document.

When repository write access is available and the user asks to modify a repository:

1. inspect existing files first;
2. make changes on a dedicated branch unless the user explicitly requests direct changes;
3. keep commits focused and descriptive;
4. review the final diff for broken links, unintended deletions, stale repository names, and placeholders;
5. create a pull request with a concise summary of the documentation changes unless the user explicitly asks to merge directly.
