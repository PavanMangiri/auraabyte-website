# AuraaByte website — setup guide

## Files
| File | What it is |
|---|---|
| index.html | Homepage: hero, app catalogue, ads transparency, contact |
| app-ads.txt | **The file AdMob crawls.** Must stay at the site root |
| privacy-policy.html | One privacy policy for all apps (review before use) |
| terms.html | Terms of use |
| 404.html, robots.txt, sitemap.xml, favicon.svg, styles.css | Supporting files |
| CNAME | Only needed for GitHub Pages; contains your domain |

## 1. Before uploading — edit these
1. **app-ads.txt** — replace `pub-XXXXXXXXXXXXXXXX` with the line from AdMob (Apps > View all apps > app-ads.txt tab).
2. **Domain** — if you bought something other than `auraabyte.com`, find-and-replace `auraabyte.com` in every file.
3. **index.html** — the `APPS` list near the bottom. Check descriptions; add your other apps (copy a line, change name/id/cat/icon/desc).
4. **privacy-policy.html** — remove anything your apps don't do (e.g. Firebase, AI) and add anything they do.

## 2. Host on Cloudflare Pages (free, no Git needed)
1. dash.cloudflare.com > Workers & Pages > Create > Pages > **Upload assets**.
2. Project name `auraabyte`, drag this whole folder in, Deploy.
3. Custom domains > Set up a custom domain > `auraabyte.com` (and add `www.auraabyte.com`, redirecting to the root).
4. Check: `https://auraabyte.com/app-ads.txt` shows plain text.

To update later: Create new deployment > upload the folder again.

## 3. Point every app to the site (Play Console)
For **each** app: Grow users > Store presence > Store settings > Store listing contact details > Website → `https://auraabyte.com` (no `www`, no trailing path). Save.

## 4. Verify in AdMob
Wait at least 24 hours, then AdMob > Apps > app-ads.txt tab. Status should change to "Verified" per app.

## 5. Email (free)
Cloudflare > your domain > Email > Email Routing: forward `support@` and `ads@` to your Gmail.
