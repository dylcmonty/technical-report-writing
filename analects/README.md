# Analects

Normalized leaf notes now live directly in this directory. The direct files that previously sat at `analects/raw/<file>` were converted to markdown, renamed under a single convention, and moved here. Nested raw collections such as `raw/technical/` and `raw/corespond/` remain in place for later normalization work.

## Layout

- `analects/*.md` stores the normalized single-file note collection.
- `analects/raw/_template.snippet.md` stores the starter template for future normalizations.
- `analects/raw/catalog.json` stores the machine-readable classification inventory for the current collection state.
- `analects/raw/technical/` and `analects/raw/corespond/` remain as nested source collections that were not part of this pass.
- `analects/archive/` remains archival reference material.

## Filename Convention

```text
YYYY-MM-DD-<slug_convention>-<name>.md
```

Rules applied in this pass:

- Use `0000-00-00` when no date is known.
- Preserve partial dates by leaving unknown month/day positions as `00`.
- Normalize `<slug_convention>` and `<name>` so their internal separators are underscores.
- Use the literal placeholder `slug` when a stable classification slug is not obvious from the source file.
- Keep the date and the two filename segments separated by hyphens.

Examples:

- `0000-00-00-company_description-fnd.md`
- `2026-04-21-business-or_area_focus.md`
- `0000-00-00-slug-founder_about.md`

## Unified Front Matter Template

```md
---
title: ""
date: "0000-00-00"
slug_convention: "slug"
name: "example_name"
classification: "slug"
status: ""
kind: ""
source_path: ""
audience: []
tags: []
source_type: ""
source_ref: ""
related: []
summary: ""
---
```

Each normalized note keeps its source path in front matter so the migration back to `raw/` remains traceable.

## Current Classification Summary

| Classification | Count |
| --- | ---: |
| `boundary` | 2 |
| `business` | 3 |
| `claim` | 3 |
| `company_approach` | 4 |
| `company_description` | 3 |
| `company_problem` | 1 |
| `company_purpose` | 2 |
| `constraint` | 1 |
| `control` | 2 |
| `education` | 2 |
| `experience` | 5 |
| `fnd` | 2 |
| `governance` | 1 |
| `identity_framing` | 1 |
| `leadership_and_involvement` | 5 |
| `literary` | 3 |
| `market` | 1 |
| `measure` | 2 |
| `mechanism` | 5 |
| `metric` | 1 |
| `motivation_framing` | 1 |
| `objective` | 3 |
| `phase_i` | 3 |
| `ponderence` | 2 |
| `problem` | 6 |
| `product_service_or_solution` | 2 |
| `research` | 3 |
| `scope` | 1 |
| `slug` | 45 |
| `source` | 6 |
| `technical` | 2 |
| `technology` | 1 |
| `technology_case` | 1 |
| `technology_comparison` | 1 |
| `technology_description` | 1 |
| `transition` | 1 |

## Current Classification Inventory

### `boundary` (2)

`0000-00-00-boundary-phase_i_is_not_agronomic_optimization.md`, `2026-00-00-boundary-website_hosting_is_the_wedge_not_the_innovation.md`

### `business` (3)

`2026-04-21-business-operating_design.md`, `2026-04-21-business-or_area_focus.md`, `2026-04-23-business-support_interest.md`

### `claim` (3)

`0000-00-00-claim-local_agriculture_is_increasingly_inequitable.md`, `0000-00-00-claim-transitional_feasibility_two_sided_viability.md`, `0000-00-00-claim-unrealized_farm_value_through_planning_confidence.md`

### `company_approach` (4)

`0000-00-00-company_approach-fnd_cvcc_relationship.md`, `0000-00-00-company_approach-fnd_ownership_model.md`, `0000-00-00-company_approach-open_standard_best_interface_model.md`, `0000-00-00-company_approach-trustless_coordination_without_central_authority.md`

### `company_description` (3)

`0000-00-00-company_description-cvcc.md`, `0000-00-00-company_description-fnd.md`, `0000-00-00-company_description-trapp_family_farm.md`

### `company_problem` (1)

