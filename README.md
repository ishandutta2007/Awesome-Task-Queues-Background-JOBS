# Awesome-Task-Queues-Background-JOBS

# Top Task & To-Do Management Tools Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Self-Hosted Sovereignty, GTD Workflows & Time Tracking Integration*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Task & To-Do Management**. These tools help individuals and teams capture, organize, and complete tasks — with options ranging from polished commercial suites to fully self-hosted platforms that keep your task data on your own infrastructure.

**Examples** include Todoist, Asana, Microsoft To Do, Any.do, TickTick, Things, OmniFocus, Remember The Milk, Habitica, and Toodledo (the category leaders).

**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, data ownership, and transparent development — ideal for users prioritizing privacy, avoiding per-seat subscription pricing, and maintaining full control over their task data.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[Todoist](https://todoist.com/)**  
  The reference point for cross-platform task management — natural language parsing, projects, labels, filters, and Karma gamification. Free tier limited to 5 active projects. Pro at **$5/month** (annual) adds reminders, filters, and themes. Templates and integrations are strengths.

- **[Asana](https://asana.com/)**  
  Team-oriented work management platform with projects, tasks, timelines, and portfolios. Free tier for up to 10 users. Paid plans scale per-user with advanced reporting and automation.

- **[Microsoft To Do](https://to-do.office.com/)**  
  Microsoft's task manager integrated with Microsoft 365. Free with a Microsoft account. My Day view, smart suggestions, and Outlook integration. Simple and clean, best for individual task tracking within the Microsoft ecosystem.

- **[TickTick](https://ticktick.com/)**  
  Feature-rich task manager with calendar, pomodoro timer, habit tracking, and Eisenhower matrix. Free tier is generous; Premium at **$35.99/year** adds calendar view, smart lists, and more.

- **[Things](https://culturedcode.com/things/)**  
  Premium macOS/iOS task manager known for its polished design and GTD-friendly workflows. One-time purchase per platform. No web or Android version.

- **[OmniFocus](https://www.omnigroup.com/omnifocus/)**  
  Power-user GTD task manager for Apple platforms. Deep customization with perspectives, forecast views, and automation. Premium pricing reflects its pro focus.

- **[Remember The Milk](https://www.rememberthemilk.com/)**  
  Long-standing task manager with smart lists, tags, and cross-platform sync. Free tier with limited smart lists; Pro at **$39.99/year**.

- **[Habitica](https://habitica.com/)**  
  Gamified task manager that turns your to-do list into an RPG. Complete tasks to earn XP and gold, build habits, and join parties for accountability.

- **[Toodledo](https://www.toodledo.com/)**  
  Customizable task manager with outlines, notes, lists, and collaboration features. Free tier with limits; paid plans for advanced features.

## Open-Source GitHub Projects

- **[Vikunja](https://github.com/go-vikunja/vikunja)**  
  **The leading open-source, self-hostable task management platform** — AGPLv3 licensed, backed by a bootstrapped team that prioritizes users over VC interests [citation:1]. **Four task views**: List, Kanban, Gantt, and Table — switch between them instantly based on your workflow [citation:6][citation:19]. **Powerful features** including recurring tasks, subtasks, priorities, labels, reminders, task relations (blocking/blocked by/related), CalDAV integration, and a powerful filter query language for smart views [citation:15][citation:19]. **Real-time collaboration** via WebSockets for instant updates across clients [citation:19]. **Universal import** from Todoist, Trello, TickTick, Microsoft To-Do, WeKan, and generic CSV [citation:1][citation:19]. **Deployment**: Docker with SQLite for simple setups or PostgreSQL for production [citation:14]. Also available as managed **Vikunja Cloud** starting at €4/month for users who prefer not to self-host [citation:17]. **Limitations**: Native mobile apps are still in active development — PWA and third-party Android apps via CalDAV are common workarounds [citation:17][citation:19]. No built-in time tracking [citation:6].

- **[Super Productivity](https://github.com/johannesjo/super-productivity)**  
  **The most feature-complete open-source alternative combining task management with time tracking** — replaces TickTick AND Toggl in one app [citation:4]. **Project-based task management** with subtasks (one level deep, deliberately limited to avoid over-nesting), descriptions, attachments, and tags [citation:4]. **Built-in time tracking** on every task with estimated vs actual time comparison, manual time entry, and a time tracking reminder that prompts you when you haven't tracked anything [citation:4]. **Today view, Scheduled calendar view, and Planner Kanban view** for different planning horizons [citation:4]. **Global keyboard-centric task capture** with syntax for +project, #tag, and @due date [citation:4]. **Habit tracking** with built-in counters (standing desk timer, coffee counter, stretch reminders) and custom trackers [citation:4]. Free and open-source.

- **[Jotter](https://github.com/simon123h/jotter)**  
  **Local-first, privacy-focused task management storing everything as plain-text Markdown files** — your data remains fully accessible even if you stop using Jotter [citation:5][citation:7]. **Markdown Kanban board** with flexible views: Kanban columns, list view, Eisenhower Matrix, and chronological Time View [citation:5]. **Git-backed sync** with selective per-project remotes — keep "Home" local while sharing "Work" with a team [citation:5]. **Git Time Machine** for rolling back to any historical snapshot, with automatic pre-restore backups [citation:5]. **MCP support** for connecting AI assistants directly to your local Kanban board [citation:5]. **Obsidian & PKM native** with index.md manifests [citation:5]. **Android app** operating 100% offline with local Markdown files [citation:5]. Install via `pipx run jotter-app` or standalone executables [citation:5]. **Limitations**: No built-in time tracking [citation:5].

- **[Planify](https://github.com/alainm23/planify)**  
  **Modern GTK4 task manager for Linux** with Todoist sync support [citation:2]. **CalDAV improvements** including Nextcloud integration [citation:2]. **Todoist API migration** with mandatory re-login flow to ensure continued sync support [citation:2]. **CLI interface** introduced in 4.18.3 [citation:2]. **Asterisk prefix for incompletable tasks (notes)** compatible with Todoist [citation:2]. Best for Linux desktop users wanting native GTK integration with Todoist sync.

- **[Mimrai](https://github.com/mimrai-org/mimrai)**  
  **Early-stage open-source task management** positioned as a lightweight alternative to Jira, Asana, Linear, and Monday.com [citation:3]. **Modern TypeScript stack**: Turborepo, Bun, React, Next.js, Supabase, Tailwind CSS, Shadcn UI [citation:3]. **AGPL-3.0 for non-commercial use** — commercial deployments require a commercial license [citation:3]. **Status**: "Evolving project, currently in its early stages of development" [citation:3]. Not yet recommended for production use.

- **[Alkonost](https://github.com/szholobetsky/alkonost)**  
  **Plain-text Kanban board with everything stored in a checklist file** you can open in any text editor, back up, or version control [citation:10]. **Full task descriptions** rendered as real formatted text — headings, tables, formulas, diagrams — with live preview editing [citation:10]. **Tags, modules, people, and urgent flags** as clickable filters [citation:10]. **Board and backlog views** — show only active statuses on the board while keeping everything accessible in the backlog table [citation:10]. **Multi-project support** — point at a folder and switch between boards [citation:10]. **Autosave and eight color themes** [citation:10]. Install via `pip install alkonost`. **Limitations**: No sync across devices built-in (file-based); no mobile app.

- **[Donetick](https://github.com/donetick/donetick)**  
  **Self-hostable task manager focused on household chores and shared lists** — designed to be shared with household members [citation:12]. **Gamification with points** for completed chores, redeemable for rewards — great for families with kids [citation:12]. **Flexible due dates and automation**: repeat at custom intervals, schedule from completion date, auto-assign based on least completed tasks, and "Things" triggers [citation:12]. **Circle system** for shared task management with household members [citation:12]. **Dashboard view** separate from work tasks to avoid notification fatigue [citation:12]. **Pushover integration** for notifications, PWA support for mobile, and Home Assistant add-on availability [citation:12]. **Limitations**: Setup requires some self-hosting familiarity; Android app requires HTTPS for connection [citation:12].

- **[Mindwtr](https://apps.apple.com/cn/app/mindwtr/id6758597144)**  
  **Free, open-source GTD task manager for Apple platforms** — offline-first with no account required [citation:8]. **Full GTD methodology**: Inbox, Next Actions, Waiting For, Someday/Maybe, Projects, Areas, Contexts, and Weekly Review [citation:8]. **Flexible sync options**: Dropbox, your own folder, WebDAV, your own server, or iCloud — you decide where data lives [citation:8]. **Import from Todoist, TickTick, and OmniFocus** [citation:8]. **Views**: List, Calendar, and Kanban [citation:8]. **Features**: reminders, repeating tasks, checklists, Markdown notes, and attachments [citation:8]. **Optional AI assistant** using your own AI account [citation:8]. **Limitations**: Apple platforms only (iOS, iPadOS, macOS, visionOS, watchOS) [citation:8].

- **[Tasks.org](https://github.com/tasks/tasks)**  
  **Open-source, privacy-focused Android task manager** — no ads, no location tracking [citation:18]. **Powerful features**: unlimited nesting of subtasks, drag-and-drop reordering, location-based reminders, and highly customizable widgets [citation:18]. **Sync options**: Tasks.org Cloud, Google Tasks, DAVx⁵ (CalDAV), Microsoft To Do, EteSync, DecSync CC, or fully offline [citation:18]. **Nextcloud Tasks and Apple Reminders compatibility** [citation:18]. **Tasker integration** for automation, Wear OS support, and automatic backups [citation:18]. **Limitations**: Android only; no web or desktop native app.

### Additional Strong Open-Source Options

- **Focalboard** — Open-source, self-hosted alternative to Trello, Notion, and Asana. Kanban boards, table views, and gallery layouts. Built-in content calendar templates [citation:11][citation:16].
- **OpenProject** — Comprehensive open-source project management with Gantt charts, agile boards, and team collaboration features [citation:11].
- **Nextcloud Tasks** — Task management integrated with Nextcloud file storage and collaboration suite. CalDAV sync with Tasks.org and other clients.

**Frameworks for building custom systems**: Combine **Vikunja** for full-featured self-hosted task management with Gantt and Kanban views, **Super Productivity** for task management with built-in time tracking and habit tracking, **Jotter** for local-first Markdown-based tasks with Git sync, and **Tasks.org** for Android-side capture and location reminders — to build a complete self-hosted task management ecosystem tailored to your workflow.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Task management tools differ significantly in deployment complexity, feature scope, and data ownership model. **Vikunja is the most feature-complete self-hosted option** but requires a database and API backend, making it heavier than flat-file alternatives [citation:19]. **Jotter stores tasks as plain Markdown files** — maximum portability but no built-in mobile app sync beyond Git [citation:5]. **Super Productivity's subtask depth is deliberately limited to one level** to avoid over-organization [citation:4]. Self-hosting shifts operational responsibility to you — backups, updates, and access management are your concern.
- Self-hosted open-source solutions require proper security hardening, backup strategies, and ongoing maintenance.

---

**Made for productivity enthusiasts, self-hosters, teams, and developers building task management platforms.**  
Let's make task management more open, private, and workflow-friendly.
