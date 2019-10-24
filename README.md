# open-sdlc


This document provides general guidance around procedures and practices
related to the software development life cycle (SDLC) at Metrum Research
Group (MetrumRG), with minor adaptations for the broader community.

## Definitions

* **Code Freeze:** Time from when no new changes to the existing
code-base is allowed until the next stage of development
begins.

* **Good Coding Practices**: Practices that have been established with
the objective of increasing the quality of software.

* **Functional Requirement:** Requirement for any functionality needed to
provide a capability/action as described in a User Story.

* **Impact Assessment:** An assessment of the impact associated with the
development of Product Features for a specific User Story.

* **Integration testing**: Process to test if associated modules continue
to work as expected, when integrated together.

* I**terative Development, Testing, and Documentation (IDTD):** The
iterative process of developing code, testing requirements, and
documenting specifications and results. Iterations are typically
executed incrementally at the level of the User Story.

* **Milestone:** Specific collection of Product Features and associated
time requirements for completion for a specific Product
Release.

* **Nonfunctional Requirement:** Requirement that defines a product
attributes such as performance, usability, etc. as defined by a User
Story.

* **Product Feature:** A feature, component, or performance
characteristic of the product which may be desired for future Product
Release.

* **Product Release:** The result of a completed SDLC process for a
specific Milestone set of User Stories.

* **RACI:** A defining set of responsibilities for team
members.

* **Responsible:** People or stakeholders who do the work. They must
complete the task or objective or make the decision. Several people
can be jointly Responsible.

* **Accountable:** Person or stakeholder who is the \"owner\" of the
work. He or she must sign off or approve when the task, objective or
decision is complete. This person must make sure that responsibilities
are assigned in the matrix for all related activities. Success
requires that there is only one person Accountable.

* **Consulted:** People or stakeholders who need to give input before
the work can be done and signed-off on. These people are active
participants.

* **Informed:** People or stakeholders who need updates on progress or
decisions, but they do not need to be formally consulted, nor do they
contribute directly to the task or decision.

* **Regression Testing:** Process to test if prior product functionality
continues to work as expected. This testing takes a risk-based approach,
and it can reuse any previous testing techniques and be incorporated
into test cycles.

* **Requirements Specification:** A listing of all Functional and
Nonfunctional Requirements compiled across all Product Features for a
specific Product Release.

* **Roadmap** A project management organizational
instrument utilized to track all User Stories describing potential
Product Features for future Product Release.

* **Traceability Matrix:** A table which links corresponding
requirements, tests, and test results for each User Story for a specific
Product Release.

* **Unit testing:** Process to test individual code elements in
isolation.

* **User Story:** Unit of description for a planned development
activity.

* **Validation Plan:** A compilation of the documentation of planned
tests of Functional or Nonfunctional Requirements associated with a
specific Product Release

* **Validation Plan Summary Report:** A summary of the Validation Testing
results and Traceability Matrix for a specific Product
Release

* **Validation Testing:** The testing of Functional or Nonfunctional
Requirements associated with the Validation Plan for a specific Product
Release

# Philosophy

Software development activities at MetrumRG are characterized
by:

* a focus on the actions that will deliver the most value to the
     customer or end*user

* a growth mindset, acknowledging that the best answer may not be
     immediately evident and that failure is part of
     learning

* an openness to constructive feedback

* a commitment to maximizing the probability of success of a
particular decision path, whether in agreement or not

* an eagerness to learn

* efficient and transparent processes

* high quality deliverables

# Project Management
-------------------------------

Software development projects are managed using iterative
methodologies. The key focus points are: 1) development in a fashion
that is focused on end-user needs, and 2) acknowledgement that precise
and accurate project requirement scoping and time/cost forecasting are
highly unlikely when attempted before the start of a project. Thus,
expectations around the project should be continually evaluated to make
appropriate tradeoffs as requirements and timelines change.

