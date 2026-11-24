<div align="center">

# GRCForge

**Open tools for Governance, Risk and Compliance — practical, self-hosted, made for European requirements.**

[Website](https://www.herz.dev) · [OpenISMS](https://github.com/GRCForge/OpenISMS) · [Releases](https://github.com/GRCForge/OpenISMS/releases) · [Security policy](https://github.com/GRCForge/OpenISMS/blob/main/SECURITY.md)

</div>

---

GRCForge builds software for the people who run an information security management system day to day: ISOs and CISOs, IT auditors, compliance teams and the admins who have to deliver the evidence. The tools follow the standards the way auditors read them — ISO/IEC 27001, NIS-2 with the German BSIG, BSI IT-Grundschutz, BSI C5, TISAX, DORA, GDPR and the EU AI Act — and keep your data on your own infrastructure.

## Projects

### [OpenISMS](https://github.com/GRCForge/OpenISMS)

An open, practice-oriented ISMS: one container plus PostgreSQL.

| | |
|---|---|
| **One register for everything** | Assets, risks, controls, policies, incidents, vendors and evidence reference each other — one control can satisfy ISO 27001, NIS-2, BSI and C5 requirements at the same time. |
| **Evidence, not checkboxes** | Every change is audit-logged and signed, documents are hash-verified, and the relationship analysis shows *why* a requirement counts as met. |
| **BSI IT-Grundschutz** | Versioned catalogues (Kompendium 2023 and Grundschutz++ via OSCAL), information domains, modelling of target objects and the IT-Grundschutz check per target object following BSI Standard 200-2. |
| **NIS-2 and BSIG** | Applicability check and self-check, gap analysis, 24 h / 72 h reporting deadlines for incidents. |
| **Privacy** | GDPR processing register, DPIA, data subject requests, data flows. |
| **AI-ready** | Built-in MCP server and a REST API documented with OpenAPI — assistants work under the same permissions as every user. |
| **Self-hosted** | Docker image `ghcr.io/grcforge/openisms-app`, Docker Compose or systemd. Your data stays with you. |

```bash
git clone https://github.com/GRCForge/OpenISMS.git && cd OpenISMS
cp .env.example .env   # set the secrets as described in the README
docker compose up -d --build
```

## How we build

- **Security first.** Pull requests run CodeQL, Trivy, Gitleaks, Snyk and `npm audit`; SonarQube checks `main`. Releases ship with CycloneDX SBOMs. Findings get fixed, not suppressed.
- **Standards as written.** Requirements come from the official sources — BSI catalogues, for example, are imported at runtime instead of copied and paraphrased.
- **Traceable by design.** Signed audit log, versioned catalogues and release notes for every version.
- **Current stack.** Node.js, React and PostgreSQL, kept up to date continuously.

## Get involved

- **Questions, bugs, ideas:** open an issue in the project repository.
- **Vulnerabilities:** please report them privately as described in the [security policy](https://github.com/GRCForge/OpenISMS/blob/main/SECURITY.md), not in a public issue.
- **Contributions and translations:** see [CONTRIBUTING.md](https://github.com/GRCForge/OpenISMS/blob/main/CONTRIBUTING.md). Translations (English, German, Spanish) are managed with Crowdin.

## Licence

OpenISMS is source-available: free for private and non-commercial use. Commercial or enterprise use and redistribution require a commercial licence — enquiries to **info@herz.dev**.

<div align="center">
<sub>Made in Germany · © 2026 Maximilian Herz</sub>
</div>
