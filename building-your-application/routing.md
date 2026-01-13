---
title: Routing
description: Learn about routing in your application
---

# Routing

This application uses file-based routing with dynamic routes for markdown content.

## How It Works

The routing system automatically generates routes based on your markdown folder structure:

```
markdowns/section-name/page-name.md
↓
/section-name/page-name
```

## Route Structure

### Static Routes

- `/` - Home page
- `/[section]/[item]` - Dynamic markdown pages

### Dynamic Parameters

The `[section]` and `[item]` segments are dynamic and match your folder structure:

- `section` - Folder name in `markdowns/`
- `item` - Markdown filename (without `.md`)

## Example Routes

Given this markdown structure:

```
markdowns/
├── getting-started/
│   └── installation.md
└── api-reference/
    └── components.md
```

The following routes are generated:

- `/getting-started/installation`
- `/api-reference/components`

## Navigation

The sidebar component automatically:

1. Scans the `markdowns/` directory
2. Builds the navigation tree
3. Highlights the active page
4. Opens the section containing the current page

## Breadcrumbs

Each page shows breadcrumbs for easy navigation:

**Home** → **Section Name** → **Page Title**

The breadcrumbs are automatically generated based on the current route.
