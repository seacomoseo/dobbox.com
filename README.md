# dobbox.com

[![dobbox.com](/assets/media/logo.png)](https://dobbox.com/)


## STEPS


### Local
- Design
  - GENERAL
    - `config.yml`
    - `data/*.{yml,md}`
  - FONTS
    - Fonts that not be in Google Fonts:
      - .otf/.ttf files in `assets/fonts` + rename
      - You need the `sansoul_tools` project in `../_tools` folder
      - Run `do fonts` comand
      - `Family` + `Style` + `Weight` must match in `config.yml ⏩ params.fonts` + `_fonts.scss` (and disable `params.fonts.google` if appropriate)
  - REDIRECTS
    - `assets/redirects.md`


### After client validate web


#### Domain

- If Netlify
  - [`Domain Management / settings`](https://app.netlify.com/sites/dobboxfrio/settings/domain)
  - `Add custom domain`
  - `Check DNS configuration` Copy
  - Add `DNS Records` copied from Netlify to Domain gestor:
    - From: `dobbox.com`
      DNS Record: `ALIAS`, `ANAME` or `flattened CNAME`
      To: `apex-loadbalancer.netlify.com`
    - From: `dobbox.com`
      DNS Record: `A`
      To: `75.2.60.5`
    - From: `www`
      DNS Record: `CNAME`
      To: `dobboxfrio.netlify.app.`
    - Maybe you need to eliminate the previous records with similar names
  - `Verify DNS configuration`
  - If it does not work after a while, try `Set as main domain` in the `www` version and also in te `nowww` version


#### [Google Search Console](https://search.google.com/search-console)

- Add property
- Verify versions ⏩ `data/config.yml`
  - `google_analytics`
  - `google_site_verification`
  - `google_file_verification`
  - DNS:
    From: `@`
    DNS Record: `TXT`
    To: `google-site-verification=[google_site_verification]`
- Link with Analytics
- Add sitemap.xml


#### [Google My Business](https://business.google.com/)

- `Add company ⏩ ...` ⏩ whait 13 days to receive postal and insert code to verify


##### Delivery

Send to all collaborators next:

```
*ENTREGA WEB dobbox.com:* https://seacomoseo.com/entrega/
```
