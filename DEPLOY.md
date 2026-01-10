# Deploy to Vercel

This API is configured to be easily deployed on [Vercel](https://vercel.com).

## Automatic Deployment

1.  **Push Changes**:
    ```bash
    git add .
    git commit -m "Add Vercel deployment configuration"
    git push origin main
    ```

2.  **Deploy**:
    *   Click the **Deploy with Vercel** button in the `README.md`.
    *   **OR** Import your repository on Vercel.

### How it works
This project uses **Bun** to build the application for Vercel Serverless.
*   The `build` script in `package.json` runs `bun build`.
*   This transforms `api/_entry.js` (and all imports) into a single optimized `api/index.js` file.
*   **Note**: A `public` directory with an `index.html` is required by Vercel when a build script is present, even if not served directly. This project includes one.
*   Vercel deploys `api/index.js` as a Node.js Serverless Function.

## Manual Deployment (CLI)

1.  Install Vercel CLI: `npm i -g vercel`
2.  Run `vercel` in the project root.
