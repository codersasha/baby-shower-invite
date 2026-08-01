# Baby Shower Invitation

A single-page digital invitation with an envelope that bounces, opens on tap, and slides the letter out.

Everything lives in `index.html` — markup, styles and script, no build step and no dependencies beyond two Google Fonts.

## Personalising an invite

Add a `name` parameter to the URL and the guest is addressed on the envelope and greeted on the card:

| URL | Envelope reads | Card reads |
| --- | --- | --- |
| `?name=Jess` | Jess | Dear Jess, |
| `?name=Tab,Rob` | Tab & Rob | Dear Tab & Rob, |
| `?name=Tab,Rob,Sue` | Tab, Rob & Sue | Dear Tab, Rob & Sue, |

Without the parameter the invitation shows with no name. Names are inserted as text, so punctuation in a name can't break the page. Up to five names are used, 24 characters each.

## Previewing locally

```bash
python3 -m http.server 8765
```

Then open http://localhost:8765/?name=Jess

## Deploying

Pushing to `main` publishes the site to GitHub Pages via `.github/workflows/deploy.yml`.
