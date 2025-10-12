Project: Material-Design-3-Dynamic-Mobile-Dashboard — Home Assistant Lovelace YAML

Quick context
- This repo is a single, large Home Assistant Lovelace dashboard expressed as YAML (`full_yaml`) plus helper folders: `template sensor/` and `hue asset/`.
- The UI is built from many custom HACS cards (see `README.md` -> "Requirements / Dependencies"). The dashboard heavily uses Jinja templating, decluttering templates, and conditional rendering.

What an AI agent should know to be productive
- Edit surface: Most UI code lives in `full_yaml`. Small changes there directly affect the dashboard layout and behavior. Refer to `README.md` for the full list of external card dependencies.
- Templates & sensors: `template sensor/` contains template sensors the dashboard expects. If an entity referenced in `full_yaml` isn't defined, check this folder before changing the dashboard.
- Hue integration helpers: `hue asset/` contains automations/scripts/input_* helpers required by the Hue scenes features; don't remove these unless replacing functionality.
- Navigation & routes: The `navbar-card` in `full_yaml` defines URLs (e.g. `/test-material-3/rooms`) and popups for room pages. Preserve the structure when adding new routes — update both the route and any matching view definitions in `full_yaml`.

Project-specific patterns to follow
- Jinja-heavy cards: Many card titles and contents are Jinja templates (e.g. greeting at top using `now().hour`, weather summaries using `state_attr(...)`). When modifying: keep filters, default fallbacks, and timezone-aware conversions (`as_datetime(...).astimezone()`).
- Decluttering card usage: The repo relies on `decluttering-card` templates to reuse complex card blocks. Look for `type: custom:decluttering-card` with `template:` entries; add new templates in place when extracting repeated blocks.
- Auto-entities & filtering: `custom:auto-entities` is used to generate card lists (lights, fans, etc.). Changes to entity groups (like `group: light.all_lights`) must match Home Assistant group/entity naming conventions used elsewhere.
- Custom card options: Many cards embed JS `data_generator` blocks (apexcharts) or `card_mod` CSS. Maintain indentation and quoting exactly; YAML is whitespace-sensitive and these blocks are treated as literal strings.

How to implement common edits
- Adding a new room view: add a route entry under `navbar-card.routes` and create a matching view/card block in `full_yaml` with the same URL path. Reuse existing room popups (see `popup:` entries under `rooms` route) as examples.
- Adding a sensor/entity reference: confirm the entity exists in `template sensor/` or in the user's HA instance. For dashboard-only helper sensors, add a file under `template sensor/` and reference it from `full_yaml`.
- Updating themes/colors: Theme variables use Material You theme tokens (e.g. `--md-sys-color-tertiary`). Search for `--md-sys-` in `full_yaml` and update the token or card_mod styles there.

Dev & debugging notes
- There's no build system — this is raw Lovelace YAML. Validate changes by pasting snippets into Home Assistant UI or using the Lovelace YAML validator in HA.
- Common failure modes: missing custom cards (install via HACS), undefined entities (sensor/entity not created), and YAML indentation errors. When you see a template referencing `state_attr('sensor.xyz','...')`, ensure `sensor.xyz` exists or provide a safe default.
- When editing `data_generator` JavaScript blocks (apexcharts), test logic with a small sample of the expected `attributes.forecasts` shape (objects containing datetime, precipitation, temperature, wind_speed, wind_bearing).

Files & places to check for context
- `full_yaml` — main dashboard. Primary edit target.
- `README.md` — dependency list and install notes (HACS components, cards to install).
- `template sensor/` — template sensors used by dashboard (look here for missing entities referenced in `full_yaml`).
- `hue asset/` — automations, scripts, and inputs used for Hue scene controls.

Small examples (copy/paste friendly)
- Greeting header (do not remove timezone handling):
  {% set time = now().hour %} {% if time >= 18 %} 🌙 Guten Abend, {{ user }}! ...
- Auto-entities filter sample (lights on): `group: light.all_lights` with options `{ type: custom:google-slider-card }` — preserve `entity_id` patterns.

If you’re unsure
- Prefer safe, minimal changes: add a conditional wrapper (`type: conditional`) so new UI blocks don't break for users missing entities.
- Ask the repo owner before removing any `decluttering-card` templates or Hue assets — they are used across many views.

After updating
- Run quick validation in Home Assistant UI. Report broken cards (card errors usually show in the frontend console or in Lovelace UI preview).

If anything in this file is unclear or you'd like the instructions expanded (examples for adding a room, extracting decluttering templates, or testing apexcharts `data_generator`), tell me which section and I'll iterate.
