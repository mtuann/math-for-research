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

