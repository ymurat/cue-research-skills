# Research Workflow and Decision Gates

Use only the stages needed for the user's decision. Do not treat a complete folder or a large plan as progress by itself.

## Collaboration questions

At each stage, answer: What is the human deciding? What evidence has actually been inspected? What may happen next? What would stop or narrow the work? Which deeper work is not yet justified?

## Stages

| Stage | Decision or evidence needed | Typical output (only if useful) |
|---|---|---|
| Project state and scope | What question, context, unit, contribution/outcome, non-goals, and stop rule are in play? | Brief project state or scope note |
| Source review | What do the most relevant sources establish, and what remains unknown? | Citation list and literature matrix |
| Construct/method definition | What is the claim, construct, unit, measure, comparison, and falsifier? | Study protocol, formal definition, or method sketch |
| Novelty check | What measurable difference remains over the closest work? | Short novelty assessment |
| Reality/feasibility check | Can the exact data, participants, software, devices, measures, and intervention answer the question? | Bounded feasibility assessment |
| Pilot or prototype | Does a small, representative test validate the scientific path as well as the technical path? | Pilot protocol, raw evidence, and interpretation |
| Execution or analysis | Is scope approved, provenance complete, and analysis plan fit for purpose? | Reproducible implementation/run/analysis package |
| Review and communication | Are claims traceable and appropriately limited? | Critique, report, paper section, lesson, or bilingual summary |

## Gates

**Scope gate.** Proceed when the question, unit/population, context, intended contribution or outcome, non-goals, evidence needs, and stop/narrow criteria are intelligible. If not, help narrow the question before building a detailed plan.

**Evidence and novelty gate.** Use `NOT_ASSESSED` until sources and direct competitors have been inspected. Then state the residual contribution; reject novelty claims that only rename an established method or apply it to a new domain without a measurable delta. A novelty pass permits feasibility analysis, not automatic implementation.

**Reality gate.** Keep separate: (1) scientific validity—can the unit, intervention, and measure test the claim? (2) engineering feasibility—can the actual data/tool path run reliably and reproducibly? (3) viability—would a null or mixed result still answer the stated question? Mark each critical check `pass`, `fail`, `unknown`, or justified `not_applicable`; a checklist without evidence does not pass a gate.

- `BLOCK`: a critical failure exists, or an unknown has no bounded test. Allow only corrective evidence work.
- `PILOT_ONLY`: no known fatal issue remains and uncertainties have bounded tests. Do only the smallest claim-relevant pilot.
- `EXECUTION_READY`: critical checks pass for the named scope; implementation or study execution may be planned at that scope.
- `FULL_RUN_READY`: in addition, a claim-eligible pilot, frozen primary comparison and analysis/sample logic, complete provenance, bounded cost, and human approval are in place.

**Claim gate.** For each headline claim, trace: research question → contribution → closest work/residual → test or proof obligation → evidence/source or result → paper/teaching location → limitation. Narrow, qualify, or remove claims without an inspected evidence path.

## Test and execution discipline

1. Define the true unit and grouping (for example, repository, commit, pull request, participant, team, learner, game session, or task). Avoid leakage between related units and account for repeated measures where relevant.
2. Specify sampling and inclusion/exclusion, intervention or treatment, controls/comparison, outcome, denominator, missingness, uncertainty, and an analysis plan before interpreting results.
3. Verify data provenance, versions, licenses, access constraints, preprocessing, and whether the treatment reaches the intended unit unchanged. Check that a claimed prerequisite capability exists before attributing its loss to an intervention.
4. For a technical smoke test, label it `engineering_smoke`; record environment and runtime, but do not call it a feasibility result.
5. For a scientific pilot, use representative units and validate the complete path: provenance, controls, measurement, hand-checked outputs, valid yield, and an interpretable stop/continue criterion.
6. Before a full run, freeze the primary contrast, sample/precision logic, exclusions, multiplicity handling, seeds or randomization, artifact schema, compute/time budget, retry cap, and stopping conditions. Obtain explicit approval.
7. Log changes to dataset, model, simulator, device, version, scale, or protocol. Re-open any validity check or claim that depended on the original choice; do not assume results transfer automatically.

## Materialize selectively

- Raw idea and unreviewed literature: create at most a scope note and source list if useful. Keep novelty and feasibility `NOT_ASSESSED`.
- Reviewed sources but unstable question: create or revise the literature matrix and scope only.
- Stable claim and measure: define the method and assess novelty before creating a full protocol.
- Named unit/access path or a feasibility-sensitive request: assess reality and propose one bounded test.
- `PILOT_ONLY`: create only the pilot materials needed to resolve those unknowns.
- Execution-ready: plan the authorized scope; do not create a full paper or broad architecture unless requested and justified.

## Teaching and learning outputs

For a lesson, assignment, rubric, or teaching intervention, identify audience/prerequisites, measurable learning objectives, activity, assessment evidence, timing, accessibility, and feedback. For claims about learning gains, define the outcome and a defensible comparison; attendance, satisfaction, engagement, presence, or game completion alone do not prove learning. Treat instructor-facing explanation and student-facing material as separate audiences when useful.
