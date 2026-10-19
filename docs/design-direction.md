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
