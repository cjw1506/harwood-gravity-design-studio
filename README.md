# Harwood Gravity Forms Design Studio

A private, browser-based studio for building and styling Gravity Forms, staff notifications, patient confirmations, and on-screen confirmation messages.

## Questions and conditional logic

Open **Questions & Logic** after importing a Gravity Forms JSON export, or select **Create blank form**. The workspace can:

- add, edit, duplicate, remove, and reorder common Gravity Forms field types;
- create multi-page forms with page and section markers;
- apply optional show/hide rules using earlier questions;
- test routes with sample answers and explain why each item is shown or hidden;
- validate missing controllers, deleted choices, ordering problems, circular dependencies, and unsafe nested logic before export;
- keep field IDs stable when labels or positions change; and
- preserve unfamiliar imported field types without silently discarding their specialised settings.

Gravity Forms does not natively model every possible chain of nested conditional rules. The studio safely expands simple **Show + All** chains and blocks ambiguous nested rules from export.

## WordPress import

Use **Export** in the Questions & Logic workspace (or **Export for Gravity Forms** in Copy code), then import the resulting single JSON file in WordPress under **Forms → Import/Export → Import Forms**. The package contains the form definition, notification and confirmation HTML, and a hidden Harwood Studio HTML field containing the scoped form CSS.

The live-form preview is based on the measured Practice365 frontend: Gravity Forms 2.10.5, its `gform-theme--no-framework` and NHS class structure, a 12-column field grid, composite field containers, Frutiger W01 with Arial fallback, and the published label/control/button metrics. Exported CSS uses the same selectors and pixel-based typography. The **Fidelity** workspace explains which details remain browser- or theme-dependent.

## Run locally

Open `index.html` in a modern browser. The application has no build step, backend, external dependencies, analytics, or network requests. Imported forms and separately created blank forms remain available as independent local projects.

## Privacy

Imported form definitions and saved design settings remain in the browser's local storage. Do not use real patient data in previews.

## Deployment

This is a static site. Deploy the repository root to any static hosting service with no build command and `/` as the output directory.
