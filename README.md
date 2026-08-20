# Awesome-Cyber-Asset-Attack-Surface-Management

Markdown
# Top Cyber Asset Attack Surface Management (CAASM) Tools Ecosystem


**Curated List of SaaS/Hosted Platforms & Open-Source GitHub Projects**  
*Focused on Cyber Asset Attack Surface Management, Asset Discovery, Exposure Management, Attack Surface Visibility & Security Control Coverage*  
**Last updated: August 2026**


This repository tracks notable **SaaS/hosted platforms** and **open-source projects** for **Cyber Asset Attack Surface Management (CAASM)**. These tools help organizations continuously discover, inventory, normalize, classify, contextualize, and monitor cyber assets across endpoints, networks, cloud, SaaS, identities, applications, containers, OT/IoT, and internet-facing infrastructure.


**Examples** include Axonius, JupiterOne, Armis, Orca Security, Noetic Cyber, runZero, Panaseer, Tanium, Qualys CyberSecurity Asset Management, ServiceNow IT Asset Management, and other asset-visibility and exposure-management platforms. Current CAASM evaluations commonly include Axonius, Armis, Qualys CSAM, JupiterOne, runZero, and related platforms, although their approaches differ substantially. :contentReference[oaicite:0]{index=0}


CAASM overlaps with **Cyber Asset Management, IT Asset Management (ITAM), External Attack Surface Management (EASM), Digital Risk Protection, Exposure Management, Vulnerability Management, Continuous Controls Monitoring (CCM), Security Operations, CMDB, IT Discovery, Network Discovery, Cloud Security, OT/IoT Security, and Configuration Management**.


**Open-source emphasis**: This repository heavily emphasizes open-source software that can be self-hosted and combined into a CAASM architecture. The open-source ecosystem is considerably more fragmented than the commercial CAASM market, so the section includes both emerging dedicated attack-surface platforms and mature open-source projects for asset discovery, network scanning, endpoint inventory, vulnerability management, cloud inventory, security telemetry, attack-surface reconnaissance, and asset-data correlation.


A particularly relevant emerging project is **Open Attack Surface Management (OASM)**, an open-source platform designed for asset discovery, vulnerability assessment, technology detection, distributed scanning, monitoring, analytics, and AI-assisted asset analysis. :contentReference[oaicite:1]{index=1}


Another notable open-source exposure-management project is **XORCISM**, which combines asset management, vulnerability intelligence, security-tool integrations, CVE-to-asset matching, identity/device synchronization, and a large connector ecosystem. :contentReference[oaicite:2]{index=2}


The goal is to provide an ecosystem map ranging from **enterprise CAASM platforms** to **open-source building blocks for constructing a self-hosted cyber-asset inventory and attack-surface management platform**.


Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites or GitHub repositories.


## Table of Contents


