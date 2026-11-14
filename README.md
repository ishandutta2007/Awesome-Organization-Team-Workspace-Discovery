# Awesome-Organization-Team-Workspace-Discovery

# Awesome Organization Team & Workspace Discovery

> A curated list of top Organization Team and Workspace Discovery platforms — both SaaS/Hosted commercial internal developer portals and open-source alternatives for cataloging services, teams, and workspaces to make organizational context discoverable.
> 🌟 Star this repo if you find it useful! 🌟

---

## 📋 Table of Contents

- [SaaS / Hosted Platforms](#-saas--hosted-platforms)
  - [Cortex](#cortex)
  - [Port](#port)
  - [OpsLevel](#opslevel)
  - [Atlassian Compass](#atlassian-compass)
  - [Postman Team Discovery](#postman-team-discovery)
- [Open-Source Software](#-open-source-software)
  - [Backstage](#backstage)
  - [Imbi](#imbi)
  - [OpenChoreo](#openchoreo)
  - [OpenCRM (clawnify)](#opencrm-clawnify)
- [Comparison at a Glance](#-comparison-at-a-glance)
- [Contributing](#-contributing)

---

## 🟦 SaaS / Hosted Platforms

Commercial, cloud-hosted Organization Team and Workspace Discovery platforms. These are not open-source but are included as reference points for feature comparison.

### Cortex
**Type:** Internal developer portal with scorecards and initiatives
Cortex is an enterprise-focused internal developer portal and service catalog used by platform teams to inventory services, libraries, domains, teams, and resources . It goes beyond cataloging by **measuring services against Scorecards** for production readiness, security, SLO compliance, cost, and AI usage, and drives developer experiences through Initiatives, Workflows, and Scaffolder templates . It pulls signals from GitHub, GitLab, AWS, Azure, GCP, and Datadog. **Pricing:** Cortex targets the enterprise segment with per-service pricing that is higher than Port at comparable service counts, justified by deeper operational maturity features like initiative tracking and CTO dashboards . A free tier exists for evaluation, but the product is built for organizations with dedicated platform engineering capacity.  
**Best for:** Enterprises needing operational maturity and standards enforcement across a large service inventory, with the budget and platform team to support it.

### Port
**Type:** AI-powered internal developer portal with fast time-to-value
Port is a commercial SaaS internal developer portal that ships a functional portal in **days** with native self-service actions, scorecards, SSO/SAML, RBAC, and audit logging working from day one . Its **no-code portal builder** and AI assistant lower the barrier for platform teams without dedicated frontend engineers. The trade-off is per-service pricing that scales linearly and less room for deeply custom integrations compared to Backstage. For a 100-service organization, the annual subscription is in the mid-five-figure range, with zero to one platform engineers needed for configuration .  
**Best for:** Mid-market engineering teams (30-200 developers) wanting a production-grade portal quickly without the operational burden of self-hosting.

### OpsLevel
**Type:** Service catalog with fast deployment and lower cost
OpsLevel provides a service catalog with a focus on **30-45 day deployment** and a lower price point than Port and Cortex (~$39/user/month per one comparison, though this may vary) . It is positioned as the speed-and-value choice for teams that need catalog and scorecard functionality without the customization depth of Backstage or the AI features of Port. For a 200-person engineering team, OpsLevel's licensing cost is significantly lower than Port's, making it a strong option for budget-conscious organizations that still need a commercial portal.  
**Best for:** Teams prioritizing deployment speed and cost efficiency over advanced AI or deep customization.

### Atlassian Compass
**Type:** Developer portal within the Atlassian ecosystem
Compass provides a software catalog and developer portal integrated with Jira, Jira Service Management, Bitbucket, and Opsgenie. The **Free plan** supports unlimited basic users and up to three full users, making it accessible for small teams. **Standard** is $7.67/user/month and **Premium** is $23.96/user/month, with Premium adding advanced compliance and data features . Compass is **Cloud-only** (no Data Center option), which matters for organizations requiring self-hosted infrastructure . It is the natural choice for teams already standardized on Atlassian tools.  
**Best for:** Atlassian-centric organizations wanting a catalog that connects directly to their existing Jira and Bitbucket workflows.

### Postman Team Discovery
**Type:** Workspace and team discovery within Postman
Postman's **Team Discovery** allows users with a verified company email domain to find and request to join teams, with optional **automatic joining** that skips admin approval . Admins can add a question for pending members to answer, and receive email notifications when discovery is active or someone requests to join. The **Publisher Profile** serves as a developer portal for API consumers, bringing together public workspaces, collections, APIs, and flows with a verified organization badge . This is workspace discovery within the Postman platform rather than a cross-organizational service catalog.  
**Best for:** Organizations already using Postman Enterprise wanting to make their API teams and workspaces discoverable to colleagues.

---

## 🟩 Open-Source Software

Self-hosted, community-driven Organization Team and Workspace Discovery tools. The open-source ecosystem is **anchored by Backstage** as the most widely adopted developer portal framework, with complementary platforms for service cataloging and workspace management.

### Backstage
**Stack:** TypeScript / React / Node.js | **License:** Apache-2.0
Backstage (Spotify, CNCF Incubating) is the most widely adopted open-source developer portal framework, with **28,000+ GitHub stars** and a plugin-based architecture for building custom developer experiences . It provides a **software catalog** using YAML-based metadata, **Software Templates** (Scaffolder) for standardized project creation, and **TechDocs** for documentation-as-code. **Critical reality check:** Backstage adoption stalls at less than 10% outside Spotify, with a true total cost of ownership reaching **$150,000 per 20 developers** in engineering time. Teams require **2-5 full-time engineers minimum** for ongoing maintenance, and implementation timelines stretch to **6-12 months** for basic functionality . The break-even point where Backstage becomes cheaper than commercial alternatives is typically **300-500 services** depending on engineer costs .  
**Best for:** Large engineering organizations (500+ engineers) with a dedicated platform team and frontend expertise willing to invest in a custom, extensible portal.

### Imbi
**Stack:** Python / FastAPI / React / PostgreSQL / ClickHouse | **License:** Open Source (AWeber)
Imbi is an open-source **service and project catalog** developed by AWeber, with graph-based data modeling via PostgreSQL (Apache AGE) and analytics via ClickHouse . It provides a UI (React/Vite), API (FastAPI), gateway (Caddy with automatic HTTPS), and MCP server (FastMCP) for AI agent access . Features include project and service inventory, permissions seeding, and OAuth2/OIDC authentication (Google, GitHub, Keycloak) plus local auth. Deploys via Docker Compose or Helm, with a single admin setup command . It is a focused catalog rather than a full portal framework, with a smaller community than Backstage.  
**Best for:** Teams wanting a lightweight, self-hosted service catalog with graph data modeling and AI agent access, accepting a smaller ecosystem.

### OpenChoreo
**Stack:** Go / Kubernetes | **License:** Open Source
OpenChoreo is an open-source **internal developer platform** built on Kubernetes that includes a **software catalog and discoverability** as a core feature. All exposed APIs, events, and data are **automatically registered in an internal catalog** with metadata including endpoint path, visibility, and owning project, enabling discovery and governance of service interfaces across teams and environments . It uses Domain-Driven Design abstractions (Projects, Components, Endpoints, Connections) that map to Kubernetes resources, with built-in ingress/egress API management, zero-trust security via Cilium, and observability by default . It is a full platform rather than a standalone catalog.  
**Best for:** Kubernetes-native teams wanting an integrated platform with automatic service cataloging as part of a broader developer platform.

### OpenCRM (clawnify)
**Stack:** SQLite / REST API | **License:** Open Source
OpenCRM (clawnify) is a lightweight HubSpot alternative for SaaS, managing contacts, companies, and deals with custom attributes, relations, and a REST API . While not a developer portal or service catalog, it provides **organizational entity discovery** for sales and CRM contexts. It supports custom field definitions and relation columns, with flexible filtering operators for list endpoints. This is included as a reference for teams wanting a minimal, API-driven entity catalog rather than a platform engineering tool.  
**Best for:** SaaS teams wanting a minimal, API-driven CRM with custom entities and relations, not for developer service discovery.

---

## 📊 Comparison at a Glance

| Software | License | Stack | Service Catalog | Scorecards | Self-Service | Self-Hosted | Best For |
|----------|---------|-------|-----------------|------------|--------------|-------------|----------|
| **Cortex** | Proprietary | Cloud | ✅ | ✅ Deep | ✅ | ❌ | Enterprise standards enforcement |
| **Port** | Proprietary | Cloud | ✅ | ✅ | ✅ Native | ❌ | Mid-market fast time-to-value |
| **OpsLevel** | Proprietary | Cloud | ✅ | ✅ | (Check) | ❌ | Speed + cost efficiency |
| **Compass** | Proprietary | Cloud | ✅ | (Check) | (Atlassian) | ❌ | Atlassian ecosystem |
| **Postman Discovery** | Proprietary | Cloud | (Workspaces) | ❌ | (Join) | ❌ | API workspace discovery |
| **Backstage** | Apache-2.0 | TypeScript | ✅ YAML-based | (Plugins) | ✅ Scaffolder | ✅ | Custom portal at scale |
| **Imbi** | Open Source | Python/React | ✅ Graph-based | ❌ | (Check) | ✅ | Lightweight catalog + AI access |
| **OpenChoreo** | Open Source | Go/K8s | ✅ Automatic | ❌ | (Platform) | ✅ | K8s-native platform + catalog |

---

## 🤝 Contributing

Contributions are welcome! If you know of an open-source Organization Team or Workspace Discovery tool that should be listed here, please open a pull request with:

- Project name and URL
- Brief description (1–2 sentences)
- Stack and license
- Why it stands out

Please ensure the project is actively maintained (releases within the last 12 months) and genuinely open-source.

**Note on the open-source ecosystem:** Organization and workspace discovery splits between **full developer portal frameworks** (Backstage) and **focused service catalogs** (Imbi). **Backstage** is the dominant open-source option but carries a hidden cost that many teams underestimate—$150k per 20 developers in engineering time and 6-12 months to basic functionality . Commercial alternatives like Port and OpsLevel deliver working portals in 30-45 days, making them cost-effective for teams under 300-500 services . **Imbi** offers a lighter-weight, self-hosted catalog with graph modeling and MCP access, while **OpenChoreo** embeds automatic service cataloging into a Kubernetes-native platform . For workspace discovery specifically, **Postman Team Discovery** and **Atlassian Compass** serve their respective ecosystems, but neither is a general-purpose organizational catalog.

---

## 📄 License

This list is released under CC0 1.0 Universal (Public Domain). The software projects listed retain their respective licenses.

---

⭐ **If this list helped you discover a useful tool, please star the repo!** ⭐
