---
title: Project Structure
description: Understanding the folder structure of your project
---

# Project Structure

This guide explains the organization of files and folders in your project.

## Root Directory

```
my-app/
├── app/              # Application routes and pages
├── components/       # Reusable React components
├── lib/             # Utility functions and helpers
├── public/          # Static assets
├── markdowns/       # Documentation markdown files
└── package.json     # Project dependencies
```

## Key Directories

### `/app` Directory

The `app` directory contains your application's routes and pages. Each folder represents a route segment.

- **layout.tsx** - Shared layout across pages
- **page.tsx** - The page component for a route
- **loading.tsx** - Loading state component

### `/components` Directory

This directory contains reusable React components:

- **UI components** - Buttons, inputs, cards, etc.
- **Feature components** - Sidebar, navigation, etc.

### `/lib` Directory

Utility functions, helpers, and business logic:

- **utils.ts** - Common utility functions
- **navigation.ts** - Navigation helpers
- **markdown.ts** - Markdown processing

### `/markdowns` Directory

**This is where all documentation content lives!** The structure is automatically reflected in the navigation:

```
markdowns/
├── getting-started/
│   ├── installation.md
│   └── project-structure.md
└── building-your-application/
    ├── routing.md
    └── data-fetching.md
```

Each folder becomes a section, and each `.md` file becomes a menu item.

## Configuration Files

- **next.config.ts** - Next.js configuration
- **tailwind.config.cjs** - Tailwind CSS configuration
- **tsconfig.json** - TypeScript configuration

## Adding New Content

To add new documentation:

1. Create a folder in `markdowns/` for a new section
2. Add `.md` files for individual pages
3. The navigation updates automatically!

No code changes needed - just add markdown files and they appear in the sidebar.