`0000-00-00-company_problem-agriculture_as_community_root.md`

### `company_purpose` (2)

`0000-00-00-company_purpose-fnd_strategic_thesis.md`, `2025-04-00-company_purpose-pitch_statement.md`

### `constraint` (1)

`0000-00-00-constraint-two_sided_feasibility_window.md`

### `control` (2)

`2024-00-00-control-deck.md`, `2024-00-00-control-gate.md`

### `education` (2)

`2026-00-00-education-hudson_high_school.md`, `2026-00-00-education-university_of_akron.md`

### `experience` (5)

`2026-00-00-experience-founder_and_developer.md`, `2026-00-00-experience-icorps_national_science_foundation.md`, `2026-00-00-experience-lake_forest_country_club.md`, `2026-00-00-experience-political_campaigns.md`, `2026-00-00-experience-stanley_black_decker.md`

### `fnd` (2)

`0000-00-00-fnd-who_is_buying_services.md`, `2025-02-25-fnd-target_customer.md`

### `governance` (1)

`0000-00-00-governance-shared_interpretability_without_central_authority.md`

### `identity_framing` (1)

`0000-00-00-identity_framing-small_farm_operational_independence.md`

### `leadership_and_involvement` (5)

`2026-00-00-leadership_and_involvement-akron_hillel.md`, `2026-00-00-leadership_and_involvement-big_brother_big_sister_charity_volunteering.md`, `2026-00-00-leadership_and_involvement-university_of_akron_nhs.md`, `2026-00-00-leadership_and_involvement-university_of_akron_zipcode_club.md`, `2026-00-00-leadership_and_involvement-zips_electric.md`

### `literary` (3)

`2025-02-25-literary-what_is_my_place.md`, `2026-01-16-literary-morning_passage.md`, `2026-04-17-literary-dylan_proverb.md`

### `market` (1)

`0000-00-00-market-food_hubs_help_but_do_not_remove_structural_pressures.md`

### `measure` (2)

`0000-00-00-measure-impact.md`, `0000-00-00-measure-of_success.md`

### `mechanism` (5)

`0000-00-00-mechanism-coordination_can_compress_overhead.md`, `0000-00-00-mechanism-cyclical_reinvestment_loop.md`, `0000-00-00-mechanism-demand_certainty_creates_a_reinforcement_loop.md`, `0000-00-00-mechanism-fixed_constants_and_dynamic_variables_in_phase_i_model.md`, `0000-00-00-mechanism-unsold_output_is_a_planning_constraint.md`

### `metric` (1)

`0000-00-00-metric-farm_income_volatility_is_the_focused_axis.md`

### `motivation_framing` (1)

`0000-00-00-motivation_framing-driven_approach.md`

### `objective` (3)

`0000-00-00-objective-phase_i_feasibility_claim_structure.md`, `0000-00-00-objective-the_project_needs_one_decisive_feasibility_claim.md`, `0000-00-00-objective-transitional_feasibility_is_the_real_question.md`

### `phase_i` (3)

`2026-00-00-phase_i-feasibility_constraint_counterparty_condition.md`, `2026-00-00-phase_i-feasibility_study.md`, `2026-00-00-phase_i-scope.md`

### `ponderence` (2)

`2025-00-00-ponderence-personal_literary_reflection_faith_glimmer_therefore_faith.md`, `2025-00-00-ponderence-personal_literary_reflection_providence.md`

### `problem` (6)

`0000-00-00-problem-being_solved_and_for_whom.md`, `0000-00-00-problem-business_solves.md`, `0000-00-00-problem-consumer_interest_does_not_become_local_advantage.md`, `0000-00-00-problem-coordination_burden_is_the_immediate_failure_mode.md`, `0000-00-00-problem-driven_builder.md`, `0000-00-00-problem-local_agriculture_is_constrained_by_structure.md`

### `product_service_or_solution` (2)

`0000-00-00-product_service_or_solution-market.md`, `0000-00-00-product_service_or_solution-uniqueness.md`

### `research` (3)

