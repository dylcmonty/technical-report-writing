---
status: draft
audience: [technical]
tags: [workbench, staging, transactions, mycite]
related: [0000-00-00-description-mycite_framework, 2024-00-00-description-control_deck]
---

# Declarative transaction workbench

## Retrieval Gist

What is the right mental model for the script-backed workbench surface?

## Description

The right model is a declarative transaction workbench, not a conventional form UI.

A user stages intended changes in a temporary declarative layer, reviews the computed effect, and only then applies those changes to the authority surface. The closest analogies are Git staging and Terraform plan/apply: the staged file is not authority by itself, but a controlled pending-change layer that can be diffed, validated, and committed.

That model keeps the interface script-backed and inspectable while still giving the user a readable way to work with structured changes, raw-versus-projected views, and durable validation rules.
