# Data Card

`UniLex_Questions.csv` has 320 questions for 16 concepts, 20 per concept: 15 AI-assisted (written with Claude, checked by the team) and 5 real Stack Exchange titles.

Columns: id, query, concept, unilex_term, source, source_url, license_or_credit, date_added, reviewed_by, review_status. Only rows marked `approved` are used.

`member_examples.csv` has 8 questions (2 per member). They are tested separately and are not in train, dev or test.

Stack Exchange titles were collected through the public API. They are CC BY-SA, so each row keeps its link, author and date. Three Stack Overflow rows have no licence version, so they just say "CC BY-SA".

Cleaning: we checked empty questions, duplicate ids and questions, and conflicting labels. All 320 stayed.

Split (seed 42): test = last 3 Stack Exchange questions per concept (48), dev = 3 random per concept (48), train = the rest (223, after leaving out SE026, which was too similar to a test question).

Limits: Stack Exchange authors are not confirmed students, some titles don't name the concept, the AI-assisted questions may sound too similar, and the test set is small.
