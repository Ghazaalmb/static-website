# Hashtiva UI prototype

Persian RTL social-media workspace, built from the supplied Hashtiva product structure and brand assets.

Live preview: https://hashtiva-studio.brownmoss10.chatgpt.site

## Run locally

No Node packages or build step are required. From the project root:

```sh
python3 -m http.server 8080 --directory dist
```

Open http://localhost:8080. The `dist` directory is the authored static application, not a generated bundle. Use an HTTP server rather than opening files directly.

## Entry points

`dist/index.html` loads these scripts in order:

1. `app.js`: base shell, demo data, helpers and initial event handlers.
2. `upgrade.js`: social identities, assistant, calendar and channel UI.
3. `workspace.js`: operational dashboard, inbox, knowledge, products and orders.
4. `product.js`: composer, review workflow, customer context, onboarding, reports and team simulation.
5. `visual.js`: page illustrations and sample report visualization.

`ocean.css` and `visual.css` finish the shared palette and visual identity.

Matching CSS files are loaded in the same order. The layers currently override functions and extend shared state. They must remain in this order until refactored; they are not independent modules.

Assets include the supplied brand images and bundled Vazirmatn font. Confirm font and brand redistribution permissions before distributing the repository beyond the authorized project team.

## Scope

This is a frontend prototype, not the original Hashtiva Next.js application and not an API-integrated client. It uses browser localStorage, static sample metrics and prepared assistant suggestions. Social accounts, channel failures/retries, approvals, roles and scheduling are simulated. There are no real messages, OAuth connections, payments, invitations, AI inference or background publishing jobs.

Uploaded images remain as data URLs in local browser storage (PNG/JPEG/WebP, up to 1 MiB per image). This is unsuitable as production media storage. Role selection demonstrates the UX only; it is not authorization.

See [backend handoff](docs/backend-handoff-fa.md) for integration priorities and [design direction](docs/design-direction.md) for decisions and verification limits.

## Verification

```sh
node --check dist/app.js
node --check dist/upgrade.js
node --check dist/workspace.js
node --check dist/product.js
```

Isolated DOM-stub checks covered route rendering and key local state workflows during creation. They are not browser or end-to-end tests. Full visual and browser QA remains required, especially composer file inputs, mobile inbox, dialogs, calendar, storage limits and keyboard navigation.

## Hosting

`.openai/hosting.json` belongs to the existing Sites deployment. It is not a backend configuration file. For a separate GitHub handoff repository, omit it and Git metadata; keep the Sites project identity unchanged in the original checkout.
