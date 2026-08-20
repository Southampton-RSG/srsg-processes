# TEC.4 - Verification

## Background

This process provides a consistent approach to verifying that project outputs meet their agreed requirements. It covers planning, conducting, recording and reviewing verification activities that are conducted iteratively throughout a project's lifecycle.

## Related Processes

- ORG.2 Management Framework  
- ORG.10 Lifecycle Model Management  
- PRJ.3 Configuration and Change Management  
- TEC.11 Requirements Analysis

## Purpose

This document defines the RSG process for verifying that project outputs satisfy that project's defined requirements, to ensure that:

- Stakeholder verification procedures relevant to the project are understood, captured, and planned for  
- Verification methods selected for a project are sufficient to verify requirements  
- Planned verification procedures are followed at expected points throughout a project  
- Verification plans are amended as required by the project, in consultation with stakeholders as needed, with amendments recorded  
- Developers are able to define, plan, adopt, and review verification procedures for a project

## Outcomes

Overall, the intended outcome of this process is that the SRSG has a repeatable and proportionate approach to ensure our project outputs demonstrably achieve their requirements throughout a project lifecycle.

Specifically, this process has the following output documents that are created and managed according to PRJ.3 Change Management: Verification Procedures, Verification Plan, Verification Records, Project Non-conformities. It also contributes outputs to the Sprint Review/Sprint Retrospective meeting documents, and the project-end Lessons Learned Report document.

## Policy

The RSG is committed to ensuring that all project requirements have been verified using defined methods. We shall:

- **Identify and plan for verification methods** as required by the project, eliciting any supplementary verification methods required by stakeholders  
- **Follow an iterative approach to verification,** where verification activities are carried out continuously throughout the cycle rather than as a single final stage  
- **Seek clarification or amendments from stakeholders on requirements** where they cannot be measurably verified (undertaken as part of TEC.11 BP1)  
- **Maintain transparency** of verification plans and verification outputs with stakeholders  
- **Involve stakeholders in verification** activities or analysis of verification outputs where their domain expertise is required to complete verification

Requirements are considered fully verified when all planned verification activities have been completed successfully.

## Verification Procedures

### BP1: Establish Verification Procedures

Any project shall ensure that requirements, both functional and non-functional, are verified successfully as they are completed, and iteratively as needed prior to final delivery. There shall be a clear way of demonstrating that each requirement has been sufficiently verified using at least one verification method, e.g. testing, peer review, or demonstration.

In general, as requirements are identified, defined, and agreed throughout the project:

