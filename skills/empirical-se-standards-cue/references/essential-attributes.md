# ACM SIGSOFT Empirical Standards: essential attributes (raw checklist items, fetched 2026-10-31 from github.com/acmsigsoft/EmpiricalStandards master/docs/standards; repo last pushed 2026-10-26T17:52Z). Raw copy for local reference; paraphrase when quoting.


## ActionResearch (13 items)
- justifies the selection of the site(s) that was(were) studied
- describes the site(s) in rich detail
- describes the relationship between the researcher and the host organization
- describes the intervention(s) in detail
- describes how interventions were determined (e.g. by management, researchers, or a participative/co-determination process)
- explains how the interventions are evaluated
- describes the longitudinal dimension of the research design (including the length of the study)
- describes the interactions between researcher(s) and host organization(s)
- explains research cycles or phases, if any, and their relationship to the intervention(s)
- presents a clear chain of evidence from observations to findings
- reports participant or stakeholder reactions to interventions
- reports lessons learned by the organization
- researchers reflect on their own possible biases

## Benchmarking (6 items)
- EITHER: justifies the selection of an existing, publicly available or standard benchmark (in terms of relevance, timeliness, etc.)
- describes the experimental setup for the benchmark in sufficient detail to support independent replication (or refers to such a description in supplementary materials)
- specifies the workload or usage profile in sufficient detail to support independent replication (or refers to such a description in supplementary materials)
- allows different configurations of a system under test to compete on their merits without artificial limitations
- assesses stability or reliability using sufficient experiment repetitions and execution duration
- discusses the construct validity of the benchmark; that is, does the benchmark measure what it is supposed to measure?

