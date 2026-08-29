---
name: readme-writing
description: Create, audit, rewrite, localize, and polish GitHub README files using the Best-README-Template structure, repository-verified facts, bilingual English/Simplified Chinese output by default, and GitHub-native visual design. Use for new README creation, README redesigns, bilingual README work, template generation, or documentation quality reviews.
---

# README Writing

Create README files that help a new visitor answer four questions quickly:

1. What is this project?
2. Why should I care?
3. How do I run or use it?
4. Where do I go next?

Optimize for clarity, accuracy, scanability, maintainability, and **template consistency** before decoration.

## Non-negotiable defaults

Unless the user explicitly asks for something different:

1. **Use the canonical Best-README-Template as the visual and structural contract.** Do not merely use it as inspiration.
2. **Produce bilingual documentation:**
   - `README.md` — English
   - `README.zh-CN.md` — Simplified Chinese
3. **Keep both language versions structurally synchronized.** The same project facts, commands, examples, badges, and major sections must appear in both versions.
4. **Put the language switcher in the hero CTA row**, alongside links such as Get Started, Documentation, and Issues. Do not place the language switcher as a detached line above the hero.
5. **Inspect the repository before writing.** Never invent commands, APIs, environment variables, features, license information, screenshots, deployment methods, or project claims.
6. **Map repository facts into the template skeleton.** Do not preserve a weak or unrelated existing README layout just because it already exists.

These defaults are part of the skill's expected output, not optional suggestions.

## Canonical templates

Always fetch and inspect the current templates before creating or substantially redesigning a README when network access is available.

### English

- Rendered: https://github.com/NakanoSanku/Best-README-Template/blob/main/BLANK_README.md
- Raw: https://raw.githubusercontent.com/NakanoSanku/Best-README-Template/main/BLANK_README.md

### 简体中文

- Rendered: https://github.com/NakanoSanku/Best-README-Template/blob/main/BLANK_README.zh-CN.md
- Raw: https://raw.githubusercontent.com/NakanoSanku/Best-README-Template/main/BLANK_README.zh-CN.md

The URLs are intentionally absolute so this skill can be installed, copied, or distributed independently without requiring the rest of the template repository locally.

When an agent can fetch remote files, prefer the **Raw** URLs for obtaining the template source and the **Rendered** URLs when a human-facing link is useful.

If network access is unavailable, follow the template contract below instead of inventing a different design.

## Template contract

The canonical template defines the default README skeleton. Preserve its visual grammar and section hierarchy while replacing placeholders with verified project content.

### Required visual grammar

A project README should normally contain, in this order:

1. `<a id="readme-top"></a>` anchor.
2. Centered hero using lightweight HTML.
3. Project logo/icon when a verified repository asset exists.
4. Centered project title.
5. One strong value proposition.
6. One short supporting sentence when useful.
7. **One CTA row** containing the primary action, useful project links, and language switcher.
8. Centered badge row.
9. Compact centered section navigation.
10. Horizontal rule before the main content.
11. Template-aligned content sections.
12. One back-to-top link near the end.
13. Reference-style badge/link definitions where practical.

Do not replace this structure with a completely different README design unless the user explicitly requests a different style.

### Hero CTA contract

For bilingual project READMEs, the English version should follow this pattern conceptually:

`Get Started → · Documentation · Issues · English · 简体中文`

The Chinese version should follow this pattern conceptually:

`快速开始 → · 文档 · Issues · English · 简体中文`

The currently active language may be emphasized with `<strong>`.

Use repository-relative language links in generated project READMEs:

- English: `README.md`
- 简体中文: `README.zh-CN.md`

If the repository already uses another established localization filename convention, preserve that convention consistently.

### Core section order

Use the following order as the default backbone:

1. `About the Project` / `项目介绍`
2. Preview or screenshot, **only when a real visual asset exists**
3. `Highlights` / `项目亮点`
4. `Built With` / `技术栈`
5. `Getting Started` / `快速开始`
6. `Usage` / `使用方法`
7. Project-specific sections that genuinely add value
8. `Roadmap` / `路线图`, when real roadmap information exists
9. `Contributing` / `参与贡献`, when contributions are accepted
10. `License` / `许可证`, only when a verified license exists
11. `Contact` / `联系方式`, when meaningful contact information exists
12. `Acknowledgments` / `致谢`, when relevant

A project may omit sections that are unsupported or irrelevant, but **do not casually reorder the backbone or replace it with an unrelated information architecture**.

Project-specific sections such as architecture, synchronization behavior, deployment, data semantics, security notes, or API details should be inserted after the closest relevant core section rather than replacing the template backbone.

## Template alignment rules

When adapting the template to a real repository:

- Preserve the centered hero composition.
- Preserve the CTA-row style and include language switching in that row.
- Preserve a compact badge block beneath the hero.
- Preserve a compact section navigation row when the README is long enough to benefit from it.
- Prefer explicit anchors such as `<a id="getting-started"></a>` so English and localized headings remain stable.
- Use one accent emoji per major section when consistent with the template.
- Keep badge styles consistent, normally `flat-square`.
- Use Markdown reference links for repeated badge/repository URLs where this keeps the source readable.
- Keep the overall spacing and hierarchy close to the canonical template.

