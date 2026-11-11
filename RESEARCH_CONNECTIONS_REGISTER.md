# Research Connections & Access Register

**Purpose:** Central index of research services, their intended role, verified ChatGPT access status, account restrictions and cost controls.

**Status checked:** 11 November 2026  
**Maintenance rule:** Update this file only after a live connector check or a confirmed account change. Tool availability is not proof that an external account is connected. A successful browser sign-in is not proof that ChatGPT's connector authorization has switched accounts.

## 1. Research and intelligence sources

| Service | Intended use | ChatGPT access status | Account / limitation | Cost control |
|---|---|---|---|---|
| ChatGPT web research | Public web research, current reporting and source discovery | Available | Public-web access; does not imply access to private accounts | Use public sources first |
| GitHub | Read project instructions, research registers and working documents | Verified | Authenticated GitHub access; repositories under `siiro-byte` were listed and relevant files read | No paid operation performed |
| Windsor.ai | Cross-platform analytics and connected data reporting | Connected; data reads restricted | Current workspace returned 12 connected accounts. The Free plan's one-account limit blocks reads until the account limit is resolved. Do not disconnect or upgrade without approval. | No upgrade or paid call without fresh approval |
| Windsor.ai — YouTube | YouTube channel analytics through Windsor | Not verified | Latest connector check did not return a YouTube account. A browser message saying authorization succeeded is not sufficient to establish data access. | No further paid action without approval |
| Metricool | Social publishing and performance analytics | Connector profiles available | Two Metricool connection profiles are exposed: **Primary** and **Metricool**. This confirms connector profiles, not which brands or channels each profile can access. Verify brand/account scope before analysis or publishing. | Use existing access; no paid upgrade without approval |
| vidIQ | YouTube keyword, topic and channel research | Tool availability only; account authorization not verified here | Do not assume a paid vidIQ plan or channel connection | Check plan/credits before any metered action |
| Similarweb | Website traffic and competitor intelligence | Tool availability only; account authorization not verified here | Account-level entitlement not established | Check plan/credits before any metered action |
| Ahrefs | SEO, keyword and backlink intelligence | Tool availability only; account authorization not verified here | Account-level entitlement not established | Check plan/credits before any metered action |
| Firecrawl | Website extraction and structured page research | Tool availability only; account authorization not verified here | Account-level entitlement not established | Check credits and estimated cost before use |
| Notion | Workspace research and knowledge capture | Not verified in this access review | Do not assume a workspace is connected | No paid action without approval |
| Composio | Orchestration across authorized external services | Tool available; target-app authorization must be checked per workflow | A Composio tool being available does not establish that a particular app account is authorized | Inspect usage/cost before calls; no paid use without approval |

## 2. Project source registers

| Project | Register | Purpose |
|---|---|---|
| Travel Alerts.ke | https://github.com/siiro-byte/travel-alerts-ke/blob/main/SOURCES.md | Official authorities, regional bodies, credible media and traveller-signal sources |
| TikTok Growth Intelligence | https://github.com/siiro-byte/Tiktok-growth-intelligence-system/blob/main/SOURCES.md | Platform-native trend sources, first-party analytics, competitor observation and brand-specific research |
| Master working principles | https://github.com/siiro-byte/Chatgpt.-Md/blob/main/CHATGPT.md | Evidence standards, verification, user control and project guidance |
| Travel Alerts.ke research entry point | https://github.com/siiro-byte/Chatgpt.-Md/blob/main/TRAVELALERTS_RESEARCH.md | Research priorities, geographic coverage, source discipline and publication gate |

## 3. Project routing

### Travel Alerts.ke
- Primary evidence: responsible national authorities, immigration and border agencies, health ministries, aviation authorities, airport/airline operators, emergency services and official travel advisories.
- Corroboration and discovery: Reuters, AP, BBC, established regional media and specialist reporting.
- Social and Reddit: leads only; independently verify before treating claims as facts.
- Analytics and growth: Metricool, vidIQ and other services only after the correct Travel Alerts.ke account is confirmed.
- Keep Africa-wide coverage balanced; include global developments when they materially affect travellers.

### Simo Traveller
- YouTube discovery: YouTube Studio/YouTube-native research and vidIQ where authorized.
- Social analytics: Metricool and Windsor only after the correct Simo Traveller account and reporting period are confirmed.
- Keep its audience and performance analysis separate from Travel Alerts.ke.

### KA-IN
- Competitor and market research: public competitor websites and public evidence, with Similarweb/Ahrefs only where authorized and cost-checked.
- Performance analysis: use the correct KA-IN brand and connected social accounts; do not mix data from other brands.

## 4. Mandatory preflight checks

Before using a connected analytics or research service:
1. Confirm the exact service and authenticated connection profile.
2. Confirm the target account, brand, channel or workspace.
3. Confirm the metric, date range, timezone and data availability.
4. Check account restrictions, plan limits, credits and estimated usage cost.
5. If any of these are unknown, report the gap rather than assuming access or interpreting missing data as zero.

## 5. Spending and authorization policy

- Default research spend: **KES 0**.
- Prefer official public sources and existing included access.
- No subscriptions, upgrades, paid API calls, metered scraping, premium reports, advertising spend or credit-consuming operations without explicit fresh approval.
- Before requesting approval for a paid operation, state the provider, purpose, exact operation/data requested, estimated cost and maximum where known, currency and KES equivalent, and free alternatives.
- Never bypass a plan limit by switching accounts, disconnecting accounts or using another workspace without the user's explicit authorization.
- A successful login or OAuth consent screen is not proof that the connector is using that account. Verify by reading the connector's returned account list or successfully retrieving the intended data.

## 6. Verification history

| Date | Check | Result |
|---|---|---|
| 11 Nov 2026 | GitHub repository and project-file access | Relevant repositories and source-register files were readable |
| 11 Nov 2026 | Windsor.ai connected accounts | Connected-account list returned; data access restricted by Free-plan account limit |
| 11 Nov 2026 | Windsor.ai YouTube connector | No YouTube account appeared in the returned connected-account list |
| 11 Nov 2026 | Metricool connection profiles | Two profiles, Primary and Metricool, exposed by connector tool schema; brand-level scope still requires live verification |

**Important:** This register records access evidence available at the time of checking. It is not a guarantee that a provider's service, account permissions, plan or connector state will remain unchanged.
