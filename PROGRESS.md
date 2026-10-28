# PROGRESS.md

## Status
- Phase 1, Day 1 (27 Oct 2026): DONE. Python 3.14.6, venv, JupyterLab and pandas installed, first notebook runs, repo pushed to GitHub (dr-nath/nap-community-text-mining)
- Day 2 (28 Oct): Python basics on small text examples. Not started.
- Day 3 (29 Oct): pandas, reading files, document table. Not started.

## Decisions
- North = Annex I, South = non-Annex I (a proxy, with known limits: 1992 classification, economies in transition in Annex I, some wealthy non-Annex I countries)
- Corpus is now "national adaptation plans and strategies", not only NAPs from NAP Central. Reason: Annex I countries probably do not submit NAPs there (found in UNFCCC materials and a forum thread; still to verify on the site)
- Hybrid sourcing: NAP Central for non-Annex I, national government sites for Annex I
- Comparison mixes country group and document type. The README must say so. The document table needs a document_type column
- Plan for 12 working days, finishing by 7 Nov (deadline 8 Nov)
- Commits use GitHub's private noreply email. Git via GitHub Desktop
- data/raw/ is not uploaded until terms of use are checked. COMMANDS.md is git-ignored (personal reference)

## Rules to write before downloading (draft)
- Inclusion: national-level, government-adopted adaptation document, official English version, most recent, not sector-specific
- Selection: if more qualify than I can use, choose by a reproducible rule (random with fixed seed)
- Sample: about 8-10 per group, smaller if needed, stated honestly
- Record per document: country, group, year, document type, source URL, date downloaded, terms-of-use note

## Open questions
- Does a "Developed Country Strategies and Plans" page exist on NAP Central, and how many countries?
- NAP Central terms of use (copy the wording)
- Number of English-language NAPs for developing countries
- Python 3.14: check that scikit-learn / spaCy / gensim install

## Lessons
- Notebooks must be created inside notebooks/ (open the folder in Jupyter first)
- Stop Jupyter with Control+C, not Cmd+C
- Publish repository in GitHub Desktop fails if the repo already exists: use Push origin

## Next step
- Day 2: start Jupyter, then Python basics

## Update 28 Oct (verified on napcentral.org)
- Developing-country list: 81 NAPs (last update 7 Oct 2026). Developed-country list: 12 plans (last update 5 Nov 2025): AUS, AUT, CAN, FIN, FRA, DEU, IRL, NZL, NLD, ESP, GBR, USA
- Hybrid sourcing DROPPED. Both groups come from NAP Central. Earlier worry (no Annex I NAPs) was wrong
- To verify: all 12 are Annex I (and Annex II?) against the UNFCCC Parties list
- Plan: 12 North vs 12 South, South sampled at random (fixed seed) from English-language national non-sectoral NAPs
- Limitations: English-only bias, developed-country plans "shared" not "submitted", page possibly out of date, document types differ (e.g. USA "strategy")
- Terms of use: still to read and copy
