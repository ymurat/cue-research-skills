# Domain Guidance

Select relevant checks; do not force every study into one experimental template. Mixed-methods and qualitative work still need a clear unit, sampling rationale, analysis trace, and limits on transfer.

## Software-engineering research

For repository mining, experiments, case studies, surveys, interviews, or developer/education studies:

- Define the unit (project, repository, commit, issue, pull request, developer, team, task, or student) and the sampling frame. State repository inclusion criteria, time window, forks/duplicates, survivorship, missing histories, and project dependence.
- Check construct validity: do proxies such as issue counts, stars, test coverage, review latency, or static-analysis warnings measure the claimed concept? Preserve denominators and distinguish association from causal effect.
- For tools or interventions, compare against a credible baseline and a realistic workflow. Control for language, project size, developer experience, task difficulty, tool familiarity, and time-on-task where relevant.
- For coding assistants, record model/version, prompt/context, repository snapshot, tool settings, retries, human edits, acceptance criteria, and whether evaluation uses hidden tests or only visible examples. Avoid test contamination and leakage from public benchmark solutions.
- Record repository commit, dependency lockfile, runtime/OS, hardware, seeds, configuration, benchmark version, and exact reproduction steps when relevant. Check the licenses and attribution for source code, datasets, models, assets, and dependencies; flag privacy, security, and supply-chain risks before recommending execution.
- For surveys/interviews, report recruitment, response and nonresponse, instrument wording, coding scheme, researcher role/reflexivity, and limits of generalization. Protect participant and employer-confidential information.
- For replications, distinguish exact, close, and conceptual replication and document departures from the original protocol.

## AI and machine-learning research

- Record model/provider and revision, system prompt/configuration, decoding, tools, preprocessing, dataset/version/license, code commit, environment, seed, and evaluation date when available.
- Audit train/validation/test separation, duplicate and benchmark contamination, temporal or entity leakage, prompt leakage, and evaluator access to answers. Use baselines matched to the question, not only convenient weak baselines.
- Define primary and secondary metrics, denominator, aggregation, uncertainty, missing outputs, failure handling, human-judge rubric, inter-rater agreement, and calibration where relevant. Separate capability, safety, usability, and cost claims.
- Validate the underlying capability before claiming an intervention degraded, improved, or exposed it. Compare multiple samples/runs when stochasticity matters; do not promote one cherry-picked output into a general claim.
- Treat generated citations, summaries, code, and translations as unverified until checked against authoritative sources, test execution, or human review. Report inference cost, latency, energy/compute if relevant, rate limits, retries, and invalid-output yield. Reassess validity when models or APIs change.

## VR/XR, HCI, and immersive systems

- Specify modality and hardware (e.g., headset, controllers, display), software/build, tracking, frame rate, interaction design, room/setup, calibration, and the participant's actual exposure.
- Choose a comparison condition that isolates the intended mechanism (such as immersion, interaction, or spatial representation); do not confound novelty, content, input device, instructor attention, and treatment.
- Distinguish presence, usability, workload, cybersickness, engagement, performance, retention, and transfer. Do not treat presence or preference as a learning or performance outcome.
- Plan informed consent, withdrawal, orientation, comfort breaks, adverse-event and stop procedures, accessibility and non-VR alternatives. Consider cybersickness, fatigue, balance/fall risk, physical-space hazards, and privacy risks from eye/face/body tracking or audio/video capture. Follow applicable institutional ethics review; do not assume a demo or classroom activity is exempt.
- Report recruitment, exclusions, prior VR experience, exposure duration, and device-related failures. For field use, state ecological limits: lab performance may not transfer to classroom, workplace, or clinical settings.

## Serious games and game-based learning

- Explain the intended learning, training, behavioral, or decision-making mechanism and map game mechanics to that mechanism; engagement is not itself evidence of effect.
- Describe game version, rules, scenario/content, difficulty, progression, feedback, session length, player actions, and facilitator involvement so the intervention can be reproduced.
- Compare against an active non-game or alternative activity where the question is whether game features help, rather than comparing a rich game with no instruction.
- Measure learning or target behavior with a valid assessment, and consider delayed retention or transfer if claimed. Separate knowledge gains from enjoyment, time-on-task, completion, and self-report.
- Consider prior gaming, accessibility, cognitive load, competitiveness/cooperation, and group effects. For minors or school deployments, consider guardian consent/assent, school approval, safeguarding, data retention, and teacher workload. Predefine safety and debriefing when content is sensitive.

## Research and teaching practice

- Separate creating a course/lesson/resource from testing its educational effectiveness. Keep pedagogical advice grounded in reviewed evidence and local course constraints.
- Align learning objectives, teaching activity, assessment, and feedback. Prefer observable outcomes over vague aims such as “understand.”
- For classroom research, consider instructor/researcher dual roles, consent and voluntariness, grading power, privacy, accommodations, and institutional ethics review. Do not assume a classroom activity is exempt from review.
- Make student-facing explanations clear, inclusive, and level-appropriate; put instructor notes, answer keys, and assessment rubrics in distinct sections if needed.
