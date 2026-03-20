# Skin Manager — Theme Repository

This repository hosts the community theme list for the [Skin Manager](https://github.com/Jellyfin-PG/Skin-Manager) Jellyfin plugin. The `skins.json` file is fetched live by the plugin, so approved themes appear in the store without requiring a plugin update.

---

## Submitting a Theme

Themes are added through GitHub issues. Open a new issue and select the **Theme Submission** template. Fill in all required fields and a maintainer will review it.

**Before submitting, make sure your theme meets these requirements:**

- The CSS is hosted at a stable, publicly accessible URL (jsDelivr CDN or GitHub raw are preferred)
- The theme works with a single `@import` or stylesheet link — no additional files required
- It has been tested on Jellyfin 10.10 or 10.11
- The source is publicly available (GitHub repository or equivalent)

Themes that are abandoned, broken, or require files beyond a single CSS import will not be accepted.

---

## Theme Format

Each entry in `skins.json` uses the following structure:

```json
{
  "name": "ThemeName",
  "author": "AuthorHandle",
  "description": "One or two sentences describing the theme.",
  "version": "1.0.0",
  "jellyfin": "10.11+",
  "tags": ["dark", "minimal"],
  "previewUrl": "https://example.com/preview.png",
  "screenshots": [],
  "sourceUrl": "https://github.com/author/theme",
  "cssUrl": "https://cdn.jsdelivr.net/gh/author/theme@main/theme.css",
  "cssImport": "@import url(\"https://cdn.jsdelivr.net/gh/author/theme@main/theme.css\");"
}
```

**Available tags:** `dark` `light` `minimal` `modern` `colorful` `backdrops` `mobile-friendly` `tv` `icons` `animations` `developer`

---

## License

The contents of this repository are licensed under [MIT](LICENSE). Individual themes remain the property of their respective authors under their own licenses.