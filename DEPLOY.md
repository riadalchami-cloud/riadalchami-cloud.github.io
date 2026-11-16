# Putting the publications site online

This folder is a complete static website. Google Scholar reads it best on a stable address it can crawl, so host it on one of these.

## Option A: GitHub Pages (free, about 10 minutes)
1. Create a free GitHub account (if you do not have one) (account: `riadalchami-cloud`).
2. Create a new public repository named exactly `riadalchami-cloud.github.io`.
3. Upload everything in this folder (keep the `papers` folder structure) and commit.
4. In the repository, open Settings, then Pages, and set Source to "Deploy from a branch", branch `main`, folder `/ (root)`.
5. After a minute the site is live at https://riadalchami-cloud.github.io

If you choose a different username or your own domain, the site has to be rebuilt with that address (all Scholar tags use full URLs). Ask Claude to rebuild it, or run `python3 build.py https://your-address` from the source files.

## Option B: AUE web space
Send this folder to AUE IT and ask them to publish it unchanged at a fixed address, for example https://www.aue.ae/faculty/riad-al-chami/. The site then needs a rebuild for that address.

## After it is live
1. Google Scholar profile: Edit profile, set Homepage to the site address.
2. ORCID: add the site under Websites and social links.
3. Google Search Console (search.google.com/search-console): add the site, then submit `sitemap.xml`.
4. Google Scholar usually picks up new pages within 2 to 8 weeks. The [PDF] link then appears next to the papers that have a hosted PDF.

## Copyright status of each paper
| Paper | Hosted file | Basis |
|---|---|---|
| EV purchase intention (Innovative Marketing 2026) | Published PDF | CC BY 4.0 |
| CSR in Lebanon (Administrative Sciences 2022) | Published PDF | CC BY 4.0 |
| Online Shopping (IJMCI 2018) | Published PDF | CC BY-NC 3.0 |
| Significance of Marketing in School (IJMCI 2018) | Published PDF | CC BY-NC 3.0 |
| Sustainability in Aviation (IGI Global 2025) | Published chapter PDF | IGI Global fair use policy: personal website allowed |
| From Talk to Trust (Springer 2025) | Author manuscript | Springer journals: accepted manuscript on personal website, no embargo |
| Immersive AR (Journal of Global Marketing 2026) | Not hosted | The file supplied is the Taylor & Francis published PDF (© Taylor & Francis), which cannot be posted. The accepted manuscript (your final Word version after peer review) can be posted on a personal website. |
| From Greenwashing to Greenbleaching (Emerald 2025) | Not hosted | The file supplied is the Emerald published PDF, which cannot be posted. The accepted manuscript can be posted now under CC BY-NC. |
| Organizational Culture and Leadership (Cambridge Scholars 2022) | Not hosted | Manuscript supplied (Chapter_6_Chami_edit2.docx). Cambridge Scholars has no public self-archiving policy; check your author agreement or ask the publisher before posting. |
| Challenging Patriarchy (Springer chapter 2025) | Not hosted yet | Springer edited volumes: accepted manuscript after 24 months (from early 2027). |
| Supply chain sustainability (BSE 2026) | Not hosted yet | Wiley: accepted version after a 12 to 24 month embargo; the original submitted version may be posted now. |
| UAE carbon footprint (PJMS 2023) | Links to publisher PDF | Already open access at the publisher. |

## Files
- `index.html`: profile and publication list, with schema.org Person and ItemList data
- `papers/<paper>/index.html`: one page per paper, with Google Scholar (Highwire) citation tags, Dublin Core, schema.org ScholarlyArticle data, abstract, keywords, plain-language summary, APA and BibTeX
- `papers/<paper>/*.bib`, `*.ris`: citation downloads for reference managers
- `sitemap.xml`, `robots.txt`: for search engines
- `llms.txt`: plain summary for AI search engines and assistants
- `_source/`: the generator (`build.py`, `papers.py`) to rebuild or add papers
