# Moto Kuni Charcoal Briquettes – website

A simple static website (no database, no coding tools needed). It works on GitHub Pages for free.

## Put it online (step by step)

1. Sign in at github.com and click **New repository**. Name it e.g. `briquettes-site`, set it to **Public**, click **Create repository**.
2. On the new repository page click **uploading an existing file**.
3. Unzip this folder on your computer, then drag **everything inside it** (index.html, style.css, the images folder, CNAME if present) into the page. Click **Commit changes**.
4. Go to **Settings → Pages**. Under *Build and deployment*, set Source to **Deploy from a branch**, branch **main**, folder **/ (root)**, and click **Save**.
5. After 1–2 minutes GitHub shows your live address (https://YOUR-USERNAME.github.io/briquettes-site/). Open it to check.

## Connect charcoalbriquettes.co.ke (DNS is on Cloudflare)

The `CNAME` file in this folder already contains your domain. Then:

1. In GitHub: **Settings -> Pages -> Custom domain**, enter `charcoalbriquettes.co.ke`, Save.
2. In Cloudflare: open the domain -> **DNS -> Records** and add (set Proxy status to **DNS only**, grey cloud):
   - Four **A** records, Name `@`, pointing to `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - One **CNAME**, Name `www`, Target `YOUR-GITHUB-USERNAME.github.io`
3. Wait a few minutes to a few hours, then tick **Enforce HTTPS** in GitHub Pages settings.

## Things to fill in (search index.html for `[`)

- Pack sizes and the minimum bulk order
- Delivery areas and payment methods in the FAQ
- Real product photos (replace the dashed "Photo" boxes with `<img src="images/yourphoto.jpg" alt="...">`)

## Changing a phone number

The WhatsApp number is in the links that start with `https://wa.me/254780708415`. Change the digits (country code first, no + or spaces).
