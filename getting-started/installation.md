---
title: Installation
description: Get started by installing the required dependencies
---

# Installation

Welcome to the installation guide. This guide will walk you through setting up your development environment.

## Prerequisites

Before you begin, make sure you have the following installed:

- **Node.js** (version 18.0 or higher)
- **npm** or **yarn** package manager
- A code editor (we recommend VS Code)

## Installation Steps

### 1. Install Node.js

Download and install Node.js from the [official website](https://nodejs.org/).

```bash
# Verify installation
node --version
npm --version
```

### 2. Create a New Project

Use the following command to create a new project:

```bash
npx create-next-app@latest my-app
cd my-app
```

### 3. Install Dependencies

Install the required dependencies:

```bash
npm install
```

### 4. Start Development Server

Run the development server:

```bash
npm run dev
```

Your application should now be running at `http://localhost:3000`.

## Next Steps

Now that you have everything installed, check out the [Project Structure](/getting-started/project-structure) guide to understand how files are organized.
