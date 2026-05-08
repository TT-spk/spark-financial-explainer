[README.md](https://github.com/user-attachments/files/27542322/README.md)
# Spark Financial Statements Explainer — Vercel Package

This folder is ready to upload to Vercel as a static project.

## File structure

```text
spark-financial-explainer-vercel/
├── index.html
├── css/
│   └── styles.css
├── js/
│   └── app.js
└── assets/
    └── README-assets.txt
```

## What to upload to Vercel

Upload the whole `spark-financial-explainer-vercel` folder, not just `index.html`.

## Circle iframe embed code

After Vercel gives you a live URL, paste this into the Circle lesson embed/custom HTML block:

```html
<iframe
  src="https://YOUR-VERCEL-PROJECT.vercel.app"
  width="100%"
  height="800px"
  frameborder="0"
  style="border-radius:12px;"
></iframe>
```

Replace `https://YOUR-VERCEL-PROJECT.vercel.app` with your actual Vercel URL.

## Engineering note — Anthropic API before production

The current packaged version is a static sandbox module. The uploaded code referenced clickable tech-stack cards, but did not include the full AI tutor/API implementation.

Before production launch, engineering should:

- Confirm whether the final module needs Claude/Anthropic AI tutor functionality.
- Keep Anthropic API requests server-side, not inside browser JavaScript.
- Store the API key as a secure environment variable, for example `ANTHROPIC_API_KEY`.
- Create a secure API route/proxy such as `/api/chat`.
- Add usage limits, monitoring, and abuse prevention.
- Remove any client-side exposed API keys before public release.
- Perform a security review before live learner/customer access.

Current package is intended for internal Circle/Vercel sandbox testing only.
