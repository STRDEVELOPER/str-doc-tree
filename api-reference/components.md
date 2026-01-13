---
title: Components
description: API reference for available components
---

# Components

This page documents the main components used in the documentation site.

## AppSidebar

The main navigation sidebar component.

### Props

- `navigation` - Array of navigation sections
- All standard Sidebar component props from shadcn/ui

### Features

- **Collapsible sections** - Click to expand/collapse
- **Active state** - Highlights current page
- **Auto-expand** - Opens section containing active page
- **Responsive** - Mobile-friendly with trigger button

### Usage

```tsx
import { AppSidebar } from "@/components/app-sidebar"
import { getNavigation } from "@/lib/navigation"

const navigation = getNavigation()

<AppSidebar navigation={navigation} />
```

## Breadcrumb

Navigation breadcrumbs showing the current page location.

### Components

- `Breadcrumb` - Container component
- `BreadcrumbList` - List wrapper
- `BreadcrumbItem` - Individual breadcrumb item
- `BreadcrumbLink` - Clickable breadcrumb link
- `BreadcrumbPage` - Current page (non-clickable)
- `BreadcrumbSeparator` - Visual separator between items

### Example

```tsx
<Breadcrumb>
  <BreadcrumbList>
    <BreadcrumbItem>
      <BreadcrumbLink href="/">Home</BreadcrumbLink>
    </BreadcrumbItem>
    <BreadcrumbSeparator />
    <BreadcrumbItem>
      <BreadcrumbPage>Current Page</BreadcrumbPage>
    </BreadcrumbItem>
  </BreadcrumbList>
</Breadcrumb>
```

## Sidebar

Core sidebar component from shadcn/ui.

### Sub-components

- `SidebarProvider` - Context provider for sidebar state
- `SidebarInset` - Main content area
- `SidebarTrigger` - Button to toggle sidebar
- `SidebarMenu` - Menu container
- `SidebarMenuItem` - Menu item wrapper
- `SidebarMenuButton` - Clickable menu button

## Collapsible

Used for expandable sections in the sidebar.

### Components

- `Collapsible` - Container with state management
- `CollapsibleTrigger` - Click target to toggle
- `CollapsibleContent` - Content that shows/hides

### States

- `defaultOpen` - Initial open state
- `data-[state=open]` - CSS state for styling

All components are built with shadcn/ui and fully customizable with Tailwind CSS.
