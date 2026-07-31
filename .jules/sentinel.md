## 2025-05-14 - Fix Critical Command Injection in shell-quote
**Vulnerability:** `shell-quote` versions <= 1.7.2 were vulnerable to command injection because `quote()` did not escape newlines in object values (GHSA-33f9-j839-rf8h).
**Learning:** Transitive dependencies can introduce critical vulnerabilities even if the project itself doesn't use the library directly. Docusaurus v2 beta versions pull in many outdated dependencies.
**Prevention:** Regularly run `yarn audit` and use the `resolutions` field in `package.json` to force-patch transitive vulnerabilities that aren't being updated by the parent package.
