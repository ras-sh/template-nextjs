# @ras-sh/template-nextjs

▲ A production-ready template for quickly scaffolding Next.js projects with best practices and modern tooling.

## Features

- **[Next.js 15](https://nextjs.org)** - React framework with App Router and file-based routing
- **Turbopack** - Next-generation bundler for fast development
- **React 19** - Latest React with modern features
- **TypeScript** - Full type safety with `@ras-sh/typescript-config`
- **Tailwind CSS v4** - Utility-first CSS framework
- **@ras-sh/ui** - Component library built on Radix UI
- **Biome** - Fast linting and formatting via `ultracite`
- **Cloudflare Workers** - Ready for deployment with Wrangler
- **Geist Fonts** - Variable fonts for modern typography
## Quick Start

```bash
pnpm install
pnpm dev
```

## Customization

This template is configured with ras.sh defaults. To customize for your own project:

### Required Changes

1. **package.json** - Update project metadata:
   - `name` - Your package name
   - `description` - Your app description
   - `homepage` - Your website URL
   - `bugs.url` - Your repository issues URL
   - `bugs.email` - Your support email
   - `repository.url` - Your repository URL
   - `author` - Your name, email, and website

2. **app/layout.tsx:15-18** - Update default metadata:
   - `title` - Your site title
   - `description` - Your site description

3. **public/site.webmanifest:2-3** - Update PWA manifest:
   - `name` - Your app name
   - `short_name` - Your app short name

4. **wrangler.jsonc:3** - Update Cloudflare Workers name:
   - `name` - Your worker name

5. **app/page.tsx** - Replace with your landing page content

### Optional Changes

- **public/** - Replace favicon and icons with your own branding
- **LICENSE** - Update license holder if needed

## Scripts

| Command | Description |
|---------|-------------|
| `pnpm dev` | Start development server (port 3000) |
| `pnpm build` | Build for production |
| `pnpm preview` | Preview production build |
| `pnpm deploy` | Deploy to Cloudflare Workers |
| `pnpm cf-typegen` | Generate Cloudflare Workers types |
| `pnpm check-types` | Run TypeScript type checking |
| `pnpm check` | Run linter checks |
| `pnpm fix` | Auto-fix linting issues |

## Project Structure

```
.
├── app/
│   ├── page.tsx             # Home page
│   ├── layout.tsx           # Root layout
│   └── globals.css          # Global styles
├── public/                  # Static assets
├── next.config.ts           # Next.js configuration
└── wrangler.jsonc           # Cloudflare Workers configuration
```

## Deployment

```bash
pnpm deploy
```

Configured for Cloudflare Workers with Node.js compatibility enabled.

## License

MIT License - see the [LICENSE](LICENSE) file for details.
