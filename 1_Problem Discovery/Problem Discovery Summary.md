# Problem Discovery Summary

## Background

The project initiator (myself) experienced real difficulties while preparing for the Microsoft AI-901 (Azure AI Fundamentals) certification exam using multiple AI tools. Existing general-purpose AI learning tools have systematic shortcomings in the certification preparation scenario.

## Investigation Method

- First-hand experience with ChatGPT, Claude, Google Gemini, NotebookLM
- Cross-checked AI outputs against the official Microsoft AI-901 syllabus
- Documented friction points during the learning process

## Key Findings

| # | Finding |
|---|---------|
| 1 | AI responses deviate from official syllabus in scope, terminology, and level of detail |
| 2 | NotebookLM auto-searches sources, potentially including unofficial guides, outdated content, or unreliable materials |
| 3 | Even when given official URLs, NotebookLM cannot distinguish main content from web page clutter (navigation bars, ads, sidebars) |
| 4 | Official learning materials are well-structured but scattered across multiple pages; retrieving a specific topic is inconvenient |
| 5 | User workflow becomes: ask AI → doubt → verify against official sources → double effort |

## User Behavior Pattern

- Verification impulse is **triggered sporadically** — when a concept feels "fuzzy" in memory
- **Friction cost** at that moment determines behavior: high friction → skip verification → fuzzy knowledge persists
- The core problem is the **gap between "the moment a question arises" and "receiving a confirmed answer"**

## Root Cause

> General-purpose AI tools are not designed to understand "certification exam syllabus" as a concept — including its knowledge structure, scope boundaries, terminology standards, and depth requirements. Therefore, they cannot teach official content the way the official syllabus defines.

## Core Contradiction

| Aspect | User Need | What Current Tools Provide |
|--------|-----------|---------------------------|
| Knowledge Source | Official syllabus as single source of truth | Auto-search, source uncontrollable |
| Knowledge Structure | Organized by official syllabus hierarchy | AI-generated, not aligned with syllabus |
| Content Parsing | Correctly parse official page content | Cannot distinguish body from clutter |
| Verification Cost | One-click topic retrieval | Manual page-by-page search |
