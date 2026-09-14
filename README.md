# Starpilot Docs

Documentation for the StarPilot fork of FrogPilot

## Local Development

Preview the docs website locally using:

1. Run `docker compose up --build`
2. Navigate to http://localhost:8000
3. When finished, `Ctrl+C` the docker command to stop the server.

## Search visibility

Every standalone guide should have a unique `title` and `description` in its Markdown
front matter. Describe the actual page content and keep device and vehicle claims in
sync with the project. Material uses these fields for search metadata and social cards.
The homepage also supplies `WebSite` structured data identifying StarPilot Docs.

MkDocs generates `sitemap.xml` using `site_url`; `docs/robots.txt` advertises that sitemap.
Reusable files under `docs/hardware/embed/` are included in guides but excluded from
standalone output. Keep existing guide URLs stable when updating titles or navigation.

After deploying:

1. Verify the site in [Google Search Console](https://search.google.com/search-console)
   with an account that controls `wiki.firestar.link`.
2. Submit `https://wiki.firestar.link/sitemap.xml` and inspect the homepage,
   installation guide, and vehicle compatibility page. Request indexing for updated pages.
3. Track impressions, clicks, and indexed pages for StarPilot, StarPilot install,
   StarPilot comma 3/3X/4, Galaxy StarPilot, and vehicle-specific searches.
4. Keep links from the project GitHub README and official community pages pointing
   to this wiki and the relevant guides. Publish feature changes here alongside announcements
   so the documentation remains useful outside Discord.

Google chooses search titles and rankings; these changes do not guarantee a position.
See Google's guidance on [page titles](https://developers.google.com/search/docs/appearance/title-link),
[site names](https://developers.google.com/search/docs/appearance/site-names), and
[sitemaps](https://developers.google.com/search/docs/crawling-indexing/sitemaps/build-sitemap).
