# Prizmatic
Created by Jeongmin Sohn and Heejoon Yi

## Overview
**Prizmatic** is a web-based, AI-assisted project management platform designed for individual developers and small software development teams.
The platform combines workspace collaboration, project and Work Item management, sprint planning, GitHub integration, and an AI project manager. Work Items represent tasks, features, bugs, or other units of project work. Its goal is to reduce the manual coordination required to organize software projects so developers can focus more on implementation.

## Problem
Small development teams often operate without a dedicated project manager. As a result, developers must organize tasks, assign work, manage sprints, track progress, and review code while also completing their development responsibilities.

Existing tools such as `Jira` and `Notion` help teams organize project information, but planning decisions and workflow maintenance still require significant manual effort. This burden can reduce development productivity, especially in small teams where each member's contribution is critical.

## Solution
Prizmatic provides a centralized platform where teams can manage workspaces, projects, Work Items, assignments, priorities, schedules, sprints, comments, documents, and notifications.

The AI project manager uses project and workspace context to:

* Decompose features into structured parent and child Work Items
* Refine project backlogs
* Detect duplicate or similar Work Items
* Recommend or apply Work Item assignments
* Assist with sprint planning and project-risk analysis
* Record Agent runs, execution steps, and completed actions

Through GitHub integration, Prizmatic can identify relevant Work Item context from pull request titles and automatically trigger AI-assisted reviews for supported pull request events. The review system analyzes code changes and publishes review summaries and line-specific feedback directly to GitHub.

By combining project management workflows with AI-assisted planning and code review, Prizmatic reduces manual coordination work while allowing team members to inspect and manage the resulting actions.

## Core Capabilities
* Workspace, member, role, and invitation management
* Project dashboards and hierarchical Work Item management
* Work Item assignments, priorities, schedules, comments, and documents
* Workspace-level sprint planning and progress tracking
* Real-time notifications and workspace updates
* AI-assisted feature decomposition, backlog refinement, and task assignment
* Agent run history, execution graphs, and action tracking
* GitHub repository integration and automated AI pull request reviews

## System Components
| Component      | Description                                                     |
| -------------- | --------------------------------------------------------------- |
| `prism-nextjs` | Next.js frontend for the Prizmatic web application              |
| `prism-nestjs` | NestJS backend API and application services                     |
| `prism-agent`  | Event-driven AI project manager and pull request review runtime |
| `prism-vector` | Vector embedding processing worker                              |
| `prism-admin`  | Administrative dashboard                                        |

## Technology Overview
* **Frontend:** Next.js, React, TypeScript, Tailwind CSS, TanStack Query
* **Backend:** NestJS, TypeScript, PostgreSQL, TypeORM
* **AI and Search:** Python, LLM-based Agent workflows, pgvector embeddings
* **Integrations:** GitHub App, GitHub webhooks, OCI Queue, OCI Object Storage, OCI Email Delivery
* **Deployment:** Vercel, Docker, OCI Compute, GitHub Actions

## Future Direction
Prizmatic currently supports an AI-assisted development cycle in which the AI project manager creates and assigns work, team members complete the work, and the AI reviews related pull requests before assisting with subsequent planning.

Future development will focus on improving Agent accuracy, performance, approval controls, and user experience. The team also plans to explore integration with AI coding workers such as Codex and Claude through the Model Context Protocol (MCP), allowing human and AI contributors to collaborate within the same workspace.

## Live Demo
https://dev.prizmatic.app
