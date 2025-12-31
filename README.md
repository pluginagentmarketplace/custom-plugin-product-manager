<div align="center">

<!-- Animated Typing Banner -->
<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=28&duration=3000&pause=1000&color=2E9EF7&center=true&vCenter=true&multiline=true&repeat=true&width=600&height=100&lines=Product+Manager+Assistant;8+Agents+%7C+12+Skills;Claude+Code+Plugin" alt="Product Manager Assistant" />

<br/>

<!-- Badge Row 1: Status Badges -->
[![Version](https://img.shields.io/badge/Version-1.0.0-blue?style=for-the-badge)](https://github.com/pluginagentmarketplace/custom-plugin-product-manager/releases)
[![License](https://img.shields.io/badge/License-Custom-yellow?style=for-the-badge)](LICENSE)
[![Status](https://img.shields.io/badge/Status-Production-brightgreen?style=for-the-badge)](#)
[![SASMP](https://img.shields.io/badge/SASMP-v1.3.0-blueviolet?style=for-the-badge)](#)

<!-- Badge Row 2: Content Badges -->
[![Agents](https://img.shields.io/badge/Agents-8-orange?style=flat-square&logo=robot)](#-agents)
[![Skills](https://img.shields.io/badge/Skills-12-purple?style=flat-square&logo=lightning)](#-skills)
[![Commands](https://img.shields.io/badge/Commands-4-green?style=flat-square&logo=terminal)](#-commands)

<br/>

<!-- Quick CTA Row -->
[📦 **Install Now**](#-quick-start) · [🤖 **Explore Agents**](#-agents) · [📖 **Documentation**](#-documentation) · [⭐ **Star this repo**](https://github.com/pluginagentmarketplace/custom-plugin-product-manager)

---

### What is this?

> **Product Manager Assistant** is a Claude Code plugin with **8 agents** and **12 skills** for product manager development.

</div>

---

## 📑 Table of Contents

<details>
<summary>Click to expand</summary>

- [Quick Start](#-quick-start)
- [Features](#-features)
- [Agents](#-agents)
- [Skills](#-skills)
- [Commands](#-commands)
- [Documentation](#-documentation)
- [Contributing](#-contributing)
- [License](#-license)

</details>

---

## 🚀 Quick Start

### Prerequisites

- Claude Code CLI v2.0.27+
- Active Claude subscription

### Installation (Choose One)

<details open>
<summary><strong>Option 1: From Marketplace (Recommended)</strong></summary>

```bash
# Step 1️⃣ Add the marketplace
/plugin add marketplace pluginagentmarketplace/custom-plugin-product-manager

# Step 2️⃣ Install the plugin
/plugin install product-manager-assistant@pluginagentmarketplace-product-manager

# Step 3️⃣ Restart Claude Code
# Close and reopen your terminal/IDE
```

</details>

<details>
<summary><strong>Option 2: Local Installation</strong></summary>

```bash
# Clone the repository
git clone https://github.com/pluginagentmarketplace/custom-plugin-product-manager.git
cd custom-plugin-product-manager

# Load locally
/plugin load .

# Restart Claude Code
```

</details>

### ✅ Verify Installation

After restart, you should see these agents:

```
product-manager-assistant:01-strategy-vision
product-manager-assistant:06-analytics-metrics
product-manager-assistant:07-leadership-stakeholder
product-manager-assistant:04-roadmap-prioritization
product-manager-assistant:05-launch-gtm
... and 2 more
```

---

## ✨ Features

| Feature | Description |
|---------|-------------|
| 🤖 **8 Agents** | Specialized AI agents for product manager tasks |
| 🛠️ **12 Skills** | Reusable capabilities with Golden Format |
| ⌨️ **4 Commands** | Quick slash commands |
| 🔄 **SASMP v1.3.0** | Full protocol compliance |

---

## 🤖 Agents

### 8 Specialized Agents

| # | Agent | Purpose |
|---|-------|---------|
| 1 | **01-strategy-vision** | Ürün stratejisi, market analizi, positioning ve vizyonu tanı |
| 2 | **06-analytics-metrics** | Veri tabanlı karar alma ve ürün metrikleri yönetimi uzmanı.  |
| 3 | **07-leadership-stakeholder** | Stakeholder yönetimi, cross-functional liderlik ve ürün advo |
| 4 | **04-roadmap-prioritization** | Ürün roadmap planlama ve feature prioritization uzmanı. Cons |
| 5 | **05-launch-gtm** | Ürün launch ve go-to-market (GTM) stratejisi uzmanı. Pazara  |
| 6 | **02-discovery-research** | Kullanıcı araştırması, customer insights ve discovery yöneti |
| 7 | **03-requirements-definition** | Ürün gereksinimlerini tanımlama, spesifikasyon yazma ve acce |

---

## 🛠️ Skills

### Available Skills

| Skill | Description | Invoke |
|-------|-------------|--------|
| `roadmap` | Master prioritization frameworks, roadmap planning, timeline | `Skill("product-manager-assistant:roadmap")` |
| `launch` | Master go-to-market strategy, launch planning and execution, | `Skill("product-manager-assistant:launch")` |
| `discovery` | Master user research methodologies, customer interviews, per | `Skill("product-manager-assistant:discovery")` |
| `requirements` | Master requirements gathering, user story writing, acceptanc | `Skill("product-manager-assistant:requirements")` |
| `leadership` | Master stakeholder management, executive communication, cros | `Skill("product-manager-assistant:leadership")` |
| `analytics` | Master metrics definition, KPI tracking, dashboarding, A/B t | `Skill("product-manager-assistant:analytics")` |
| `strategy` | Master product strategy, market analysis, competitive positi | `Skill("product-manager-assistant:strategy")` |

---

## ⌨️ Commands

| Command | Description |
|---------|-------------|
| `/launch` | Product Launch Planning & Execution |
| `/roadmap` | Product Roadmap Planning |
| `/start` | Start Your Product Manager Journey |
| `/discover` | User Discovery & Research Guide |

---

## 📚 Documentation

| Document | Description |
|----------|-------------|
| [CHANGELOG.md](CHANGELOG.md) | Version history |
| [CONTRIBUTING.md](CONTRIBUTING.md) | How to contribute |
| [LICENSE](LICENSE) | License information |

---

## 📁 Project Structure

<details>
<summary>Click to expand</summary>

```
custom-plugin-product-manager/
├── 📁 .claude-plugin/
│   ├── plugin.json
│   └── marketplace.json
├── 📁 agents/              # 8 agents
├── 📁 skills/              # 12 skills (Golden Format)
├── 📁 commands/            # 4 commands
├── 📁 hooks/
├── 📄 README.md
├── 📄 CHANGELOG.md
└── 📄 LICENSE
```

</details>

---

## 📅 Metadata

| Field | Value |
|-------|-------|
| **Version** | 1.0.0 |
| **Last Updated** | 2025-12-29 |
| **Status** | Production Ready |
| **SASMP** | v1.3.0 |
| **Agents** | 8 |
| **Skills** | 12 |
| **Commands** | 4 |

---

## 🤝 Contributing

Contributions are welcome! Please read our [Contributing Guide](CONTRIBUTING.md).

1. Fork the repository
2. Create your feature branch
3. Follow the Golden Format for new skills
4. Submit a pull request

---

## ⚠️ Security

> **Important:** This repository contains third-party code and dependencies.
>
> - ✅ Always review code before using in production
> - ✅ Check dependencies for known vulnerabilities
> - ✅ Follow security best practices
> - ✅ Report security issues privately via [Issues](../../issues)

---

## 📝 License

Copyright © 2025 **Dr. Umit Kacar** & **Muhsin Elcicek**

Custom License - See [LICENSE](LICENSE) for details.

---

## 👥 Contributors

<table>
<tr>
<td align="center">
<strong>Dr. Umit Kacar</strong><br/>
Senior AI Researcher & Engineer
</td>
<td align="center">
<strong>Muhsin Elcicek</strong><br/>
Senior Software Architect
</td>
</tr>
</table>

---

<div align="center">

**Made with ❤️ for the Claude Code Community**

[![GitHub](https://img.shields.io/badge/GitHub-pluginagentmarketplace-black?style=for-the-badge&logo=github)](https://github.com/pluginagentmarketplace)

</div>
