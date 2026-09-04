# Shopify Theme Guardrails

## Non-Negotiable Guardrails
- **Presentation Layer Focus**: Modify the presentation layer only unless a functional change is explicitly requested. Preserve Shopify Liquid, section schemas, snippets, routes, product objects, product forms, variant selection, quantity controls, cart drawer/page behavior, checkout links, customer account links, localization, analytics hooks, accessibility attributes, and responsive behavior.
- **Native Shopify Data & Flow**: Do not replace Shopify product data with hardcoded product names, prices, variants, images, inventory, or URLs. Do not create a fake cart, fake checkout, fake account system, or static product form. Use the existing theme’s native objects, snippets, settings, and endpoints.
- **Pre-Edit Inspection**: Before editing, inspect the repository structure and identify the main layout, homepage template, header, footer, product section, cart components, customer-account links, global CSS, JavaScript entry points, and existing section schemas. Reuse existing components where possible.
- **Minimal & Safe Changes**: Make the smallest safe change needed for the requested section. Do not refactor unrelated files. Do not delete existing settings or schema options. If a file is shared by multiple templates, confirm that the change will not unintentionally affect unrelated pages.
- **Accessibility & CSS Standards**: Use semantic HTML, keyboard-accessible controls, visible focus states, meaningful alt text from Shopify image data, and mobile-first responsive CSS. Avoid inline styles unless the existing theme convention requires them. Prefer theme settings and section settings over hardcoded values.
- **Completion Reporting**: At the end of every task, report:
  1. Files changed
  2. What was intentionally left untouched
  3. Any assumptions made
  4. A short manual test checklist
