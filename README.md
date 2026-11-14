# Kitchen Mode

Mobile-friendly recipe reader: ingredients first, then one step per screen.

## Deploy on Netlify
1. Unzip this folder and put it in a GitHub repository.
2. On Netlify, choose **Add new project → Import an existing project**, select the repository.
3. Netlify reads `netlify.toml`; deploy with no build command and publish directory `.`.
4. Open the resulting HTTPS URL in Android Chrome, then use **⋮ → Add to Home screen**.

**Important:** Drag-and-drop deployment of only `index.html` will not run the recipe extraction function. Use a Git-based Netlify deployment (or Netlify CLI) to deploy functions.

## Local development
`npm install` then `npx netlify dev`.

## Limitations
Automatic import works on sites exposing Recipe JSON-LD. Some sites block fetches or have no structured recipe data; use the manual-entry fallback. The wake lock requires HTTPS and browser support. Recipes are not uploaded to a user account or stored between visits. For security, deploy this function only with suitable request/rate controls if heavy public usage is expected.
