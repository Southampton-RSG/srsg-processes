# Appendix: Verification Methods, Classes and Levels

## Purpose

This supplementary document lists non-exhaustive examples of different methods, classes and levels of verification which may be helpful when selecting verification methods for a project which are recorded within a Verification Procedures document.

## Methods of Verification

All project outputs must be verified in some way, irrespective of the type of output. At a high level, these methods typically include:

- **Testing** conducted by project team members either manually or using automation, e.g. manual software testing against a test plan, running a suite of automated unit or functional tests, integration testing.  
- **Review** of any project output, e.g. code or document review.  
- **Measurement** of quantitative properties of an output against specifications, e.g. performance benchmarking.  
- **Product demonstrations** conducted by either internal team members or customers, e.g. from internal team members to customers, or customers to a potential community of users.  
- **Analysis** using evaluation and reasoning to demonstrate correctness, e.g. static code analysis.

Depending on the scale, type and complexity of the project, only some of these may be used. For example, for a small scale single developer project code, review by a third party may not be warranted or tractable.

## Verification Classes

The following are example classes \- or types \- of verification that may be used depending on the nature of the project:

| Class |  Description  |
| :---- | :---- |
| Architectural / Design Verification | Verification of an architecture or design against its intended operating environment and purpose. Significant design decisions should be reviewed with a suitably experienced colleague |
| Functional Testing | Verification that the software, data product or analysis behaves according to the defined requirements |
| Interface Conformance Testing | Verification that interfaces, inputs and outputs conform to expected requirements |
| Regression Testing | Verification that previously resolved defects have not been reintroduced |
| Performance Testing | Verification of performance-related non-functional requirements  |
| Reliability Testing | Verification of behaviour under expected operating conditions over time |
| Stress Testing | Verification of behaviour under unusually high workloads |
| Usability Testing | Verification that users can understand and use the product effectively |
| Documentation Testing | Verification that the documentation correctly and sufficiently supports both users and developers |
| Security Testing | Verification of security requirements and controls |
| Platform Testing | Verification that the product operates correctly on supported platforms and environments |

## Software Verification Levels

We commonly use the following levels of testing verification for software projects:

| Level | Description | When Conducted |
| :---- | :---- | :---- |
| Unit Testing | Verification of the smallest practical unit of software typically at function or module level. | Ideally written as code is developed and finalised. Where this is not possible due to practical constraints, it should be completed as soon as practical afterwards. |
| Integration Testing | Verification that components work together correctly and produce the expected behaviour. | Conducted throughout the development, often towards the end of a sprint. |
| System Testing | Verification of the complete system within its intended operating environment. | Ideally performed alongside integration testing. Where target environments are not available, it should be planned and scheduled at suitable project milestones. |
