## 2026-04-16 - Dependency Vulnerabilities: axios SSRF and form-data Unsafe Random Boundary
**Vulnerability:** Critical vulnerabilities in nested dependencies: `axios` (SSRF due to hostname normalization bypass) and `form-data` (Predictable boundary due to unsafe random function).
**Learning:** Legacy projects often have deep dependency trees with outdated packages that are not directly listed in `package.json`.
**Prevention:** Regularly run `yarn audit` and use the `resolutions` field to force updates of transitive dependencies to patched versions when parent packages haven't updated their requirements.