Development proceeds incrementally, with a preference for consistently
delivering high quality software. Requirements specification, testing,
and documentation are also implemented incrementally via an iterative
development, testing and documentation (IDTD) process. To develop as
such, sprint cycles or other techniques may be used based on project
requirements, team design, and overall project complexity.

## Roles & Responsibilities

* A key component of project management is assignment of specific roles
and responsibilities to project team members. The roles and
responsibilities are adjusted given the project size and scope and, in
some cases, multiple roles may be served by the same individual. Roles
and responsibilities will be defined for each Product Release and
documented in the project version control system. Further delineation of
roles is defined via a RACI (Responsible, Accountable, Consulted,
Informed) matrix for each User Story (see Development section). A
non-exhaustive list of roles and responsibilities is shown
below:

* **PL:** Project Lead: Status and communication of project activities, deliverables, and timelines within the team and to external stakeholders.
* **TL:** Tech Lead: Overall technical and design implementation choices and execution. Scoping of implementation timelines.
* **D:** Developer: Implementation of functionality, testing, documentation, and other relevant developer activities.
* **DO:** Devops (optional): Operational activities such as continuous integration/development, building and publishing releases.
* **SA:** System Architect (optional): System design strategy.
* **SME:** Subject Matter Expert (optional): Subject matter specific feedback and guidance.
* **QA:** Quality Assurance: Development activities proceed via the defined SOP relevant to the project.

# Project Lifecycle

The Project Lifecycle is comprised of multiple phases: Kickoff,
Planning, Development, Review, Validation, Release, and
Maintenance.

### Kickoff

The project kickoff is a unique extension to the planning phase that
happens at the beginning of a given project. The focus of this phase is
to set the project scope and default expectations around development
activities, roles and responsibilities, work instructions, and various
other procedural elements of the project lifecycle. 

During all subsequent planning sessions, these choices are assessed for
whether they still hold true. If so, the project proceeds as outlined in the
planning section below. If any changes are proposed, an impact
assessment of the proposed changes must be performed. In particular, if
changes impact how development and release occur, a plan to address all
project work to date to align with any gaps compared to the proposed
changes. For example, if the definition of low vs medium product risk is
changed, all activities classified as low product risk under the
original definition must be assessed to determine whether they would
have been classified as medium product risk under the newly proposed
change, and if so, must retrospectively be updated to meet the medium
product risk requirements around testing, information flow, and other
project requirements before the next release.

In addition, an initial discussion with potential customers for the
product results in the specification of potential Product Features
reflecting functionality or desired user experience characteristics.
These Product Features are then translated into terms easily understood
or specified by end-users as User Stories. In addition to defining User
Stories to represent desired Product Features, additional development
tasks such as bug fixes or internal refactoring necessary to support
future release(s) may be also be identified. Initial planning for a
project categorizes all potential User Stories by priority in a product
Roadmap with an initial estimate of the time necessary to
complete each.

### Planning

This phase is typically led by the Project Lead and initiates the
effort for the upcoming Product Release. First, any feedback or requests
from customers that has been collected over the previous release cycle
is triaged and prioritized into the product roadmap. Given the Product
Roadmap, the scope, schedule, and team assignments are
defined for the upcoming Product Release.

1. Scope: The initial scope is defined by selecting from the Product
Roadmap the User Stories which are highest priority,
or bring the most value to the end-user for the next Product
Release.

2. Schedule: An initial assessment of the total estimated time to
complete the scope defined for a Product Release is made, relative
to customer expectations for the delivery of the next Product
Release. Adjustments in scope may be necessary to accommodate
timing requirements. The combination of the scope and schedule for
a specific Product Release is known as a Milestone.

3. Team Assignment: Team members, roles and responsibilities are
defined for this Milestone. The style and frequency of code
reviews should also be defined within the context of the team
make-up.

### Development

