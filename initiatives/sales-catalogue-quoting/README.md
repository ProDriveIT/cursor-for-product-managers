# Sales catalogue quoting

**Agent name:** Service Catalogue Quoting Assistant

**Status:** In Progress  
**Timeline:** 22 Oct 2026 — end date not set  
**Owner:** Dan  
**Stakeholders:** Bruce Penson (Visionary, Sales & Marketing)

## 🎯 Initiative Goal

Give the Pro Drive sales team a Copilot agent that quotes services from the live IT Glue SC:020 catalogue. One question can name more than one service. Each answer comes from that service’s own guide. The agent does not invent a time or a fee, and it does not keep a copy of the catalogue.

**Why it matters:** Sales need a fast quote without a second price list. The guide in IT Glue stays the source. This supports product-map goal **B** (sell services to existing clients) by making those services quotable. It is an internal sales tool, not a client SKU. Current-quarter OKRs are not written yet (`company-level-context/okrs/README.md`).

**Out of this product:** The Cursor skill `sc020-quote` is James’s own reader. It is not the sales product and it is not what Dan builds.

## 📊 Current Status

- [ ] User Research Complete
- [ ] Opportunities Identified
- [ ] PRD Drafted
- [ ] Tasks Generated
- [x] Development Started
- [ ] Analytics Setup Complete

Development means the agent is quoting from the live catalogue (proved 22–23 Oct 2026 on Datto SaaS backup and Datto Secure Edge). Dan’s click guide is the task list. A product PRD is not written yet.

## 🗂️ Folder Structure

- **[user-interviews/](./user-interviews/)** - Customer discovery and research
  - `snapshots/` - Individual interview insights using `/create-interview-snapshots`
  - `synthesis/` - Cross-interview analysis and patterns
  - `transcripts/` - Raw interview recordings and notes
- **[opportunities/](./opportunities/)** - Identified opportunities and pain points
- **[assumptions/](./assumptions/)** - Assumption logs and test cards from `/identify-test-assumptions`
- **[solutions/](./solutions/)** - Solution explorations from `/generate-solutions`
- **[design/](./design/)** - Design briefs and Figma prompts from `/create-design-brief` and `/generate-figma-prompt`
- **[prototype/](./prototype/)** - Working prototype and companion doc from `/build-prototype`
- **[product-analytics/](./product-analytics/)** - Data analysis and metrics
- **[prd/](./prd/)** - Product Requirements Document using `/create-prd`
- **[tasks/](./tasks/)** - Implementation tasks using `/generate-tasks`

## 🔗 Quick Links

- [1-pager for Bruce](./prd/1-pager-sales-catalogue-quoting.md) (draft, 23 Oct 2026)
- [PRD](./prd/)
- [User Research Summary](./user-interviews/synthesis/)
- [Priority Opportunities](./opportunities/)
- [Assumptions & Tests](./assumptions/)
- [Solution Explorations](./solutions/)
- [Prototype & Companion Doc](./prototype/)
- [Implementation Tasks](./tasks/)
- [Dan’s build guide](file:///C:/GitHub-Repos/10%20Projects/2026-09%20agent-ecosystem-copilot/04-build-guides/Build-Sales-Catalogue-Quoting-Agent.md)
- [Company context](../../company-level-context/prodrive-context.md)
- [Product map](../../company-level-context/product-vision-and-strategy/product-map.md)

## 📝 Notes

The agent is **Service Catalogue Quoting Assistant**. Sales ask in Copilot. One flow, Get-SC020, calls the quote function. The function reads IT Glue. The agent writes a summary table, then one section per service.

Rules already in force:

- Live read every question. No knowledge file and no spreadsheet copy.
- SC:020 only. One document per service. Do not blend documents.
- If time, fees, where, who, discovery questions, or the Service Specification are missing, say so and give the guide name, link, and updated time.
- The Service Specification is the only wording that can be sent to a client.
- Sales only. Do not publish the agent to the whole company.
- Dan holds a function key. He does not hold the IT Glue key.

The quote function and Dan’s guide already exist. This folder is the product record. Do not move the Cursor skill into it.

---
*Created using initiatives template. Use `/setup-initiative` for new initiatives.*
