# ppm-registry

The official prefix registry for the [Pear-VBA](https://github.com/Pear-VBA) package ecosystem.

Every package published in the Pear-VBA ecosystem must register a unique prefix here before publishing. The prefix guarantees that all public symbols in your package will not collide with symbols from any other package.

→ Full convention specification: [Pear-VBA/ppm](https://github.com/Pear-VBA/ppm)

---

## Register your prefix

1. Fork this repository
2. Add one line to `prefixes.json`:
   ```json
   "ABC": "your-github/your-repo"
   ```
3. Open a Pull Request with the title: `Register prefix ABC for your-github/your-repo`

Your PR will be reviewed and merged within 48 hours if it passes all checks below.

---

## Acceptance criteria

- Prefix is 2–4 Latin letters only, no digits or special characters
- Prefix does not conflict with any existing entry (case-insensitive)
- Prefix is not on the [reserved list](https://github.com/Pear-VBA/ppm/blob/main/SPEC.md#12-reserved-prefixes)
- The referenced repository is public and exists on GitHub
- The referenced repository contains a `package.bas` with a matching `prefix` field

---

## prefixes.json format

```json
{
  "EHC": "Pear-VBA/vba-http",
  "JSN": "Pear-VBA/vba-json"
}
```

One prefix per package. Keys are case-insensitive — `EHC` and `ehc` are treated as the same prefix.
