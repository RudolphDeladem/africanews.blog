# africanews.blog

Plain static site (no build step). Live at https://africanews.blog, hosted on Netlify
(site name `africanews-blog`); the domain's DNS is at Hostinger and points to Netlify.

## Daily article workflow

The owner gives a topic; write the article and publish it without asking again.

1. Research the topic. Use only facts you can source; say in the article what is not
   known. End with a note naming the sources and the date.
2. Create `<slug>/index.html` by copying the structure of an existing article (meta tags,
   JSON-LD, masthead, facts box, footer). Add a 1200x630 image in `assets/images/`.
3. Home page (`index.html`): make the new article the lead story and move the previous
   lead to the top of "More stories" (`.story` blocks).
4. Add the URL to `sitemap.xml`.
5. Check both pages in a browser at desktop and phone widths.
6. Commit and push, then deploy: zip the site files (`git archive` of `index.html`,
   `robots.txt`, `sitemap.xml`, `assets` and every article folder) and POST the zip to
   the Netlify API `sites/<site id>/deploys`. Verify the new URL on the live domain.

Style: plain English, short sentences, British spelling, no hype. Byline is
"the africanews.blog tech desk".