Development proceeds as an iterative process of developing code,
testing requirements, and documenting specifications and results (IDTD).
Iterations are typically executed incrementally at the level of the User
Stories for a specific Milestone. Milestone project progress and current
status of User Stories for a specific Milestone should progress through the the following stages: Backlog,
Scope, Scope-Complete, Implement, Implement-Complete, Accept,
Accept-Complete, and Done. The entire process, including approval of
stage transitions, is tracked and documented using a version-control
system.

1. **Backlog**: The backlog is defined by the complete set of User
Stories defined in the planning phase in priority order.
Additional User Stories are included in the backlog for tasks that
are not related to the development of Product Features, such as
review meetings with the customer, documentation aggregation,
final approval and merge of the code-base, etc.

2. **Scope**: The scoping stage is critical for the successful
completion of all following stages and for delivering quality and
accuracy of each User Story and ultimately for the Product
Release. The scope for each User Story includes definition of
specific Functional Requirements, Nonfunctional Requirements, and
an Impact Assessment. The Impact Assessment considers all
activities to be implemented in the User Story and assesses the
product risk that implementation of this User Story will adversely
impact the system/software. Given the Impact Assessment, the roles
of team members with respect to transition through Development
Project Stages is defined via a RACI.

   * Low Product Risk: unlikely to adversely impact the user as
       compared to the existing Feature, addition of this
       functionality is unlikely to negatively impact existing
       functionality.

   * Medium Product Risk: some dependencies with other product
       features, may change existing product functionality, improper
       implementation would have a meaningful impact to end-user
       functionality or product value.

   * High Product Risk: extensive dependencies with other product
       features, major change in existing product functionality,
       omission of this feature would adversely impact on the value
       of the product *and/or* the use of the existing features in
       the product that may be impacted is difficult to
       assess.

3.  **Scope Complete**: Transition to Scope Complete requires completed
Functional Requirements, Nonfunctional Requirements and Impact
Assessment for the User Story.

4.  **Implement**: This stage begins with the development based on
acceptance criteria for each of the Functional and Nonfunctional
Requirements. A hierarchy of tests will be written and
executed.

Tests should be used judiciously, and strive to represent the
real-world usage scenarios outlined in the user stories. Tests
should be automated when possible but some manual testing may
be required. Unit tests provide a foundation of testing and
capture expected outputs. Prior to release, additional
integration tests can capture the expected behavior across
multiple units. Specific regression tests may be defined as
necessary and appropriate.

5.  **Implement Complete**: Transition to Implement Complete requires a
    code review and review of test cases and acceptance
    criteria.

6.  **Accept**: Test cases for the User Story are confirmed. Code
    associated with the User Story undergoes a code freeze, and
    Deviations (failures) are identified and result in a return to one
    of the prior stages, as appropriate.

7.  **Accept Complete**: Transition to this stage requires verification
    that the User Story requirements have been satisfied and all
    requirements specifications, and testing results for the User
    Story have been documented in the version control
    system.

8.  **Done**: Code for this User Story is incorporated into the
    codebase for the next release.

### Review

Code review is an ongoing process for all development efforts. Each
code review should strive to cover a single User Story
feature/implementation detail. The style and frequency of code reviews
should be agreed upon in the Planning stage for the specific Milestone.
Considerations for code review activities include:

1. Experience and capabilities of other team members

2. Impact assessment for specific User Stories

3. Project timing and deadlines for code review activities

4. Adherence to code standards

In some cases, code reviews may be difficult due to limitations of
teammate capabilities or expertise. In these situations, the author
should request a conceptual review to discuss the code implementation
strategy and logic flow.

Upon completion of all User Stories, a functionality review may be
undertaken at the Milestone level. A code freeze is initiated, and a
pre-release candidate is created to denote the development team's
expectation of completion of development tasks. User acceptance testing
is performed for completeness and correctness, and results are
documented. Where the code review may focus on code quality and
correctness, a functionality review assesses whether the integrated
product meets the user's needs.

### Validation Summary

Under the IDTD process, several of the individual components necessary
for software validation are implemented and documented in the version
control system throughout the development process. In the validation
phase, incrementally developed content is aggregated and any gaps are
identified and new tests may be implemented. This ensures the completion
of all validation-related activities and deliverables.

