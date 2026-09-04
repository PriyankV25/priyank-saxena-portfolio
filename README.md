# Priyank Saxena — Portfolio Website

A responsive static portfolio built with vanilla HTML, CSS and JavaScript.

## Run locally
Because the certificate gallery loads `certificates.json`, serve the `site` folder with a local HTTP server instead of opening `index.html` directly.

Example:
`python -m http.server 8000`
Then open `http://localhost:8000`.

If port 8000 is busy, use another port, for example `python -m http.server 3000`.

## Contact form — FormSubmit
The contact form sends messages directly to `priyank.saxena.dev@gmail.com` through FormSubmit. No database, PHP, Node.js or custom backend is required.

### Activate the form
1. Deploy the `site` folder to your final hosting provider (GitHub Pages, Netlify, Vercel, Cloudflare Pages, etc.).
2. Open the deployed portfolio and submit the contact form once using a test/visitor email address.
3. FormSubmit will send an activation/confirmation email to `priyank.saxena.dev@gmail.com` the first time the form is used.
4. Open that email and click the activation/confirmation link.
5. After activation, future form submissions will be forwarded to your inbox.

FormSubmit says no registration is required; the first submission triggers the confirmation email. See: https://formsubmit.co/documentation

### Thank-you page
The form automatically sets `_next` to `thank-you.html` based on the current website URL. This means you do **not** need to hard-code your future domain into the HTML.

After a successful submission, the visitor is sent to:
`https://your-deployed-domain.example/thank-you.html`

The supplied `thank-you.html` uses the same dark glassmorphic/automation theme as the main portfolio.

### Important
The form is currently configured with `_captcha=false` to keep the visitor flow simple. FormSubmit recommends keeping reCAPTCHA enabled for stronger spam protection. If spam becomes a problem, remove the `_captcha` hidden field and FormSubmit's default CAPTCHA protection will apply.

## Deploy
The entire `site` folder can be deployed to GitHub Pages, Netlify, Vercel, Cloudflare Pages, or another static hosting provider.

## Contents
- `index.html` — complete portfolio UI and interactions
- `thank-you.html` — post-submission page in the same theme
- `certificates.json` — metadata for all supplied certificates
- `assets/certificates/` — original certificate files
- `assets/certificate-thumbs/` — generated first-page/gallery previews
- `assets/career/` — supplied professional/career images
- `resume.pdf` — supplied resume
