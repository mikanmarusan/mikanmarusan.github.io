## Public Repository Hygiene

This repository is **public**. Anything committed is world-readable and may be
indexed by search engines.

Do NOT commit:
- Secrets: `.env*`, API keys, tokens, OAuth client secrets, private keys.
- Personal contact info: email, phone, postal address. Public handles only
  (`github.com/mikanmarusan`, `twitter.com/mikanmarusan`).
- Local absolute paths: `/Users/...`, `/home/...`, machine names.

**Why:** The site does not currently expose private contact info — adding it via
committed Markdown would create a new, search-engine-indexable disclosure.

**How to apply:**
- Stage explicit files. Do NOT use `git add -A` or `git add .`.
- Before committing, scan the staged diff for the patterns above.
- This rule applies equally to commit messages, PR titles/bodies, and issue
  text.
