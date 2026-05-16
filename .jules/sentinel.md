## 2025-05-22 - [Dependency Security] Transitive Vulnerability Fix
**Vulnerability:** Critical command injection in `shell-quote@1.7.2` (GHSA-33f9-j839-rf8h).
**Learning:** Legacy projects often carry deep transitive vulnerabilities in build tools (e.g., `react-dev-utils` -> `shell-quote`).
**Prevention:** Use `resolutions` in `package.json` to force-update transitive dependencies without breaking the parent package's peer dependency requirements. Always verify package versions against the registry before applying resolutions.
