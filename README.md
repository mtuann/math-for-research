# Math for CS / AI / Engineering Research

A public math site for building foundations, understanding advanced theory, reading papers, and learning how strong research work is assembled.

## Stack

- `Quarto`
- `GitHub Actions`
- `GitHub Pages`

## Current Structure

- `start-here/`
- `roadmaps/`
- `topics/`
- `applications/`
- `paper-lab/`
- `research/`
- `publication/`
- `library/`
- `notes/`

## Contributor Standards

- sourcing policy: [CONTRIBUTING.md](CONTRIBUTING.md)
- page rules: [contributing/page-templates.md](contributing/page-templates.md)
- research-facing page rules: [authoring/research_page_templates.md](authoring/research_page_templates.md)
- starter files: [contributing/templates](contributing/templates/README.md)

## Planning Docs

- site structure: [website_syllabus_tree.md](website_syllabus_tree.md)
- advanced expansion: [advanced_syllabus_tree.md](advanced_syllabus_tree.md)
- reference roadmap: [math_foundation_reference_roadmap.md](math_foundation_reference_roadmap.md)
- production map: [content_production_map.md](content_production_map.md)

## Local Preview

Once Quarto is installed:

```bash
quarto preview
```

To render the full site:

```bash
quarto render
```

## Deployment

The site is set up to publish to GitHub Pages using:

- `.github/workflows/publish.yml`

Pushes to `main` trigger a build and deploy workflow.
