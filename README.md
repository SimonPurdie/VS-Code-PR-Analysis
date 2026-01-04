# Analysing Pull Request Trends in VS Code (2022–2025)

## Overview

This project examines the evolution of Pull Request (PR) activity in the [microsoft/vscode](https://github.com/microsoft/vscode) repository - one of the world's largest and most active open-source projects - from May 2022 through December 2025.

The goal is simple: **visualise how the rise of AI-assisted coding tools has impacted contribution patterns in a major open-source project.**

The data tells a compelling story. As autonomous coding agents became publicly available in mid-2025, VS Code saw a dramatic surge in PR submissions. But more PRs didn't necessarily mean more merged code. The merge success rate dropped sharply even as review times improved, suggesting that the VS Code maintainers' quality bar held firm against the flood of AI-generated contributions.

---

![VS Code PR Analysis Dashboard](images/VS%20Code%20PRs%20Visualisation%204k.png)


## Key Findings

### 1. The 2025 Agentic AI Surge

![PR Submission Rate Chart](images/pr%20submission%20rate.png)

*Pull Requests submitted for merge (May 2022 – Dec 2025)*

Some major milestones in the introduction of AI-assisted coding tools are marked on the visualisation. The original GitHub Copilot (June 2022) brought sophisticated autocompletion. Following ChatGPT's release (November 2022), Copilot X (March 2023) was introduced, bringing LLM integration to the development environment.

The chart above shows VS Code's monthly PR volume sustaining modest growth throughout the period following the adoption of that generation of AI coding tools.

Everything changed in **May 2025** with the public preview of the **Copilot Coding Agent** - an autonomous tool capable of writing and submitting pull requests with minimal human oversight. From the period following that release, to the beginning of December 2025, the monthly PR submissions went from ~780 to ~1,400 - an increase of ~79% in 7 months.

---

### 2. Merge Success Rate Drops

![PR Merge Success Rate Chart](images/pr%20merge%20success.png)

*Percentage of Pull Requests successfully merged (May 2022 – Dec 2025)*

While volume surged, success rate told a different story.

For three years, the VS Code project maintained a high and stable merge rate. Contributors - largely experienced developers - submitted PRs that met the project's standards.

The **mid-2025 inflection point** changed that. As autonomous agents began generating and submitting pull requests at scale, the percentage of PRs successfully merged began a sustained decline.

This suggests that while AI agents dramatically increased *output volume*, much of that output was **rejected or closed** by maintainers.

---

### 3. Time-to-Merge Improved

![Average Days to Merge Chart](images/average%20days%20to%20merge.png)

*Average days from PR submission to merge (May 2022 – Dec 2025)*

Perhaps the most surprising finding: Far from being overwhelmed, the VS Code review pipeline became *more* efficient.

Starting in late 2024, time-to-merge entered a sustained downward trend. By the height of the 2025 AI surge, high-quality PRs were being merged faster than ever.

---

### 4. Market Share Context

![VS Code Market Share Chart](images/approx%20market%20share.png)

*VS Code approximate market share from Stack Overflow Developer Surveys (2021–2025)*

To help provide context of VS Code's dominance in the IDE market, and rule out the hypothesis that PR surges were driven by any changes in its popularity, data is cross-referenced data from the annual **Stack Overflow Developer Surveys**.

VS Code's approximate market share remained **stable** throughout the study period, with its usage fluctuating only a few percentage points around ~74% of all participants. The 2025 PR surge cannot be attributed to a sudden influx of new VS Code users or a viral adoption event.

---

### Closing Notes

This analysis examines one repository during a specific period, but the underlying question extends well beyond VS Code: how are software development workflows affected when AI agents can autonomously generate and submit code at scale?
The data here captures an early snapshot of that shift. The patterns visible in these charts - increased output volume, maintained quality standards, adapted review processes - are playing out across the software industry in different forms.

---

## Data & Methodology

### Data Collection

PR data was extracted directly from the **GitHub GraphQL API** using custom Python scripts. The extraction covered all pull requests in the `microsoft/vscode` repository from May 2022 through December 2025.

The data collection tooling is maintained in a separate repository:
**[SimonPurdie/PR-Scraper](https://github.com/SimonPurdie/PR-Scraper)**

### Data Sources

- **GitHub GraphQL API** [https://docs.github.com/en/graphql](https://docs.github.com/en/graphql)
- **Stack Overflow Developer Survey** [https://survey.stackoverflow.co/](https://survey.stackoverflow.co/)

---

## License

Unless otherwise noted, the contents of this repository - including collected data, analysis artifacts, BI project files, and generated visualisations - are licensed under the MIT [License](LICENSE).

Third-party data used in this project is governed by its respective licenses and terms, including GitHub’s Terms of Service and Stack Overflow’s data usage policies.

---

*Analysis by [Simon Purdie](https://github.com/SimonPurdie) • Data collected December 2025*
