# Copilot Instructions for aoai-devday-2025

This is a **Slidev presentation project** about "生成AIを活用したVS Codeによるこれからの開発体験" (The Future of Development Experience in VS Code with Generative AI).

## Project Architecture

- **Main presentation file**: `slides.md` - Single markdown file containing all slides with YAML frontmatter
- **Theme**: Uses Slidev's "seriph" theme with custom slide transitions
- **Development server**: Vite-based, runs on port 3030
- **Package manager**: pnpm (required, not npm/yarn)

## Key Development Workflows

### Starting Development

```bash
pnpm install
pnpm dev  # Opens browser automatically at localhost:3030
```

### Building & Export

```bash
pnpm build    # Static site for hosting
pnpm export   # PDF/PPTX export
```

## File Structure Patterns

- **Empty directories**: `components/`, `pages/`, `snippets/` are reserved for Slidev components/layouts but currently unused
- **Slide content**: All presentation content lives in single `slides.md` file
- **Configuration**: Vite config only sets server port (3030) and host settings

## Slidev-Specific Conventions

### Slide Syntax in slides.md

- Slides separated by `---` markers
- YAML frontmatter at top for theme, title, transitions
- MDC (Markdown Components) syntax enabled
- Supports Vue components inline

### Example slide structure:

```markdown
---
transition: slide-left
---

# Slide Title

Content here with Vue/MDC syntax support
```

## Development Environment

- **Dev Container**: Node.js 22 with TypeScript, includes Slidev extension
- **VS Code Extensions**: Slidev, Vue.volar, Prettier auto-configured
- **Formatting**: Auto-format on save enabled, Emmet for markdown
- **Port forwarding**: 3030 automatically forwarded in dev container

## Content Focus

This presentation covers VS Code's evolution with GitHub Copilot and future AI-powered development experiences. When editing content, maintain the technical conference presentation style and focus on developer tooling innovations.

## Important Notes

- Use pnpm only (not npm/yarn) - project configured specifically for pnpm
- Slidev presentations are single-file by design - avoid splitting slides across files
- Theme customization should be done via frontmatter, not separate CSS files
- Preview changes instantly via hot reload on localhost:3030
