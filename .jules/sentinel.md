## 2025-05-14 - Fix Critical Command Injection in shell-quote
**Vulnerability:** `shell-quote` versions <= 1.7.2 were vulnerable to command injection because `quote()` did not escape newlines in object values (GHSA-33f9-j839-rf8h).
**Learning:** Transitive dependencies can introduce critical vulnerabilities even if the project itself doesn't use the library directly. Docusaurus v2 beta versions pull in many outdated dependencies.
**Prevention:** Regularly run `yarn audit` and use the `resolutions` field in `package.json` to force-patch transitive vulnerabilities that aren't being updated by the parent package.

## 2026-04-16 - Dependency Vulnerabilities: axios SSRF and form-data Unsafe Random Boundary
**Vulnerability:** Critical vulnerabilities in nested dependencies: `axios` (SSRF due to hostname normalization bypass) and `form-data` (Predictable boundary due to unsafe random function).
**Learning:** Legacy projects often have deep dependency trees with outdated packages that are not directly listed in `package.json`.
**Prevention:** Regularly run `yarn audit` and use the `resolutions` field to force updates of transitive dependencies to patched versions when parent packages haven't updated their requirements.
