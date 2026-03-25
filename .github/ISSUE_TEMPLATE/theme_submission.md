---
name: Theme Submission
about: Submit a CSS theme to be included in the Skin Manager store
title: "[THEME] "
labels: theme-submission
assignees: ''
---

**Theme name**

**Author**

**Description**

**Version**

**Jellyfin compatibility**

**Source repository**

**CSS URL**

**Preview image URL**

**Tags**

---

**Variables** *(optional)*

If your theme supports configurable variables, paste the `vars` array below. Leave this section blank if the theme has no variables.

Each variable needs: `key` (can be camelCase, PascalCase, or UPPER_SNAKE_CASE), `name`, `description`, `type`, and `default`. Available types: `text`, `color`, `number`, `boolean`.

The key is converted to a lower-kebab-case CSS custom property automatically. For example, `accentColor` becomes `--accent-color`. Your CSS should reference these via `var(--accent-color, fallback)`. Alternatively, you can use exact string substitution via `{{accent-color}}`.

```json
[
  {
    "key": "accentColor",
    "name": "Accent Color",
    "description": "Primary highlight color used throughout the theme.",
    "type": "color",
    "default": "#00a4dc"
  }
]
```

---

**Addon CSS sheets** *(optional)*

If your theme supports optional addon stylesheets toggled by boolean variables, list them here. Leave this section blank if the theme has no addons.

Addons are declared as `@sm-import-if` comments in your CSS file and a matching `boolean` var in `skins.json`. When the user enables the var, the addon stylesheet is fetched and appended to the theme.

In your CSS file:
```css
/* @sm-import-if VAR_KEY [https://cdn.jsdelivr.net/gh/author/theme@main/addons/addon.css](https://cdn.jsdelivr.net/gh/author/theme@main/addons/addon.css) */
```

In your `vars` array:
```json
{
  "key": "varKey",
  "name": "Addon Name",
  "description": "What this addon does.",
  "type": "boolean",
  "default": "false"
}
```

List your addons and their corresponding var keys below:

---

**Checklist**

- [ ] CSS is hosted at a stable, public URL (jsDelivr CDN preferred)
- [ ] Theme works on Jellyfin 10.10 or 10.11
- [ ] Theme applies with a single CSS import
- [ ] Source repository is publicly accessible
- [ ] `version` field is set in the submission
- [ ] If vars are included: CSS uses `var(--lower-kebab-case, fallback)` or `{{lower-kebab-case}}` syntax
- [ ] If addons are included: `@sm-import-if` comments are present in the CSS and matching boolean vars are declared
