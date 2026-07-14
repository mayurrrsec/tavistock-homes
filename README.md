# Tavistock Homes — Website

A fast, self-contained **static website** — a warm, editorial, photography-led design that keeps the
brochure's brand DNA but has its own layout and voice. One responsive page (Welcome · Step inside ·
Our approach · Care & team · Education · Safeguarding · Referrals · Contact), plus a matching 404 page.

- **No build step, no database, no framework.** Just HTML + CSS + your images and fonts.
- **Fully portable** — open `index.html` to preview offline, or drop the whole folder onto any host
  (Cloudflare Pages, GitHub Pages, Netlify, or your GetDotted/Freeola web space). Deploys the same
  everywhere, so we're never locked to one host.
- **Photography-led** — a split editorial hero, a "You belong here" manifesto band (the real words
  from the kitchen wall), and a room-by-room photo tour (living spaces · kitchen · bedrooms · garden).
- **Brand DNA of the brochure** — navy/gold/sage/cream palette, Fraunces + Inter (local fonts),
  the vector emblem, and its Ofsted registration status.

## Folder contents
```
website/
├─ index.html        ← the site (all copy & layout)
├─ 404.html          ← friendly "page not found"
├─ css/style.css     ← all styling (responsive; mobile menu built in)
├─ fonts/            ← Fraunces + Inter (local, OFL)
└─ assets/
   ├─ photos/        ← optimised site photography (16 images)
   └─ brand/         ← logo source files
```

## Preview locally
Double-click `index.html` — it opens in your browser with everything working (no internet needed).

---

## Hosting — recommended: **Cloudflare Pages** (free)

We're hosting it now to gather feedback, in a way that later moves onto `tavistockhomes.com`
without a rebuild. **Cloudflare Pages** is the pick because:

- **Drag-and-drop deploy** — no coding/Git needed. You get an instant shareable link like
  `tavistock-homes.pages.dev`.
- **Free**, fast worldwide, automatic HTTPS.
- **Easy to connect your domain later** — when `tavistockhomes.com` is ready, add it as a custom
  domain in one screen. Your free `@tavistockhomes.com` **email keeps working** (we only touch the
  website record, not mail).

### Deploy steps (Cloudflare Pages — drag & drop)
1. Create a free account at **dash.cloudflare.com**.
2. Left menu → **Workers & Pages** → **Create** → **Pages** → **Upload assets**.
3. Name it `tavistock-homes`, then **drag the whole `website` folder in** (or a .zip of it).
4. Click **Deploy**. In ~30 seconds you'll get a live `…pages.dev` link to share for feedback.
5. **Later**, to go live on your domain: Pages project → **Custom domains** → add
   `www.tavistockhomes.com` (and `tavistockhomes.com`) → follow the DNS prompt.

### Alternative: **GitHub Pages** (also free)
Good if you'd rather keep it in a GitHub repo. Slightly more setup (needs a repo; custom-domain
HTTPS takes a little longer to activate):
1. Create a GitHub account + a new repository (e.g. `tavistock-homes`).
2. Upload the **contents** of the `website` folder to the repo (so `index.html` is at the root).
3. Repo → **Settings → Pages** → Source: `main` branch, `/root` → **Save**.
4. You'll get `https://<username>.github.io/tavistock-homes/`.
5. Later: **Settings → Pages → Custom domain** → enter `www.tavistockhomes.com`, and add a
   `CNAME` file + DNS record.

> Either host works with the exact same files. We can start on Cloudflare Pages for feedback and
> switch to your domain whenever it's ready — nothing needs rebuilding.

## When the domain is connected
- Replace the brochure's `[website — to follow]` placeholder with the real URL (page 11 + back cover),
  then `python build.py` in the `brochure/` folder to refresh the PDFs.

## Still to add when available
- A real quote/testimonial (Contact or Inside section).
- Official Ofsted "Registered" logo image (currently the styled badge).
- A Google Map embed / directions block, if wanted.