`0000-00-00-research-description.md`, `0000-00-00-research-potential_applications.md`, `0000-00-00-research-scientific_impact.md`

### `scope` (1)

`0000-00-00-scope-deep_mss_formalism_is_not_core_byte_material.md`

### `slug` (45)

`0000-00-00-slug-creativity_and_practicality.md`, `0000-00-00-slug-different_than_competitors.md`, `0000-00-00-slug-dylan_montgomery_impulse_to_build.md`, `0000-00-00-slug-dylan_montgomery_personal_passion.md`, `0000-00-00-slug-dylan_montgomery_working_mindset.md`, `0000-00-00-slug-founder_about.md`, `0000-00-00-slug-fruitful_network_development.md`, `0000-00-00-slug-how_i_got_into_computer_science.md`, `0000-00-00-slug-if_i_could_solve_a_problem_today.md`, `0000-00-00-slug-improvisational_technical_work.md`, `0000-00-00-slug-innovation_summary.md`, `0000-00-00-slug-learning_what_i_didnt_know.md`, `0000-00-00-slug-message_anecdote.md`, `0000-00-00-slug-mss_novelty.md`, `0000-00-00-slug-multifaceted_pursuit.md`, `0000-00-00-slug-new_tasks.md`, `0000-00-00-slug-non_technical_description.md`, `0000-00-00-slug-onboarding_instructions.md`, `0000-00-00-slug-participate_motivation.md`, `0000-00-00-slug-peronal_lines_fragments_metacognition.md`, `0000-00-00-slug-peronal_lines_fragments_problems.md`, `0000-00-00-slug-peronal_lines_fragments_want.md`, `0000-00-00-slug-potential_commercial_impact.md`, `0000-00-00-slug-primordial_curiosity.md`, `0000-00-00-slug-purposeful_and_forward_moving.md`, `0000-00-00-slug-relevant_team_experience.md`, `0000-00-00-slug-scientific_fields.md`, `0000-00-00-slug-software_technical_definition_and_description.md`, `0000-00-00-slug-success_criteria.md`, `0000-00-00-slug-team_vision_execution_qualifications.md`, `0000-00-00-slug-unique_innovative.md`, `0000-00-00-slug-weaknesses.md`, `2025-00-00-slug-biography.md`, `2025-00-00-slug-customer_facing_development.md`, `2025-00-00-slug-dylan_montgomery_linkedin.md`, `2025-00-00-slug-icorps_nsf_funded_agricultural_research.md`, `2026-00-00-slug-architecture_defensible_primitive_for_novelty.md`, `2026-00-00-slug-civic_problem_solution.md`, `2026-00-00-slug-dylan_montgomery_hacking_a_non_computer.md`, `2026-00-00-slug-local_agronomic_framing_solution_fit.md`, `2026-00-00-slug-post_icorps_progress.md`, `2026-04-21-slug-anticipated_support_use_and_impact.md`, `2026-04-21-slug-reason_for_sought_support.md`, `2026-04-21-slug-support_purpose_framing.md`, `2026-04-21-slug-team_and_qualifications.md`

### `source` (6)

`0000-00-00-source-dylan_montgomerys_github.md`, `0000-00-00-source-dylan_montgomerys_google_scholar_page.md`, `0000-00-00-source-dylan_montgomerys_linkedin.md`, `0000-00-00-source-fnd_github.md`, `0000-00-00-source-ricky_jia_github.md`, `0000-00-00-source-ricky_jia_linkedin.md`

### `technical` (2)

`2026-00-00-technical-problem_that_justifies_software_work.md`, `2026-00-00-technical-skills.md`

### `technology` (1)

`0000-00-00-technology-innovation_description.md`

### `technology_case` (1)

`0000-00-00-technology_case-semantic_self_description_enables_open_coordination.md`

### `technology_comparison` (1)

`0000-00-00-technology_comparison-arduino_and_google_pattern_for_platform_authority.md`

### `technology_description` (1)

`0000-00-00-technology_description-mycite_framework.md`

### `transition` (1)

`0000-00-00-transition-coordinated_local_agriculture_pathway.md`