1. **Identify and define the procedures necessary to verify the project requirements**:  
   1. Select suitable verification procedures, where a procedure includes a verification method and potentially a set of steps to undertake the procedure if such detail is needed. For typical RSE projects, see [Appendix: Verification Methods, Classes and Levels](https://docs.google.com/document/d/14gO_I0HxKS_Dia2mA775oludkgrrSOe9EE9Jal5VNZE/edit?tab=t.0) for example methods.  
   2. Discuss with stakeholders and take into account any additional verification procedures and those they are required to be involved in, how they need to be involved, and any client verification platforms that may need to be used, e.g. for compliance with regulations or other customer protocols.  
   3. Identify with stakeholders any independent verification procedures required to be undertaken by 3rd parties, e.g. the Cyber Security team for security reviews, or Research Innovation Services for legal or licensing.  
2. **Identify where project-level outputs need to be reviewed and how this will happen**. For design for example, there may be an architecture, components, technical choices, or other discrete design elements that may require verification.

Once identified:

3. **Define the verification procedures that will be used within a project Verification Procedures document**, with each procedure including a brief description of the verification method (the specific technique or technology used to verify a requirement), and the criteria that determine whether or not verification was successful. Where the methods are not already common RSG practice, include any environment set-up, tools, and step-by-step instructions required to accomplish that verification.  
4. **Refine the verification procedures throughout the project as needed**, as technical, operational, and other details become clearer and needs change.

As a general principle, automated verification should be used wherever practical and cost-effective to do so, particularly for repeatable verification activities such as unit testing, regression testing, static analysis and continuous integration checks. Manual verification remains important where human judgement is required, such as software usability assessment, customer demonstrations, data review, exploratory testing, etc. The balance between automated and manual verification will vary depending on the nature of the project. For software development projects, automated verification is often predominant; for data-focused project(s) that make use of third-party software, manual verification may form a larger part of the overall verification approach. 

Verification does not normally need to be witnessed by the customer. However, customers should be involved where appropriate through demonstrations, discussion of results, acceptance activities, project reviews or project handovers. For more technically involved customers, this may include a more detailed examination of the outputs or verification results. 

Overall, requirements are generally considered satisfied when both the defined Verification Procedures and Validation Procedures (defined in TEC.5 BP.1) have been completed successfully for all requirements.

### BP2: Plan Verification Activities

Once captured, the project verification procedures are defined within a project's Verification Plan. By default for a straightforward RSE project the Verification Plan should either be covered within their individual requirements issues in a project board, or take the form of a separate set of "verification" issues (linked to the requirement issues they verify), or for projects with more complex verification requirements, covered in a separate document. In any case, the overall Verification Plan needs to satisfy:

- **The verification procedures to be used** (as defined in the Verification Procedures document).  
- **The verification methods used to satisfy a requirement**, as indicated in each requirement issue, or in more complex cases as a traceability matrix in a table, with methods on one axis and requirements on the other, marking individual cells for a given method used to verify a requirement.  
- **Who will be responsible for administering each verification procedure,** either directly from within the project, or for initiating and overseeing a 3rd party verification activity.  
- **A schedule for when the procedures will be used**, throughout the project and software lifecycle.  
- **The extent to which the results of conducting a verification procedure need to be recorded as Verification Records**, how and where they should be recorded, and how long the records need to be held.  
  - For many typical development-level activities (such as recording results of individual test runs for every test case) this typically won't be required for every run, although successful verification should be noted as a requirement is completed (e.g. within a pull request). Results are discussed as needed within normal client interactions.  
  - Verification Records should be retrievable for larger-scale test runs conducted on specialist infrastructure such as Iridis, or in cases where "Run-For-Record" is needed to satisfy any compliance, certification, or final delivery requirements.   
  - Additionally, in identified cases of security, legal, regulatory or other situations where this needs to be demonstrated or available for audit, recording should be done in accordance with acknowledged procedures in those cases.  
  - By default, such records need to remain retrievable for at least one year after the project ends.

For efficiency and practicality, there should be a balance between verification tasks and development progress. In general, ensure that input data is reasonably tested against known outputs, representing a high level of test coverage through the system.

The Verification Plan will be reviewed and approved by the project team and the customer (to the extent that they wish or need to be involved).

### BP3: Conduct Verification Activities

Verification activities are conducted in accordance with the Verification Plan, and results shared with customers.

Ensure that results from system tests are recorded as Verification Records as specified in the Verification Plan, e.g.

- For automated systems, such as those provided by Continuous Integration infrastructures such as GitHub Actions, ensure the logs are not deleted and retained for a minimum of one year after the project is completed.  
- For other testing runs (e.g. for manual testing, or for those on Iridis or some other infrastructure), ensure results are recorded for larger test suite runs, linked to in a pull request.

Main findings and actions arising from code review should be recorded, e.g.

- For GitHub pull requests, ensure PRs contain highlights of the outcomes from review that are traceable to the commits made to address the issues found \[see PRJ.3\]  
- Whether for code or not, for other forms of review that aren't supported by infrastructure directly (e.g. an in-person review), record any non-conformities and actions ideally as GitHub issues on the code repository in question, or for non-code outputs, a review meeting document in Google Drive \[see PRJ.3\]

Where they are not otherwise recorded, the results of verification activities as discussed within sprints and within sprint reviews or retrospectives should be captured.

Any proposed changes to verification procedures and plans are recorded and discussed with stakeholders, and approved changes made in the Verification Procedures and Verification Plan documents.

In typical development when tests fail, the developer will directly fix the issue and retest until successfully verified. In the cases where the issue is still live and successful retesting hasn't occurred, the failure is recorded and discussed in client meetings (e.g. during a sprint demo or review it's noted that a particular feature doesn't yet work as required). For higher integrity projects where a test fails on a more formal "Run-For-Record" system test scenario, the test is recorded and either a "Quick Fix" is made or a Workaround (WAR) is documented to bypass the issue whilst a proper fix is developed.

When a project completes any verification records not already shared are handed over to the customers if they want them (e.g. as slides in a wrap-up meeting, or as links to records or documents).

### BP4: Review Effectiveness of Verification

#### Verification Review

The goal of review is to determine the effectiveness of the verification procedures used within a sprint or project, and is conducted with both the development team and with the clients throughout the project, typically in Sprint Review or Sprint Retrospective meetings, or project-end Lessons Learned meetings.

Within the development team, determine:

1. **Within the context of the project, what should change for future sprints.** Following a sprint (e.g. within the Sprint Retrospective meeting), evaluate the verification activity for the sprint. Were the verification procedures sufficient? What needs to change? If any underlying client verification platforms’ changes are identified (i.e. with the tooling or infrastructure used for verification), plan for how this change will be addressed.  
2. **How the outcomes of the verification activity will or should affect future projects.** During the project lessons learned meeting, consider and record opportunities or threats for future projects given the outcomes of the verification activity.

With the clients:

1. **Assess and agree on the outcomes of verification activities** within the Sprint Review meeting.  
2. **Identify any client verification platform changes early**, in the cases where a client's technologies, infrastructure, or tooling is required to conduct a verification procedure.

During review, evaluate whether the effort for verification activities is commensurate with the project. Assess this regularly during Sprint Retrospectives and Reviews, accounting for:

- Overall, an estimate of the effort taken to conduct verification activities.  
- From within the development team: the number and severity of issues discovered by the verification activities, plus the impact or potential impact of any infractions  
- From the customer, user base, and the development team: the number and severity of issues encountered through some level of "use" of the project outputs, the impact of any infractions

#### Identifying and Recording Non-conformities

Overall, the review process should also identify, assess, and record any nonconformities, where a nonconformity relates to a failure to satisfy an agreed requirement. All nonconformities should be recorded within a Project Non-conformities document. This should include the following information about each nonconformity:

1. **Description of the nonconformity,** including how, when and why it occurred.  
2. **Its severity**, one of:  
   1. *Major nonconformity:* a significant failure to meet a requirement and undermines the product's ability to function effectively.  
   2. *Minor nonconformity:* an isolated occurrence, the overall integrity of the product isn't compromised but requires attention to prevent escalation. Typically, these are simple to resolve.  
   3. *Opportunity for Improvement:* an area where the system could become vulnerable or where efficiency could be enhanced.  
3. **How it was or will be resolved**, including any Quick Fixes or Workarounds that were applied to overcome the non-conformance in the short term.  
4. **Any issues which are still outstanding**, and what needs to be done and by whom.  
5. **Recommendations for improvement** based on what happened here, both for any future phases of the project or more generally for other future projects.

Some aspects to consider when forming recommendations:

1. **Was the non-conformity resolved appropriately quickly according to its severity** (immediately, within a sprint review, within a sprint retrospective, etc.)? Did waiting to resolve it cause issues that could have been avoided if it were resolved more quickly? Did taking time to resolve it quickly disrupt other work, when resolution of this could have waited?  
2. **Not all non-conformities require recommendations for change**. Sometimes unexpected occurrences happen and the existing procedures handle everything as well as possible.  
3. **The more severe the consequences, and the more issues which are still outstanding, the more weight should be given to considering recommendations for the future**, either in how to avoid this type of issue or to handle it better.

The Project Non-conformities document should be considered within the Lessons Learned activity.  