### Allowed deviations

Deviate from the template only when repository evidence or project type requires it. Examples:

- A library may move installation and minimal usage earlier.
- A CLI may emphasize command examples over screenshots.
- A private/internal project may omit community badges.
- A repository with no license file must not invent a license section or badge.
- A project with no screenshot asset should omit the preview image instead of fabricating one.

When deviating, keep the same visual language and return to the template backbone afterward.

## Bilingual output contract

Bilingual output is the default for this skill.

### New README

Create both:

- `README.md`
- `README.zh-CN.md`

### Existing README improvement

- If only `README.md` exists, improve it and create `README.zh-CN.md`.
- If only `README.zh-CN.md` exists, improve it and create `README.md`.
- If both exist, update both together.
- If the repository already has another language structure, follow it while keeping English and Simplified Chinese synchronized when requested or already present.

### Synchronization requirements

Both language files must share:

- the same hero layout;
- the same image/logo assets;
- the same badges;
- equivalent CTA destinations;
- equivalent major sections;
- identical installation commands;
- identical code samples unless comments are intentionally localized;
- identical environment variable names;
- equivalent tables and feature coverage;
- equivalent deployment and contribution instructions.

Translate prose naturally. Do not mechanically translate technical identifiers, commands, filenames, package names, API names, environment variable names, code identifiers, or URLs.

Before finishing, compare the two files section by section. A bilingual deliverable is incomplete if one language is materially missing content present in the other.

## When to use this skill

Use this skill when asked to:

- create a README from scratch;
- improve or redesign an existing README;
- turn repository facts into polished project documentation;
- create a reusable README template;
- translate or localize a README;
- add badges, screenshots, navigation, examples, or contribution guidance;
- review a README for structure, correctness, template alignment, or visual quality.

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
- existing README text containing project-specific facts that should be retained.

If repository evidence conflicts with the current README, prefer repository evidence and avoid unsupported claims.

### Evidence hierarchy

Prefer evidence in this order:

1. Repository source/configuration files.
2. CI/deployment configuration.
3. Existing project documentation and ADRs.
4. Current README factual content.
5. User-provided facts.

Do not infer a feature merely from an installed dependency.

## README modes

### New README

1. Fetch both canonical templates.
2. Inspect the repository.
3. Choose the relevant template sections.
4. Replace template placeholders with verified project facts.
5. Add project-specific sections without discarding the template structure.
6. Produce both English and Simplified Chinese versions.

### README improvement

Do **not** treat the existing README layout as sacred.

Preserve useful facts, working links, commands, examples, attribution, and project-specific explanations, then **re-map that content into the canonical template structure**.

The objective is not “edit the old README until it reads better.” The objective is “rebuild the README using verified existing content inside the template contract.”

### Localization

Translate meaning rather than words mechanically. Keep commands, filenames, identifiers, API names, package names, code, environment variables, and placeholders unchanged unless the localized project intentionally uses different values.

### Template creation

Use obvious, searchable placeholders such as:

- `github_username`
- `repo_name`
- `project_title`
- `project_description`
- `project_license`
- `email`

Explain placeholders in a removable note or collapsible block. Do not leave project-specific claims inside a reusable template.

## Writing style

Write for scanning first and deep reading second.

- Lead sections with the most useful fact.
- Prefer short paragraphs and meaningful bullets.
- Use concrete language instead of generic claims such as “awesome”, “powerful”, or “next-generation” unless evidence supports them.
- Explain benefits in user terms, not only implementation terms.
- Keep headings descriptive and predictable.
- Use terminology consistently throughout the document.
- Avoid repeating the same explanation in multiple sections.
- Keep the hero copy concise; move detail into `About`.

## About and highlights

The About section should explain:

1. the problem or workflow the project addresses;
2. what the project does;
3. who benefits from it;
4. an important architectural or product boundary when that materially affects usage.

Highlights should contain the strongest verified capabilities, normally 3–8 items. Avoid converting every implementation detail into a “feature.”

## Built With

Prefer compact visual badges for the primary stack, aligned with the template.

Only include technologies verified from manifests/configuration. Do not list every transitive dependency.

For example, a web app might show its primary framework, language, styling system, storage/scheduling layer, and major platform integration while leaving secondary utilities to deeper documentation.

## Installation rules

Installation instructions are high-risk documentation because incorrect commands immediately damage trust.

- Use commands verified from the repository whenever possible.
- Include the required runtime or tooling version when it materially affects setup.
- Show the correct working directory.
- Mention environment variables only when they actually exist.
- Never fabricate API keys, package names, script names, ports, or configuration files.
- Prefer a short successful path over documenting every possible setup variation.
- Link to or collapse advanced setup when it becomes too large for the primary flow.

## Usage examples

Show the smallest useful workflow first.