## CaseStudy (7 items)
- justifies the selection of the case(s) or site(s) that was(were) studied
- describes the site(s) in rich detail
- the site is a real (physical or virtual) place, not a toy example or imaginary world
- reports the type of case study
- describes data sources (e.g. participants' demographics and work roles)
- defines unit(s) of analysis or observation
- presents a clear chain of evidence from observations to findings

## CaseSurvey (9 items)
- presents step-by-step, systematic, replicable description of the search process for published case studies (not necessarily in peer-reviewed venues)
- defines clear inclusion and exclusion criteria for cases
- describes the sampling strategy (see the [Sampling Supplement](https://github.com/acmsigsoft/EmpiricalStandards/blob/master/docs/supplements/Sampling.md))
- mitigates sampling bias and publication bias, using some (not all) of:
- defines a coding scheme to convert qualitative case descriptions into quantitative variables
- EITHER: describes the coding scheme in detail;
- clearly explains how missingness in the dataset was managed
- draws conclusions based on the quantitative variables derived
- acknowledges generalizability threats; discusses how case studies reviewed may differ from target population

## DataScience (12 items)
- explains why it is timely to investigate the proposed problem using the proposed method
- explains how and why the data was selected
- presents the experimental setup (e.g. using a dataflow diagram)
- describes the feature engineering approaches and transformations that were applied
- explains how the data was pre-processed, filtered, and categorized
- EITHER: discusses state-of-art baselines (and their strengths, weaknesses and limitations)
- defines the modeling approach(es) used (e.g. clustering then decision tree learning), typically using pseudocode
- discusses the hardware and software infrastructure used
- justifies all statistics and (automated or manual) heuristics used
- describes and justifies the evaluation metrics used
- goes beyond single-dimensional summaries of performance (e.g., average; median) to include measures of variation, confidence, or other distributional information
- discusses technical assumptions and threats to validity that are specific to data science

## EngineeringResearch (9 items)
- describes the proposed artifact in adequate detail
- justifies the need for, usefulness of, or relevance of the proposed artifact
- conceptually evaluates the proposed artifact; discusses its strengths, weaknesses and limitations
- empirically evaluates the proposed artifact using:
- clearly indicates which of the above empirical methodology is used
- EITHER: discusses state-of-art alternatives (and their strengths, weaknesses and limitations)
- EITHER: empirically compares the artifact to one or more state-of-the-art alternatives
- assumptions (if any) are explicit, plausible and do not contradict each other or the contribution's goals
- uses notation consistently (if any notation is used)

## Experiments (18 items)
- states formal hypotheses
- uses two-sided hypotheses OR justifies use of one-sided hypotheses based on face validity or previous work
- describes the dependent variable(s) and justifies how they are measured (including units, instruments)
- describes the independent variable(s) and how they are manipulated or measured
- describes extraneous variables and how they are controlled: physically, statistically, or not at all
- justifies sample size (e.g. using power analysis)
- describes how characteristics of the phenomenon under investigation relate to experimental constructs
- describes the research design and protocol including treatments, materials, tasks, design (e.g. 2x2 factorial), participant allocation, period and sequences (for crossover designs), and logistics
- EITHER: uses random assignment and explains logistics (e.g. how random numbers were generated)
- describes experimental objects (e.g. real or toy system) and their characteristics (e.g. size, type)
- justifies selection of experimental objects; acknowledges object-treatment confounds, if any
- design and protocol appropriate (not optimal) for stated research questions and hypotheses
- confirms no incentives for participation were offered or describes financial or non-financial incentives
- describes participants (e.g. age, gender, education, relevant experience or preferences)
- reports distribution-appropriate descriptive and inferential statistics; justifies tests used
- reports effects sizes with confidence intervals (if using frequentist approach)
- discusses construct, conclusion, internal, and external validity
- discusses alternative interpretations of results

## GeneralStandard (18 items)
- states a purpose, problem, objective, or research question
- explains why the purpose, problem, etc. is important (motivation)
- defines jargon, acronyms and key concepts
- names the methodology or methodologies used
- methodology is appropriate (not necessarily optimal) for stated purpose, problem, etc.
- describes in detail what, where, when and how data were collected (see the [Sampling Supplement](https://github.com/acmsigsoft/EmpiricalStandards/blob/master/docs/supplements/Sampling.md))
- describes in detail how the data were analyzed
- presents results
- results directly address research questions
- enumerates and validates assumptions of statistical tests used (if any)
- discusses implications of the results
- discloses all major limitations
- states clear conclusions which are linked to research question (or purpose, etc.) and supported by explicit evidence (data/observations) or arguments
- contributes in some way to the collective body of knowledge <!-- (see Replications Supplement) -->
- language is not misleading; any grammatical problems do not substantially hinder understanding
- acknowledges and mitigates potential risks, harms, burdens or unintended consequences of the research (see the ethics supplements for [Engineering Research](https://github.com/acmsigsoft/EmpiricalStandards/blob/master/docs/supplements/EthicsEngineering.md), [Human Participants](https://github.com/acmsigsoft/EmpiricalStandards/blob/master/docs/supplements/EthicsHumanParticipants.md), or [Secondary Data](https://github.com/acmsigsoft/EmpiricalStandards/blob/master/docs/supplements/EthicsSecondaryData.md))
- visualizations/graphs are not misleading (see the [Information Visualization Supplement](https://github.com/acmsigsoft/EmpiricalStandards/blob/master/docs/supplements/InformationVisualization.md))
- complies with all applicable empirical standards

## GroundedTheory (8 items)
- identifies the variant(s) of Grounded Theory used/adapted (Glaser, Strauss/Corbin, Charmaz, etc.)
- characterizes the data (participants' demographics, types of documents, nature of field notes, ...)
- explains how the research iterated between data collection (using theoretical sampling) and analysis (using constant comparison)
- states that and how theoretical saturation was determined
- explains how key patterns (e.g. categories) were found via GT steps (e.g. selective coding)
- states results in terms of concepts that assign meaning to data ("theoretical coding": do not merely _describe_ the data)
- grounds most or all important concepts in raw data explicitly (e.g. by providing quotations)
- discusses the transferability of the theory

## Longitudinal (11 items)
- determines the appropriate number of waves based on the natural oscillation of the research phenomenon
- uses at least two data collection waves
- subjects (humans or artifacts) are identifiable between waves
- justifies the data analysis strategy
- the data analysis strategy is appropriate for the interdependent nature of the data
- discusses the critical alpha levels or justifies Bayesian priors
- justifies sample size (e.g. using power analysis)
- describes data loss throughout the different waves
- explains how missing data are handled
- describes the subjects (e.g., demographic information in the case of humans)
- discusses the operationalization of the research model (i.e. construct validity)

## MetaScience (3 items)
- presents information that is useful for other researchers
- makes recommendations for future research
- presents clear, valid arguments supporting recommendations

## MixedMethods (7 items)
- **justifies** using multiple methodologies and/or methods
- provides a **purpose statement** that conveys the overarching multi or mixed method design intent (why)
- describes the **multi-methodology**, **multi-method** or **mixed method** design (what)
- describes **which phases** of the research study the different methods or methodologies are used in (when)
- describes how the design aligns with the research question or objective
- **integrates the findings** from all methods to address the research question/objective
- acknowledges the **limitations** associated with integrating findings

## OptimizationStudies (13 items)
- explains why the problem cannot be optimized manually or by brute force within a reasonable timeframe
- EITHER: describes prior state of the art in this area
- describes the search space (e.g., constraints, independent variables choices)
- uses realistic and limited simplifications and constraints for the optimization problem; simplifications and constraints do not reduce the search to one where all solutions could be enumerated through brute force
- justifies the choice of algorithm underlying the approach
- compares approaches to a justified and appropriate baseline
- explictly defines the solution formulation, including a description of what a solution represents, how it is represented, and how it is manipulated
- explicitly defines all fitness functions, including the type of goals that are optimized and the equations for calculating fitness values
- explicitly defines evaluated approaches, including the techniques, specific heuristics, and the parameters and their values
- EITHER: clearly describes (and follows) a sound process to collect and prepare the datasets used to run and to evaluate the optimization approach
- EITHER: makes data publicly available
- identifies and explains all possible sources of stochasticity
- EITHER: executes stochastic approaches or elements multiple times

## QualitativeSurveys (8 items)
- explains how interviewees were selected (see the [Sampling Supplement](https://github.com/acmsigsoft/EmpiricalStandards/blob/master/docs/supplements/Sampling.md))
- describes interviewees (e.g. demographics, work roles)
- describes interviewer(s) (e.g. experience, perspective)
- presents clear chain of evidence from interviewee quotations to findings (e.g. proposed concepts)
- clearly answers the research question(s)
- provides evidence of saturation; explains how saturation was achieved
- researchers reflect on their own possible biases
- identifies key issues under consideration

## QuantitativeSimulation (9 items)
- justifies that simulation is a suitable method for investigating the problem (or research question, etc.)
- describes the simulation model (conceptual, implementation, or hybrid abstraction levels), including input parameters and response variables
- describes the underlying simulation approach
- describes simulation packages or tools used to develop and run the simulation model, including version numbers, and computational environments
- describes the data used for model calibration, the calibration procedures, and contextual information
- describes how the simulation model was verified and validated at different abstraction levels
- describes the study protocol, including independent variables, scenarios, number of runs per scenario (in case of using stochastic simulation), and steady-state or terminating conditions
- analyzes validity threats considering the supporting data and the simulation model
- clearly explicates the assumptions of the simulation model

## QuestionnaireSurveys (12 items)
- identifies the target population and defines the sampling strategy (see the [Sampling Supplement](https://github.com/acmsigsoft/EmpiricalStandards/blob/master/docs/supplements/Sampling.md))
- describes how the questionnaire instrument was created
- describes how participants were selected or recruited (e.g. sampling frame, advertising, invitations, incentives)
- EITHER: measures constructs using (or adapting) validated scales
- describes how responses were managed/monitored, including contingency actions for non-responses and drop-outs
- explains handling of missing data (e.g. imputation, weighting adjustments, discarding)
- step-by-step, systematic, replicable description of data collection and analysis
- analyzes response rates
- assesses sufficiency of number of participants (statistical power)
- acknowledges generalizability threats; discusses how respondents may differ from target population
- provides the questionnaire instrument (as an appendix or supplementary materials)
- the questionnaire design matches the research aims and the target population

## Replication (14 items)
- discusses the motivation for conducting the replication in appropriate detail (e.g., to validate the results, to broaden the results by changing the participant pool or the artifacts)
- defines the type of the replication by methodological similarity (exact, methodological, conceptual)
- defines the type of the replication by overlap (partial, complete, extended)
- defines the type of the replication by participants (internal, external, mixed)
- the research questions of the original study
- the design of the original study
- if applicable, the participants of the original study (their number and any relevant characteristics)
- the artifacts of the original study
- the context variables of the original study that might have affected the design of the study or interpretation of the results
- the major findings of the original study
- EITHER: describes overlap or interactions with the original study author(s),
- describes and justifies any differences from the original study (design, participants, artifacts, procedures, data collection, or analysis)
- compares the results of the replication to the results of the original study
- clearly differentiates between results that are consistent and inconsistent with the original study

## RepositoryMining (15 items)
- explains why repository mining is appropriate for the proposed research problem
- defines unit(s) of analysis or observation
- describes and justifies the data sources (e.g. GitHub, StackOverflow)
- describes and justifies how the repositories are selected from the data sources (e.g. selection criteria, use of third-party tools, APIs, programming languages of choice)
- describes how the inclusion and exclusion criteria were validated (e.g., by manually inspecting the results of the automated search)
- describes the selected repositories
- describes the procedure for the acquisition (e.g., first selecting repositories and then downloading, or all completed together)
- if the data obtained is too large to be processed in its entirety
- describes dataset characteristics including size of the selected repositories, and dataset attributes relevant to the study at hand (e.g., number of commit messages)
- describes data preprocessing steps
- if manual annotations are carried out:
- describes and justifies measures or metrics used
- uses previously validated measures, quantitatively assesses construct validity, or both
- if predictive modeling is used, complies with the [Data Science Standard](https://github.com/acmsigsoft/EmpiricalStandards/blob/master/docs/standards/DataScience.md)
- discusses threats to external validity (e.g. caused by selection of data source(s) and repositories, selection criteria, search strings)

## SystematicReviews (8 items)
- identifies type of review (e.g. case survey, critical review, meta-analysis, meta-synthesis, scoping review)
- presents step-by-step, systematic, replicable description of search process including search terms
- defines clear selection criteria
- specifies the data extracted from each primary study ; explains relationships to research questions
- describes in detail how data were extracted and synthesized (can be qualitative or quantitative)
- describes coding scheme(s) and their use
- clear chain of evidence from the extracted data to the answers to the research question(s)
- presents conclusions or recommendations for practitioners/non-specialists