1.  Requirements Specification: This document lists all Functional
    Requirements and Nonfunctional Requirements compiled across all
    Product Features for a specific Product Release.

2.  Validation Plan: The Validation Plan is a document that defines
    activities and responsibilities for the validation effort. This
    document sets the testing strategy and acceptance criteria for
    successful validation qualification.

3.  Validation Testing: Validation Testing includes execution and
    documentation of all of the final User Story specific tests
    conducted throughout development, as well as the User Acceptance
    Tests performed during the functionality review.

4.  Validation Plan Summary Report: This report summarizes the results
    of the Validation Testing in the context of the Validation Plan
    for the specific Product Release. Test results are mapped to
    corresponding tests, requirements, and Users Stories via a
    Traceability Matrix.

5.  Traceability Matrix: This table links corresponding requirements,
    tests, and test results for each User Story for a specific
    Release. Traceability is managed in the IDTD process by
    implementing specific naming conventions and organizational
    practices within the version control system.

### Release

Completion of validation typically leads to release of the Product,
pending the potential resolution of remaining product defects. In some
circumstances, release may proceed with known defects given an otherwise
favorable assessment of the value of the product.

1. Defect Management: Defects remaining in the code base for a
particular release are identified in release notes and
subsequently tracked as User Stories in the Product Roadmap. Defect-related User Stories are considered for
inclusion in subsequent product releases in the planning phase of
the SDLC.

2. Versioning: Product Releases should adhere to the closest feasible
implementation possible of semantic versioning
(https://semver.org/) allowable by the language. If deviations are
made, they should adhere to the best-practices established by the
language. Version constraints (generally) do not influence
development processes, rather, they serve to quickly communicate
the state of changes in a project.

### Maintenance

Each product line shall have a defined support and maintenance process,
typically facilitated by a ticketing system. There are three key areas
of maintenance categories:

1. Bug Fixing: It is impractical to perform an exhaustive test on a
large software system. Therefore, it is reasonable to assume that
any large system will have errors. The process of receiving
reports of such errors, diagnosing the problem, and fixing them is
called "Bug Fixing". Upon identification, bugs will be defined and
described as new User Stories. The system impact of the bug will
be assessed and appropriately prioritized in the product Roadmap
for incorporation into a new release.

2. Query/Clarification: This is simply responding to query posed by
the user, which is a result of lack of familiarity or
understanding of the product. No bug or defect is identified. The
maintenance team member would understand the query and provide a
corresponding solution (explanation, guidance, etc.) to the
user.

3. Enhancements/Feature Requests: User-generated product enhancements
or feature requests are acknowledged as such and new User Stories
are created for each feature request. These User Stories are
tracked in the product Roadmap and development proceeds as
described in the Planning phase of the SDLC.

References
=======================

* 21 CFR Part 11: *Predicate Rules*

* ISO/IEC 19941;2017 (E): *Information technology - cloud computing -

* ISO/IEC/IEEE 90003; 2018 (E):

* ISPE GAMP Good Practices Guide; *A Risked Based Approach to GxP
Compliant Laboratory computerized systems; Second Edition*

* ISPE GAMP Good Practice Guide*; A RIsk based Approach to compliant
Electronic Records and Signatures*

* PIC/S: *Guidance Good Practice for Computerized Systems in regulated
GxP Environment; 2007*

* ISPE GAMP *COP Annex II Interpretation*

* ICH Q9; *Quality RIsk Management; Version 4; Nov.2027*

* B.Meyer, Agile!, DOI 10.1007/978 - 319 - 05155-0\_5, Springer
International Publishing Switzerland 2014

* General Principles of Software Validation, Guidance for Industry and
FDA Staff
  * https://www.fda.gov/regulatory-information/search-fda-guidance-documents/general-principles-software-validation]{.underline}](https://www.fda.gov/regulatory-information/search-fda-guidance-documents/general-principles-software-validation)
