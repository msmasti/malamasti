# NUM by Mala Masti — Website

Strategic advisory practice for early-stage VLSI and chip startups using AI to redesign hardware processes.

## Site structure

```
index.html          ← Main website
CNAME               ← Custom domain config (malamasti.com)
docs/               ← Resume PDF goes here
assets/             ← Any images/icons go here
README.md           ← This file
```

## Hosting on GitHub Pages

1. Create a new GitHub repository named `malamasti.com` (or `num-site`)
2. Upload all files from this zip
3. Go to **Settings → Pages**
4. Set source to **main branch / root folder**
5. GitHub will auto-deploy to `https://msmasti.github.io/<repo>` within ~2 minutes

## Custom domain setup (malamasti.com)

After GitHub Pages is live, configure your domain registrar DNS:

| Type  | Name | Value                  |
|-------|------|------------------------|
| A     | @    | 185.199.108.153        |
| A     | @    | 185.199.109.153        |
| A     | @    | 185.199.110.153        |
| A     | @    | 185.199.111.153        |
| CNAME | www  | msmasti.github.io      |

Then in GitHub → Settings → Pages → Custom domain → enter `malamasti.com`

## Email on malamasti.com

Recommended: **Zoho Mail free plan** (https://zoho.com/mail)
- Supports custom domain email on free tier (1 user)
- Set up: num@malamasti.com
- Add the MX records Zoho gives you to your domain registrar DNS

Alternative: **Google Workspace** ($6/mo) for Gmail with your domain.

## Resume PDF

Place your resume PDF as: `docs/mala-masti-advisor-resume.pdf`
The About section links to it automatically.

## Adding your photo

Replace the initials "MM" placeholder in the About section:
In `index.html`, find `about-portrait` and replace the div with:
```html
<img src="assets/mala-masti.jpg" alt="Mala Masti" style="width:100%;border-radius:12px;object-fit:cover;" />
```

## Domain registrar recommendation

- **Namecheap** (namecheap.com) — affordable, clean UI
- **Cloudflare Registrar** (cloudflare.com/products/registrar) — at-cost pricing

Search for: `malamasti.com`

## msmasti.com redirect (optional but recommended)

Register `msmasti.com` as well (~$10/yr) and add a simple redirect so anyone who types your GitHub username as a domain lands on your site.

In Cloudflare → malamasti.com → Page Rules → add:
- URL: `msmasti.com/*`
- Setting: Forwarding URL (301) → `https://malamasti.com/$1`

This way github.com/msmasti and msmasti.com both point people to the right place.
