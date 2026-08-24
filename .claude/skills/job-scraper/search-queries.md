# Search Queries for Job Scraper

<!-- SETUP: Customize these queries based on your skills, target roles, and location -->

## Installed portal CLIs (primary for `/scrape`)

`/scrape` discovers every portal skill under `.agents/skills/*/SKILL.md` and runs its CLI first. Shipped country-agnostic CLIs include `linkedin-search` and `freehire-search`; Danish demos and any skill you add with `/add-portal` are included the same way. You do **not** need a matching `site:` line below for those CLIs to run.

The `site:` query templates in this file are the **WebSearch fallback** — for portals without a CLI, company career pages, or when a CLI fails.

**Language scope:** write every query category in every language listed in your CLAUDE.md Languages table (typically 1-2, sometimes more). A posting requiring a language you have *not* declared, as a job condition, is excluded before scoring; a posting requiring a *higher level* than you declared in a language you *do* work in is flagged for your own judgment, not excluded — see `04-job-evaluation.md`'s Language Gate, the single source of truth for this rule. Translate each category's keywords rather than machine-translating word-for-word (e.g. "Frontend Developer" -> "Desarrollador Frontend", not a literal word-for-word translation) if you work in more than one language.

## Search Sites

Primary (US market job boards):
- **indeed.com** - largest general US job board
- **linkedin.com/jobs** - LinkedIn job listings (filter: United States / New York City); also covered by `linkedin-search` CLI
- **builtin.com** - product/startup-focused board (matches preference for product companies and startups)
- **wellfound.com** - startup-focused board (optional)

Danish portal demos (Jobindex, Jobbank, Jobdanmark, Jobnet) ship disabled and are not relevant to this US-based search - left off.

Secondary (company career pages via Google):
- Direct Google searches with `site:` filters for known target companies

## Query Categories

Queries are grouped by priority. Write **each category in every language from your Languages table** (see Language scope above). Combine each query with your location terms (e.g. your city, region, or metro area) where the site supports it.

**Organize by function, not job title.** The same underlying work carries different titles across companies and markets (a "Data Scientist" role at one employer may be posted as "Insights Analyst" or "Data Consultant" at another). Name each priority category after the function it covers, and list several plausible job titles as query variants within that category rather than betting an entire priority tier on one exact title string.

### Priority 1: Software Engineering

Core backend/software engineering roles - direct match to current and past job titles.

```
site:indeed.com "Software Engineer" New York
site:indeed.com "Backend Engineer" New York
site:indeed.com "Software Engineer II" New York
site:linkedin.com/jobs "Software Engineer" United States
```

### Priority 2: AI / Agentic Engineering

Roles building or applying LLM-powered agents - matches the Claude API/MCP project portfolio.

```
site:indeed.com "AI Engineer" New York OR Remote
site:indeed.com "Machine Learning Engineer" agentic OR LLM New York OR Remote
site:indeed.com "Applied AI Engineer" New York OR Remote
site:linkedin.com/jobs "AI Engineer" United States
```

### Priority 3: Data Engineering

Roles matching the ETL/CDC/cloud data platform background at JPMorgan and State Street.

```
site:indeed.com "Data Engineer" New York OR Remote
site:indeed.com "Data Platform Engineer" AWS OR Snowflake New York
site:linkedin.com/jobs "Data Engineer" United States
```

### Priority 4: Broader / Adjacent

Wider net for adjacent titles worth including given the ownership/client-facing project portfolio.

```
site:indeed.com "Forward Deployed Engineer" United States
site:indeed.com "Full-Stack Engineer" New York OR Remote
site:builtin.com "Software Engineer" OR "AI Engineer" OR "Data Engineer"
site:wellfound.com "Software Engineer" OR "AI Engineer"
```

## Location Filter

No hard location constraint - open to relocation, remote, or hybrid. Treat all of the following as acceptable:
- New York City and surrounding areas (ideal - current base, no relocation needed)
- Remote (US) (ideal)
- Any other US metro area (acceptable - open to relocation)

No location should be excluded on distance/commute grounds; location is not a Pass/Fail filter for this candidate.

## Language Filter

Your working languages and levels are in CLAUDE.md's Languages table. When filtering scraped results, apply `04-job-evaluation.md`'s Language Gate: a posting requiring a language you haven't declared at all is excluded; a posting requiring a higher level than you declared in a language you do work in is not excluded, flag it clearly instead (see `job-scraper/SKILL.md`'s Step 3 "Quick Fit Assessment" for how the flag surfaces in `/scrape` output). Postings simply *written* in a language you don't work in, that don't require it on the job, are fine.

## Date Filter

Only include jobs posted within the last 2 days, or with an application deadline that has not yet passed. If a posting date cannot be determined, include it but flag as "date unknown".

## Adapting Queries

If the user specifies a focus area, select queries from the matching category and also generate 2-3 custom queries for that focus. For example:
- "/scrape [focus_area]" -> relevant category queries + custom focus-specific queries
