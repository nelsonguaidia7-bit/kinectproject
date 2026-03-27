
  # Student Portfolio Site (Community)

  This is a code bundle for Student Portfolio Site (Community). The original project is available at https://www.figma.com/design/TsXmgjhbDVHzOfMZjkPPF2/Student-Portfolio-Site--Community-.

  ## Running the code

  Run `npm i` to install the dependencies.

  Run `npm run dev` to start the development server.

  ## Deploy on Cloudflare Pages

  This app is a Vite + React SPA. Use **Cloudflare Pages** with your Git repo:

  1. **Workers & Pages** → **Create** → **Pages** → **Connect to Git** → pick this repository.
  2. **Build configuration:**
     - **Root directory:** `Studentportfoliositecommunity-main`
     - **Build command:** `npm ci && npm run build`
     - **Build output directory:** `dist`
  3. This folder includes **`wrangler.toml`** (`pages_build_output_dir = "./dist"`) so Wrangler / Pages tooling can find the project. If the **repository root** is your working directory, use the **`wrangler.toml`** at the repo root (it points at `./Studentportfoliositecommunity-main/dist`).
  4. **Environment variables (optional):** set `NODE_VERSION` to `20` (or rely on `.nvmrc`; Cloudflare reads it when using **Framework preset: None** or set the env var).
  5. Deploy. After the first build, assign a custom domain under **Custom domains** if needed.

  `public/_redirects` sends all routes to `index.html` so React Router (e.g. `/project/:id`, `/author/:id`) works on refresh and deep links.
