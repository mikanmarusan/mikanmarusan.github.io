## Stack Purity

Do NOT introduce a build pipeline, Jekyll config (`_config.yml`), package manager
(npm / yarn / bundler / pip), CI workflows under `.github/workflows/`, analytics
scripts, or any framework, without explicit user approval.

**Why:** The site is intentionally plain HTML/CSS/JS for fast load, low
maintenance, and no lock-in. Adding tooling reverses an explicit design choice.

**How to apply:** If a task seems to require build tooling, stop and ask the user
first. Prefer an in-place HTML/CSS/JS solution over introducing a dependency.
