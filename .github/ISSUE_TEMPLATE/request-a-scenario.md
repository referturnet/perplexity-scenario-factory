---
name: Request a scenario
description: Suggest a new Perplexity automation scenario for the catalog
labels: [scenario-request]
title: '[Scenario Request] '
body:
- type: textarea
  id: goal
  attributes:
    label: What should the scenario accomplish?
    description: One or two sentences describing the research or automation outcome.
  validations:
    required: true
- type: input
  id: domain
  attributes:
    label: Domain
    description: e.g. competitor research, sourcing, SEO, due diligence
  validations:
    required: true
- type: textarea
  id: context
  attributes:
    label: Example prompt you would use today
    description: Optional — helps us design the scenario structure.
  validations:
    required: false
