# Between the Lines

A single-file web app (`index.html`, no build step, no dependencies). Users upload a WhatsApp
export (.zip or .txt), pick a chat type and get a report. Chats are analysed in the browser.

## Emailing uploaded chats (consent-based)
In `index.html`, `MAIL_ENDPOINT` points to a Formspree form. After a user ticks the consent box
and clicks Continue, the chat text is POSTed to that form (the free plan does not allow file
uploads, so text is sent, capped at ~150,000 characters). To use your own form, replace the
endpoint. Restrict the form to your domain in the Formspree settings.

## Run locally
Open `index.html` in a browser, or run `python3 -m http.server` in this folder.

## Host for free
- Netlify Drop: drag this folder to https://app.netlify.com/drop
- Cloudflare Pages: upload the folder (Pages > Create > Direct Upload)
- GitHub Pages: push to a repo, then Settings > Pages > deploy from the main branch
