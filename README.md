# Awesome-Identity-And-Access-Management

# Top Identity and Access Management (IAM) Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on SSO, Identity Federation & Self-Hosted IAM Platforms*  
**Last updated: November 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Identity and Access Management (IAM)**. These tools enable organizations to centralize authentication, enforce multi-factor authentication, manage user lifecycles, and govern access to applications—providing a single identity plane across workforce, customer, and partner ecosystems.

**Examples** include Atlassian Access, Okta, Microsoft Entra ID, Ping Identity, OneLogin, JumpCloud, CyberArk, ForgeRock, Auth0, and Duo Security (the category leaders).

**Open-source emphasis**: IAM is a domain where open-source tooling is **exceptionally mature and production-proven**, with clear leaders for different scales and philosophies. **Keycloak** remains the most widely deployed open-source identity server—Apache-2.0 licensed, backed by Red Hat, with deep support for OIDC, OAuth 2.0, SAML, LDAP federation, and identity brokering . **Casdoor** offers the broadest protocol coverage in a single Go binary—OIDC, SAML, CAS, LDAP, RADIUS, and SCIM, plus built-in Casbin authorization for ACL/RBAC/ABAC . **Authentik** provides the most flexible sign-in flow engine for homelabs and proxy-based SSO . **ZITADEL** is purpose-built for multi-tenant B2B SaaS with organizations and delegated administration . The critical caveat: **commercial platforms differentiate on managed compliance, customer identity at scale, and AI-driven access decisions**—Okta's Customer Identity for external users and Ping's AI-powered fraud/risk protection remain commercial advantages that open-source requires assembly to match .

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-products)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[Atlassian Access](https://www.atlassian.com/)**  
  SSO and security controls across Atlassian Cloud products; enforces SAML SSO, SCIM provisioning, and audit logs for Jira, Confluence, and Bitbucket users.

- **[Okta](https://www.okta.com/)**  
  The leading independent identity platform; Workforce Identity for employees and Customer Identity for external users, with SSO, MFA, lifecycle management, and governance across thousands of app integrations .

- **[Microsoft Entra ID](https://www.microsoft.com/en-us/security/business/microsoft-entra)**  
  Microsoft's cloud identity service with SSO, Conditional Access, MFA, and lifecycle workflows; deeply integrated with Microsoft 365 and Azure, with P1 included in many M365 plans .

- **[Ping Identity](https://www.pingidentity.com/)**  
  Enterprise identity platform (merged with ForgeRock) with PingOne for Customers and Workforce; AI-driven access decisions, fraud/risk protection, identity governance, and decentralized identity capabilities .

- **[OneLogin](https://www.onelogin.com/)**  
  Identity and access management platform (now part of One Identity) with SSO, MFA, and automated user provisioning.

- **[JumpCloud](https://jumpcloud.com/)**  
  Cloud directory platform combining SSO, device management, LDAP, and Directory-as-a-Service lifecycle management; positioned for small to mid-sized organizations .

- **[CyberArk](https://www.cyberark.com/)**  
  Identity security platform with privileged access management (PAM), identity governance, and secrets management; focused on protecting high-privilege accounts.

- **[ForgeRock](https://www.forgerock.com/)**  
  Identity platform (merged with Ping Identity) with comprehensive IAM, access management, and identity gateway capabilities; AI/ML-powered real-time access adaptation .

- **[Auth0](https://auth0.com/)**  
  Developer-focused identity platform for applications; B2B plans include Self-Service SSO and SCIM, with add-ons for enterprise connections and MFA.

- **[Duo Security (Cisco)](https://duo.com/)**  
  MFA and zero-trust access platform; provides phishing-resistant authentication, device trust, and adaptive access policies.

## Open-Source GitHub Projects

### Full IAM Platforms (Keycloak, Casdoor)

- **[Keycloak](https://github.com/keycloak/keycloak)**  
  The **most widely deployed open-source identity server** (Apache-2.0, ~37k GitHub stars, CNCF incubating, Red Hat-backed) . Features: **OIDC, OAuth 2.0, SAML 2.0**, LDAP/AD user federation, identity brokering, fine-grained authorization services, and **SCIM 2.0 server support (since 26.8)** . **Caveats**: Java application with significant tuning/upgrade/theming effort; **no official managed service** from the project—commercial support requires Red Hat subscription or third parties . **Best for enterprises wanting the most mature, auditor-recognized IAM foundation**—especially those already standardized on Red Hat or Java.

- **[Casdoor](https://github.com/casdoor/casdoor)**  
  The **broadest-protocol open-source IAM platform in a single Go binary** (Apache-2.0, ~14.5k GitHub stars) . Features: **OIDC, OAuth 2.0, SAML, CAS, LDAP server, RADIUS server, and SCIM**—so it can replace legacy LDAP or CAS servers rather than sit beside them ; **70+ social/enterprise identity providers**; **built-in Casbin authorization** for ACL/RBAC/ABAC; **MCP server and OAuth 2.1 for AI agents** (unique among open-source IAM) ; syncers for Keycloak, Okta, Entra ID, Google Workspace, and any SQL database . **Managed cloud**: Casdoor Cloud from $24/month (billed yearly) for a dedicated instance, no per-user fees . **Caveats**: smaller community than Keycloak; documentation lags features per user reports; no SOC 2/ISO 27001 reports yet . **Best for teams wanting maximum protocol coverage and a lightweight single binary**—especially those needing LDAP/RADIUS replacement or AI-agent auth.

### Flexible Flow Engines (Authentik, ZITADEL)

- **[Authentik](https://github.com/goauthentik/authentik)**  
  The **most flexible sign-in flow engine** among open-source IAM platforms (MIT core, enterprise features under commercial license) . Features: **visual flow and stage editor** for custom authentication logic; **proxy provider** for adding SSO to apps with no login integration (Traefik, Caddy, Nginx, Envoy); OIDC, SAML, LDAP, and RADIUS outposts . **Caveats**: **no managed cloud** from the maintainers; enterprise features licensed per internal user ($5/user/month) . **Best for homelabs and self-hosters** wanting visual flow customization and proxy-based SSO—less suited for large enterprise governance.

- **[ZITADEL](https://github.com/zitadel/zitadel)**  
  A **Go platform built for multi-tenant B2B SaaS** (AGPL-3.0, ~15.3k GitHub stars) . Features: **organizations and delegated administration** built in; OIDC, SAML, LDAP identity provider; **managed cloud priced by daily active users** (free up to 100 DAU, Pro $100/month for 25,000) . **Caveats**: **AGPL-3.0 copyleft** may require legal review; **no LDAP or RADIUS server** capabilities (unlike Casdoor) . **Best for B2B SaaS companies** needing native multi-tenancy—not for teams needing to replace legacy LDAP infrastructure.

### Additional Strong Open-Source Options

- **Ory (Hydra, Kratos)** — Headless, API-first identity services (Apache-2.0); Hydra is an OpenID Certified OAuth 2.0 server . **Caveat**: **no admin UI or login pages** in open-source—you build all screens yourself; SAML lives in separate product Ory Polis . **Best for teams wanting API primitives** and willing to build UI.
- **Apache Syncope** — Open-source IAM/IGA platform (Apache-2.0) with user/group/role management, automated provisioning workflows, RBAC, delegated administration, and **SAML 2.0/OIDC/SCIM support** . **Best for organizations needing IGA capabilities** (provisioning, access reviews) alongside IAM—less focused on SSO UX than Keycloak or Casdoor.
- **midPoint (Evolveum)** — The **most feature-complete open-source IGA platform** (Apache-2.0); full provisioning, access reviews, role management, organizational structure, and RBAC . **Caveat**: steep learning curve; documentation solid but setup takes real time . **Best for IGA-focused deployments** needing SailPoint-equivalent governance—not a pure SSO replacement.
- **WSO2 Identity Server** — Enterprise-grade open-source IAM (Apache-2.0); SSO, MFA, OAuth2/OIDC, SAML, identity federation, social login, RBAC, fine-grained authorization, and **GDPR/HIPAA compliance features** . **Best for enterprises wanting a mature, compliance-oriented IAM** with commercial support options—heavier than Casdoor or Authentik.

**Frameworks for building custom systems**: For **enterprise IAM with the broadest community and audit recognition**, Keycloak . For **maximum protocol coverage (OIDC/SAML/CAS/LDAP/RADIUS/SCIM) in a single binary**, Casdoor . For **visual flow customization and proxy SSO**, Authentik . For **B2B SaaS multi-tenancy**, ZITADEL . For **IGA with provisioning and access reviews**, midPoint or Apache Syncope . **No open-source project matches the managed customer identity scale and AI-driven risk decisions** of Okta Customer Identity or Ping—those are commercial advantages .

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- IAM platforms handling authentication credentials and identity data must comply with applicable security standards (SOC 2, ISO 27001) and privacy regulations; **self-hosted IdPs become critical infrastructure**—an outage or misconfiguration can lock users out of all connected applications.
- **Open-source IAM is exceptionally mature**—Keycloak provides enterprise-grade SSO and federation , Casdoor provides the broadest protocol coverage in a single binary , and Authentik/ZITADEL serve specialized needs . However, **commercial platforms differentiate on managed compliance, customer identity at scale, and AI-driven access decisions**—Okta Customer Identity and Ping's AI-powered risk protection remain commercial advantages. Choose based on whether you need maximum community/audit recognition (Keycloak), protocol breadth (Casdoor), visual flows (Authentik), or B2B multi-tenancy (ZITADEL).
- Verify license terms for commercial use; Keycloak and Casdoor use Apache-2.0 , ZITADEL uses AGPL-3.0 , and Authentik uses MIT for core with commercial enterprise features .

---

**Made for identity architects, IT administrators, and security engineers choosing their IAM platform.**  
Let's make identity and access management more open, but with clear eyes about the managed customer identity and AI-driven risk decisions that commercial platforms still lead on.
