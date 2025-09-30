# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

This repository uses **Trunk** for formatting, linting, and development workflows:

### Development Environment
```bash
# Install Mintlify CLI for local development
npm i -g mintlify

# Start local development server
mintlify dev

# Install Trunk CLI for formatting and linting
npm i -g @trunkio/launcher
```

### Formatting and Linting
```bash
# Format all files (runs automatically on save)
trunk fmt

# Run lint checks on changed files
trunk check

# Run lint checks on all files
trunk check --all
```

### Style and Documentation
- Uses **Vale** for style checking against Google's Developer Documentation Style Guide
- Uses **Mintlify** for documentation site generation and hosting
- Auto-deploys to production on pushes to `main` branch

## Architecture and Structure

### Project Type
This is a **documentation repository** for Hypermode's open source projects:
- **Dgraph** - distributed graph database
- **Badger** - embeddable key-value store
- **Ristretto** - embeddable memory cache

### Content Organization
- **Root level**: Main documentation pages (`.mdx` files)
- **`dgraph/`**: Documentation for Dgraph database (primary content)
- **`badger/`**: Documentation for Badger key-value store
- **`snippets/`**: Reusable code snippets for documentation
- **`images/`**: Static image assets

### Configuration Files
- **`docs.json`**: Mintlify configuration (navigation, themes, settings)
- **`.trunk/trunk.yaml`**: Trunk configuration for linting and formatting
- **`styles/`**: Vale style configuration and vocabulary files

### Content Format
- All documentation is written in **MDX** (Markdown with JSX components)
- Uses Mintlify-specific components for enhanced documentation features
- Follows Google's Developer Documentation Style Guide
- Icons sourced from Font Awesome catalog

### Development Workflow
1. Make changes to `.mdx` files
2. Test locally with `mintlify dev`
3. Trunk automatically formats on save
4. Run `trunk check` before committing
5. Push to `main` for automatic deployment

### Important Notes
- **Homepage**: Now redirects to `/dgraph/overview` (Dgraph is the primary focus)
- **Navigation**: Contains only Dgraph and Badger tabs
- **Global Navigation**: Only "Dgraph Cloud" anchor remains