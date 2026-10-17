# Project Structure

This repository contains multiple 3D websites and motion projects, each deployed separately to Vercel.

## Folder Organization

```
3D/
├── liquid-gold/          # Project 1: Liquid Gold effect
│   ├── index.html
│   ├── assets/
│   ├── vercel.json       # Vercel config for this project
│   └── README.md
│
├── 5sense/               # Project 2: 5Sense project
│   ├── index.html
│   ├── assets/
│   ├── vercel.json
│   └── README.md
│
├── getplate/             # Project 3: GetPlate (glass effect)
│   ├── index.html
│   ├── assets/
│   ├── vercel.json
│   └── README.md
│
└── README.md             # Main documentation
```

## Deploying to Vercel

### Option 1: Deploy Each Folder as Separate Site
1. Go to [Vercel Dashboard](https://vercel.com)
2. Click "Add New" → "Project"
3. Import this GitHub repo
4. For each project folder:
   - Set **Root Directory** to the folder name (e.g., `liquid-gold/`)
   - Deploy

### Option 2: Single Monorepo Deployment
Create a `vercel.json` at the root with routing rules to serve different folders.

## Adding New Projects

1. Create a new folder: `mkdir project-name`
2. Add your HTML files and assets
3. Create a `vercel.json` config (optional):
   ```json
   {
     "buildCommand": "echo 'Static site'",
     "outputDirectory": "."
   }
   ```
4. Commit and push:
   ```bash
   git add project-name/
   git commit -m "Add project-name"
   git push
   ```

## Current Projects

- **liquid-gold-standalone.html** - Liquid gold effect demo
- **5sense.html** - 5Sense project
