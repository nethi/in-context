# in-context

Shared Context and Exchange. A public notebook for notes, links, essays, and evolving thoughts.

## Repository Structure

- `content/`: The permanent source of truth for all notes and articles. Tool-agnostic Markdown.
  - `notes/`: Zettelkasten or general notes.
  - `posts/`: Blog posts or essays.
  - `links/`: Curated links.
  - `journal/`: Periodic entries.
  - `assets/`: Images and other attachments.
- `renderers/`: Site generation tools.
  - `quartz/`: Initially used for rendering the content.
- `.github/workflows/`: CI/CD pipelines for automated deployment.

## Local Setup & Preview

To preview the site locally using Quartz:

1.  **Install dependencies:**
    ```bash
    cd renderers/quartz
    npm i
    ```

2.  **Run preview:**
    ```bash
    npx quartz build -d ../../content --serve
    ```

## Daily Workflow

Adding or updating content is straightforward:

```bash
git add content
git commit -m "Add notes"
git push
```

## Deployment

Deployment happens automatically via GitHub Actions whenever changes are pushed to the `main` branch. It builds the site using Quartz and deploys it to GitHub Pages.

- **Published URL:** `https://nethi.github.io/in-context/`
