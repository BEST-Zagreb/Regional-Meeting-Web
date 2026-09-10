# Regional Meeting

Static archive of the website that ran at **best.hr/rm** until 2026-09-10, when the WordPress server
behind it was retired. Every page here is plain HTML. There is no database, no PHP and nothing to
keep patched.

Intended home: **rm.best.hr**

- 2 published pages, 62 files, 3.6 MB
- Verified: every page and asset requested over HTTP, 51 URLs, **0 failures**
- Verified: every page rendered in a browser, **0 broken images**

## Looking at it locally

    python3 -m http.server 8000

Then open <http://127.0.0.1:8000/>. Any static file server works, and so does dragging the folder
into Cloudflare Pages or Netlify.

## How it was made

Mirrored with `wget`, then checked against the site's own database rather than by clicking around,
because a crawler only finds pages that something links to. The full method, the tooling and the
verification results live in the migration notes alongside this archive.

## What deliberately differs from the original

This is a faithful copy with three exceptions, all of them deliberate.

### Links were made relative

Every reference to `best.hr` that pointed at a file in this archive was rewritten to a relative
path, so the site is self-contained and does not call a server that no longer exists. Links to
genuinely external sites are untouched.

### Personal contact details were replaced

Named personal email addresses and mobile phone numbers were replaced with the organisation's role
address, **board@best.hr**. This archive is public and outlives the students named in it. People's names
stay, as credit; their private contact details do not.

### Links that led nowhere were repaired or removed

Some links were already broken on the live site. Where the target still existed under a different
address it was repointed; where it existed nowhere the link was removed and the surrounding
content left in place.

## Licence

The content, images and copy belong to BEST Zagreb. Third-party theme and plugin assets under
`wp-content/` remain under their own licences and are included only because the pages need them to
render as they originally did.
