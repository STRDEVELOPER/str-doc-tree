---
title: Data Fetching
description: Understanding how markdown content is loaded and rendered
---

# Data Fetching

Learn how this documentation site fetches and displays markdown content.

## Server-Side Rendering

All markdown content is rendered on the server using Next.js App Router:

1. **File System API** - Node.js `fs` module reads markdown files
2. **Gray Matter** - Parses frontmatter metadata
3. **Remark** - Converts markdown to HTML
4. **Server Components** - Renders content server-side

## Markdown Processing

### Reading Files

The `lib/markdown.ts` module handles markdown processing:

```typescript
export async function parseMarkdown(filePath: string) {
  const fileContents = fs.readFileSync(filePath, 'utf8')
  const { data, content } = matter(fileContents)

  // Convert markdown to HTML
  const processedContent = await remark()
    .use(html)
    .process(content)

  return {
    title: data.title,
    content: processedContent.toString(),
    metadata: data
  }
}
```

### Frontmatter

Each markdown file can include frontmatter metadata:

```markdown
---
title: Page Title
description: Page description
author: Your Name
---

# Content starts here
```

## Navigation Building

The `lib/navigation.ts` module scans the file system:

```typescript
export function getNavigation(): NavSection[] {
  // Scan markdowns directory
  // Build navigation tree
  // Sort by numeric prefix
  return sections
}
```

## Performance

- **Static Generation** - Pages are pre-rendered at build time
- **No Client-Side Fetching** - All data loaded server-side
- **Caching** - File system reads are cached in production

## Adding Content

To add new content:

1. Create a markdown file in the appropriate folder
2. Add frontmatter with title and description
3. Write your content in markdown
4. Save the file - that's it!

The navigation and routing update automatically.
