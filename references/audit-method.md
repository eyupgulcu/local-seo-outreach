# Mini audit method (free, public sources only)

Goal: a few verifiable observations per business, collected in minutes, with the method and date recorded so
the report can be defended. No paid API calls unless the user sets a cap.

## 1. Website (raw HTML is enough)

Fetch the home page with a mobile browser user agent (for example `curl -sL -A "<mobile UA>" <url>`). Record:

- http to https redirect works, or the site fails to open.
- Mobile viewport meta tag present or missing.
- Title and meta description: empty, brand-only, or missing the city and the trade word.
- Heading structure: an H1 that is meaningful, or something like "Blog".
- Tappable phone link (`tel:`), WhatsApp or contact form present.
- Footer year (an old year signals neglect).
- Structured data types present (LocalBusiness, Product, none).
- Menu links that lead to a theme demo, a parked page, or a 404.
- Product or catalog pages: exist or not.
- CMS and version if visible, only when the version is clearly outdated.

Do not run intrusive scans. Reading what any visitor can load is the limit.

## 2. Search presence

For each target city, run a web search for "<city> <trade>" and for "<business name> <city>". Record the
top results and whether the business appears. Be honest about the tool: a generic web search API may not
reproduce what a customer sees on a specific search engine in a specific country. Write the report line as
"in our own web search" and add that the engine's own ranking may differ.

## 3. Maps profile

Use rating and review count from the lead record or the public listing, and note the capture date. If the
field is empty, write "could not verify". Do not infer category or opening hours you did not see.

## 4. AI assistant visibility

Ask an assistant with web search: "recommend <trade> in <city>". Note which businesses it names. Say which
assistant you used. If you could not query a particular product, do not name it in the report. A single run
is a single sample: say that asking again may give different names.

## 5. Pick the biggest gap

Rank observations by how easily the owner will agree and how directly you can fix it. Choose one. Link it to
one offer. Keep the rest as "other small points" in two lines at most.

## 6. Record keeping

One row per business: id, city, site, date of audit, each observation with its method, the chosen gap, the
chosen offer. Keep the row with the report so a reply can be answered with evidence.

## Known limits to repeat in reports

- Search results come from our tool and may differ from the customer's.
- Review counts are from the capture date.
- AI answers vary per run.
- We observed public pages only; internal analytics were not available.
