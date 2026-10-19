# Hashtiva workspace redesign

Reviewed public product descriptions and documentation on 2026-10-19:
- https://novinhub.ir/ and /publish: shared publishing queue, content calendar, unified conversations and team workflow.
- https://vardast.chat/ and /docs/smart-dm-automation: knowledge-grounded assistant, keyword triggers, editable message preview and human handoff. Inspected the publicly linked workflow editor screenshot.
- https://yektabot.com/ and /features: product catalogue and order follow-up alongside conversations.

These are workflow references, not copies of competitor branding or private dashboards. Hashtiva retains the supplied logo, navy/blue/cyan palette and Persian RTL typography.

The home screen prioritizes tasks, content review and assistant setup. The inbox joins conversation status, reply review and customer context. Automation has explicit trigger/message/edit states. Knowledge sources, products, order status and content dates persist in browser storage. Calendar entries use actual selected dates.

This remains a frontend prototype. Social accounts, orders and metrics are illustrative; no OAuth, payments, external messaging or AI inference is connected. Assistant suggestions are labelled prepared examples.

Validation: JavaScript syntax checks plus isolated DOM-stub checks for all 14 routes and local knowledge, flow, reply, product, order and calendar operations. Browser rendering and visual inspection of the deployed UI were unavailable in this environment.

## Product workflow iteration

The composer now owns new and edited posts through a three-step dialog: channels and media, per-network copy/preview, and review/scheduling. It validates title, target accounts, captions, image content, future dates, demo connection state and reviewer role. Uploads are restricted to PNG/JPEG/WebP up to 1 MiB; quota failures retain the editor for correction. Browser-local drafts carry review status, source context and audit records.

Conversation context now includes tags, internal notes, ownership, handoff and linked orders. Prepared recommendations link a conversation or knowledge item to an editable draft; the assistant panel also offers a draft action. Onboarding, simulated channel errors/retries, local reports, role simulation and team history remain explicitly marked as prototype behavior. No real invitations, messages, social connections, scheduled publishing or AI calls occur.

Additional isolated checks cover all 16 routes, review permissions, past/future scheduling, image requirements, disconnected accounts, caption variants, notes/tags, team members and audit persistence. Visual browser QA remains unavailable.

## Ocean identity — October 2026

Palette supplied by the owner: Deep Ocean `#0B2D5B`, Indigo Purple `#6A5ACD`, Teal `#14B8A6`, Coral `#FF8A5B`, Slate `#94A3B8`, Cloud `#F5F8FF`. Cloud and navy establish the surfaces, indigo identifies AI and primary actions, teal indicates activity, and coral highlights selected calls to action. Darker slate and teal companions are used for small text. Network identity colors remain recognizable.

`dist/ocean.css` is the final identity layer, loaded after the four product stylesheets. `octopusIcon()` is the shared code-native vector used by AI controls, cards and the floating assistant; `assets/octopus.svg` provides the same mark for inline image use. The `spark` icon key intentionally resolves to this octopus for existing callers. Preserve this mapping when componentizing the prototype.

Validation: JavaScript syntax and existing DOM-stub workflow checks passed across 16 routes. Browser visual QA remains outstanding.

## Graphic expansion

`visual.css` and `visual.js` add illustration-led page covers, a six-color ribbon asset, an iridescent octopus, network constellation, content card compositions, larger content previews, workflow icons and a report bar chart. The chart uses the same sample conversation counts and range toggle as the table. Decorative art is hidden from accessibility APIs; existing actions remain text-labeled and usable. All six supplied swatches appear in the visual signature and illustrations. These are SVG/CSS graphics with no image-generation or third-party asset dependency. Visual mobile layouts stack the covers below 700px. Existing DOM-stub workflows pass with the final visual layer loaded; full browser visual QA remains required.

## Feature-specific layouts

The repeated page-cover system has been removed. `features.css` and `visual.js` now provide a distinct command dashboard, studio format desk, inbox state filters, knowledge-library composition and workflow canvas. Other feature surfaces retain their task-specific controls with scoped styling via `data-view`. The dashboard readiness ring is computed from approved/scheduled content; counts reflect browser-local state. Format shortcuts open the existing composer. Theme control now reflects the selected state, persists preference and labels its next action. DOM-stub checks pass for all 16 routes; browser visual QA remains outstanding.