- [SaaS/Hosted Platforms](#saashosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [Additional Open-Source & Security Infrastructure Projects](#additional-open-source--security-infrastructure-projects)
- [Building a Custom Open-Source CAASM Stack](#building-a-custom-open-source-caasm-stack)
- [Important CAASM Concepts](#important-caasm-concepts)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)


## SaaS/Hosted Platforms


- **[Axonius](https://www.axonius.com/)**  
  Cyber Asset Management and CAASM platform that aggregates data from security, IT, cloud, endpoint, identity, and infrastructure tools to create a unified view of organizational assets and identify security-control gaps.


- **[JupiterOne](https://www.jupiterone.com/)**  
  CAASM and cyber risk platform that continuously aggregates assets across cloud, code, identity, endpoints, SaaS, and other systems into a connected asset graph. It emphasizes relationships between assets, coverage gaps, policy-as-code, and cross-domain security queries. :contentReference[oaicite:3]{index=3}


- **[Armis](https://www.armis.com/)**  
  Asset intelligence and cyber exposure-management platform with particularly strong capabilities for unmanaged devices, IoT, OT, medical devices, operational technology, and other cyber-physical environments.


- **[Orca Security](https://orca.security/)**  
  Cloud-native security platform providing agentless cloud asset discovery, vulnerability management, cloud security posture management, attack-path analysis, and exposure management across cloud environments.


- **[Noetic Cyber](https://noeticcyber.com/)**  
  Cyber asset management and continuous controls monitoring platform designed to aggregate security and IT data, discover asset relationships, identify security-control gaps, and improve asset visibility.


- **[runZero](https://www.runzero.com/)**  
  Network-centric asset discovery platform combining active network scanning, passive discovery, fingerprinting, and integrations to identify managed, unmanaged, unknown, and potentially rogue assets across IT, OT, IoT, and remote environments. :contentReference[oaicite:4]{index=4}


- **[Panaseer](https://panaseer.com/)**  
  Cyber asset management and security-control monitoring platform focused on creating trusted asset inventories, correlating security telemetry, identifying control gaps, and measuring security-control effectiveness. :contentReference[oaicite:5]{index=5}


- **[Tanium](https://www.tanium.com/)**  
  Enterprise endpoint and asset-management platform providing real-time endpoint visibility, asset inventory, vulnerability management, configuration management, and security operations capabilities.


- **[Qualys CyberSecurity Asset Management](https://www.qualys.com/solutions/attack-surface-management)**  
  Cyber asset management platform for discovering, identifying, classifying, and managing known and unknown assets across hybrid IT. Qualys combines agents, scanners, passive network sensors, API integrations, cloud discovery, and external attack-surface capabilities. :contentReference[oaicite:6]{index=6}
Recommended Open-Source Combinations

Basic Network CAASM

Nmap + NetBox + PostgreSQL + Grafana

Suitable for organizations primarily interested in continuously discovering and inventorying network-connected assets.

Endpoint-Centric CAASM

osquery + Fleet + Wazuh + PostgreSQL/ClickHouse

Provides endpoint inventory, software information, security telemetry, vulnerability information, and centralized analysis.

External Attack Surface Stack

Amass + Subfinder + Naabu + httpx + Nuclei + PostgreSQL

Useful for continuously discovering domains, subdomains, IPs, ports, web services, technologies, and exposures on an organization's external attack surface.

Cloud CAASM Stack

CloudQuery + Steampipe + Cartography + Neo4j

Provides cloud-resource inventory together with relationship mapping and graph-based analysis.

Open-Source Exposure Management Stack

OASM + Nmap + Nuclei + OpenVAS + osquery + Wazuh

OASM can serve as the central attack-surface layer while specialized open-source scanners provide deeper asset and vulnerability telemetry. OASM explicitly supports distributed scanning, vulnerability assessment, technology detection, monitoring, and analytics. 
GitHub
+1

Advanced Open-Source CAASM Stack

Network Discovery → Endpoint Discovery → Cloud Discovery → Kafka → Asset Normalization → Neo4j/NetBox → Vulnerability Correlation → Risk Engine → Grafana/OpenSearch → SOAR

This architecture resembles the conceptual architecture of modern commercial CAASM platforms: aggregate data from many sources, normalize and deduplicate assets, establish relationships, identify missing security controls, enrich assets with vulnerabilities and business context, and automate remediation.

Exposure-Management Stack

XORCISM + Nmap/Nuclei/OpenVAS + Wazuh + CloudQuery + Neo4j

XORCISM is particularly interesting for this architecture because its connector ecosystem is designed to normalize findings and assets from many security tools and automatically correlate CVEs with affected assets. 
GitHub

Important CAASM Concepts

A complete CAASM system typically combines several capabilities:

Asset Discovery — Finding all known and unknown cyber assets.

Continuous Asset Inventory — Maintaining an up-to-date inventory rather than a periodic spreadsheet.

Asset Normalization — Converting heterogeneous data from multiple tools into a common asset model.

Asset Deduplication — Determining when multiple tools are referring to the same underlying asset.

Identity Resolution — Connecting different identifiers for the same device, application, user, or cloud resource.

Asset Enrichment — Adding ownership, location, business unit, criticality, vulnerabilities, and other context.

Asset Ownership — Determining who owns or is responsible for each asset.

Business Criticality — Identifying assets that are particularly important to business operations.

Unknown Asset Discovery — Finding assets absent from official inventories.

Shadow IT Discovery — Identifying unauthorized applications, services, devices, and infrastructure.

Rogue Asset Detection — Detecting unauthorized or unexpected devices.

Endpoint Discovery — Identifying laptops, desktops, servers, and other endpoints.

Network Discovery — Mapping network-connected devices and services.

Cloud Asset Discovery — Discovering resources across AWS, Azure, GCP, and other clouds.

SaaS Discovery — Identifying applications and SaaS services used by an organization.

Identity Discovery — Inventorying users, service accounts, roles, and machine identities.

Application Inventory — Tracking applications, services, APIs, and software components.

Container Discovery — Inventorying containers, images, clusters, and workloads.

Kubernetes Discovery — Mapping clusters, nodes, workloads, services, and identities.

OT/IoT Discovery — Identifying operational technology and Internet-of-Things assets.

External Attack Surface Management — Discovering Internet-facing infrastructure.

EASM — External Attack Surface Management for domains, IPs, applications, APIs, and services.

CAASM — Internal and cross-domain cyber asset visibility and security-control analysis.

ITAM — Lifecycle management of IT assets.

CMDB Integration — Connecting security asset intelligence with configuration-management databases.

Security Tool Integration — Ingesting information from EDR, XDR, SIEM, IAM, CSPM, vulnerability scanners, MDM, and other tools.

API-Based Discovery — Pulling asset data directly from cloud and security platforms.

Agentless Discovery — Discovering assets without deploying endpoint agents.

Active Scanning — Probing networks and services to discover assets.

Passive Discovery — Learning about assets from observed network traffic and telemetry.

Fingerprinting — Determining operating systems, services, applications, and technologies.

Vulnerability Correlation — Linking vulnerabilities to specific assets.

Configuration Assessment — Identifying insecure configurations.

Security Control Coverage — Determining which assets are protected by required controls.

Control Gap Detection — Identifying assets missing EDR, vulnerability scanning, MFA, encryption, logging, or other controls.

Continuous Controls Monitoring — Continuously verifying that security controls remain effective.

Exposure Management — Combining assets, vulnerabilities, misconfigurations, identities, and business context to prioritize risk.

Risk Prioritization — Ranking assets and exposures based on likelihood and business impact.

Attack Path Analysis — Understanding paths from exposures to critical assets.

Blast Radius Analysis — Determining the potential impact of compromised assets.

Crown Jewel Identification — Identifying highly sensitive or business-critical systems.

Asset Relationship Graphs — Modeling relationships between devices, users, applications, identities, networks, and data.

Dependency Mapping — Understanding infrastructure and application dependencies.

Business Context — Connecting technical assets to business owners, applications, departments, and processes.

Policy-as-Code — Defining security and asset-management requirements as machine-evaluable policies.

Compliance Coverage — Measuring whether assets satisfy regulatory or organizational controls.

Continuous Monitoring — Detecting asset changes and new exposures over time.

Drift Detection — Detecting changes from approved configurations or security baselines.

Lifecycle Management — Tracking asset creation, modification, ownership, retirement, and disposal.

Software Inventory — Maintaining an inventory of installed and deployed software.

End-of-Life Detection — Identifying unsupported hardware, operating systems, and software.

Attack Surface Reduction — Removing unnecessary, vulnerable, or unmanaged assets.

Remediation Automation — Automatically initiating actions against identified security gaps.

Security Orchestration — Connecting CAASM findings to ticketing, SOAR, ITSM, and remediation systems.

Data Quality — Measuring completeness, accuracy, freshness, and consistency of asset information.

Asset Confidence Scoring — Measuring confidence in discovered asset identities and attributes.

Real-Time Inventory — Maintaining near-real-time visibility into rapidly changing infrastructure.

Historical Asset Tracking — Maintaining a timeline of asset changes.

M&A Asset Discovery — Discovering inherited infrastructure during mergers and acquisitions.

Third-Party Asset Discovery — Identifying assets operated by vendors or third parties.

Internet Exposure Monitoring — Monitoring externally exposed services and infrastructure.

Attack Surface Graphs — Representing the relationships between assets, vulnerabilities, identities, and controls.

AI-Assisted Security Queries — Using AI to query and reason over asset inventories.

Natural-Language Asset Search — Asking security questions in natural language.

Automated Asset Classification — Automatically categorizing assets by type, owner, risk, or business function.

Automated Remediation — Triggering security or IT workflows when asset conditions violate policy.

Security Coverage Metrics — Measuring the percentage of assets covered by security controls.

Unknown-to-Known Conversion — Turning previously unidentified assets into managed assets.

Exposure-to-Asset Mapping — Connecting vulnerabilities and exposures to concrete assets.

Asset-to-Business Mapping — Connecting technical infrastructure to business services and owners.

How to Contribute

Fork the repo.

Add/edit entries in README.md (follow the existing format).

Include: name, official link or GitHub repository, 1–2 sentence description, and whether it is SaaS/hosted or open-source.

Prefer projects with active repositories and meaningful documentation.

For open-source projects, accurately identify the primary capability — CAASM, EASM, asset discovery, ITAM, endpoint inventory, vulnerability management, cloud discovery, network discovery, or supporting infrastructure.

Do not label a network scanner, vulnerability scanner, CMDB, or ITAM system as a complete CAASM platform unless it actually provides CAASM functionality.

Verify the project's current license before adding it.

Submit a PR with a short explanation.

Star the repo if you find it useful!

Disclaimer

This is a community-curated list — not exhaustive and not an endorsement.

CAASM overlaps significantly with ITAM, CMDB, EASM, vulnerability management, exposure management, cloud security, endpoint management, network discovery, and security operations.

The open-source ecosystem for complete CAASM platforms is substantially smaller than the commercial ecosystem. Many open-source projects therefore provide individual layers rather than a complete Axonius/JupiterOne/Armis equivalent.

Open-source, source-available, open-core, and hosted offerings are not equivalent. Always verify the current license and self-hosting terms before adoption.

Asset discovery and security scanning should only be performed on systems and networks that you own or are explicitly authorized to assess.

Active Internet scanning can generate substantial traffic and may trigger security controls or provider abuse mechanisms. Use appropriate authorization, rate limits, and scanning policies.

Asset inventories may contain sensitive infrastructure, identity, vulnerability, and security information and should be protected accordingly.

Production CAASM systems should implement appropriate authentication, authorization, encryption, audit logging, retention, backup, disaster recovery, and data-governance controls.

Security findings should be validated before automated remediation is performed.

Made for CISOs, security architects, SecOps teams, IT asset managers, vulnerability-management teams, cloud-security engineers, network teams, DevSecOps teams, and developers building modern cyber-asset visibility platforms.
Let's make cyber asset attack surface management more open, composable, transparent, continuously monitored, and developer-friendly.
