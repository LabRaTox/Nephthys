# Contributing Translations

Thank you for helping translate Nephthys!

## How to add a new language

1. **Fork** this repository and create a new branch (e.g. `translation/es`)
2. Copy `locales/en/translation.json` to `locales/xx/translation.json`
   — replace `xx` with the [ISO 639-1](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) language code (e.g. `es`, `pl`, `nl`)
3. Translate all string values (right side of the `:`)
4. Validate your file — run this in the project root:
   ```
   node -e "require('./locales/xx/translation.json'); console.log('OK')"
   ```
5. Open a **Pull Request** with the title `translation: add xx (Language Name)`

---

## Rules

### Do NOT translate
| What | Example |
|------|---------|
| Placeholders | `{{user}}`, `{{count}}`, `{{guild}}` |
| HTML tags | `<code>`, `<strong>`, `<a href="...">` |
| Platform names | Discord, Twitch, YouTube, Kick, Trovo, Ko-Fi, Patreon, Steam, EVE Online, X (Twitter), Spotify |
| Technical terms | OAuth2, Webhook, API, XP, DJ |
| Bot command names | `/reminder`, `/giveaway`, `/voice-lock` |
| Emoji | 🎉 ✅ ❌ — keep them as-is |

### Do translate
- All descriptive text, labels, button names, hints, error messages
- Section titles and headings
- Placeholder text inside input fields (e.g. `"e.g. Slash Commands"`)

### Tone
- **Dashboard / UI:** formal (`vous` in French, `Sie` in German)
- **Bot responses in chat:** informal, friendly (standard in gaming communities)

---

## JSON format rules

- Keep the exact same key structure as `en/translation.json`
- Do not add or remove keys
- Arrays (`[...]`) must keep the same number of elements
- Escape double quotes inside strings: `\"` or use single-quoted alternatives
- Valid JSON only — no trailing commas

**Quick validation:**
```bash
node -e "require('./locales/xx/translation.json'); console.log('OK')"
```

---

## Currently supported languages

| Code | Language | File |
|------|----------|------|
| `de` | Deutsch | `locales/de/translation.json` |
| `en` | English | `locales/en/translation.json` |
| `fr` | Français | `locales/fr/translation.json` |

---

## Questions?

Open an [Issue](../../issues) and tag it with `translation`.