A good example should be:

- realistic;
- copy-pasteable when possible;
- short enough to understand quickly;
- consistent with the repository's actual API, UI, or CLI;
- followed by deeper documentation when needed.

For end-user web applications, a short “typical workflow” list may be more appropriate than invented code. Do not force a JavaScript code sample into a UI application just because the generic template contains one.

Do not invent imports, functions, endpoints, flags, or output.

## Badges

Use badges intentionally and keep styling consistent.

Good badge categories include:

- CI/build status;
- package or release version;
- license, only when verified;
- supported runtime version;
- primary framework version when useful;
- contributors, stars, forks, or issues for public community repositories.

Default to `flat-square` to match the canonical template.

Avoid decorative badge walls. A focused row is better than exhaustive metadata.

## Images and visual design

Use visuals when they explain the project faster than text.

Good choices:

- one product screenshot;
- a short demo GIF;
- an architecture diagram;
- a workflow diagram;
- before/after examples.

Always include meaningful `alt` text.

Prefer repository-relative image paths for project assets. If no suitable visual asset exists, omit the preview block instead of using a fake placeholder in a project-specific README.

Do not depend on unsupported HTML, JavaScript, or custom CSS.

## Links and navigation

- Prefer relative links for files inside the generated project's repository.
- Use stable GitHub anchors; explicit HTML anchors are preferred for localized/bilingual documents.
- Check that branch names in absolute URLs match the repository default branch.
- Keep external links purposeful and current.
- Keep the language switcher in the hero CTA row.
- Keep the section navigation compact and centered for long READMEs.

## Project-specific extension sections

Real projects often need more detail than the generic template. Add those sections without losing template alignment.

Examples:

- architecture or lifecycle;
- data/storage semantics;
- authentication setup;
- cloud integration;
- deployment;
- API configuration;
- security constraints;
- repository guide;
- development/testing commands.

Prefer `<details>` for long secondary setup instructions when collapsing them improves readability.

Do not let project-specific sections push `Getting Started` so far down that new users cannot quickly run the project.

## GitHub-native components

Use these sparingly when they improve comprehension:

- Markdown tables for compact comparisons or configuration references;
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

If no license file or explicit license declaration exists, do not invent a license badge or section. You may omit License entirely.

## Quality checklist

Before finishing, verify all applicable items.

### Template alignment

- [ ] The canonical English and Chinese templates were fetched or the embedded template contract was followed.
- [ ] The hero is centered and visually follows the template.
- [ ] The CTA row contains primary links and the language switcher on the same row.
- [ ] Badges appear as a focused block below the hero.
- [ ] A compact section navigation row is present when useful.
- [ ] Major sections follow the template backbone unless there is a documented project-specific reason.
- [ ] Project-specific sections extend the template instead of replacing it.

### Accuracy

- [ ] The title and description explain the project clearly.
- [ ] All project claims are supported by repository evidence or user-provided facts.
- [ ] Installation commands are correct.
- [ ] Usage examples/workflows match the real project.
- [ ] Environment variable names are verified.
- [ ] Deployment instructions are verified.
- [ ] No license information is invented.
- [ ] No screenshots or assets are referenced unless they exist.

### Bilingual parity

- [ ] `README.md` exists as the English version unless the user explicitly requested otherwise.
- [ ] `README.zh-CN.md` exists as the Simplified Chinese version unless the user explicitly requested otherwise.
- [ ] Both files link to each other from the hero CTA row.
- [ ] Both files contain equivalent major sections.
- [ ] Commands, code, environment variables, URLs, and technical names are synchronized.
- [ ] Neither language version contains materially more project information than the other without a clear localization reason.

### Rendering and maintenance

- [ ] Internal links and image paths resolve correctly.
- [ ] External links point to the intended repository, docs, or service.
- [ ] Default branch names in URLs are correct.
- [ ] Badge styles are consistent and badges are useful.
- [ ] Images have alt text.
- [ ] Empty, placeholder, or irrelevant sections are removed.
- [ ] Reference-style links do not contain stale repository names.
- [ ] The final README reads well on both desktop and narrow screens.

## Output behavior

When the user asks only for README drafts, return **both complete ready-to-use documents** by default:

1. English `README.md`
2. Simplified Chinese `README.zh-CN.md`

Do not return only one language unless the user explicitly asks for a single-language deliverable.

When repository write access is available and the user asks to modify a repository:

1. inspect existing files first;
2. fetch the canonical English and Chinese templates;
3. inspect repository evidence;
4. create a dedicated branch unless the user explicitly requests direct changes;
5. update or create both `README.md` and `README.zh-CN.md`;
6. keep commits focused and descriptive;
7. compare both language files for structural/content parity;
8. review the final diff for broken links, unintended deletions, stale repository names, template drift, and placeholders;
9. create a pull request with a concise summary unless the user explicitly asks to merge directly.

A README task is not complete when the English file looks polished but the Chinese counterpart is missing, or when the content is accurate but the document visibly abandons the canonical template.