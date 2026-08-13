# Terms of Reference for the SRSG Process Working Group

[Back to Context of the Organisation](./context_of_the_organisation.md)

## Purpose

The purpose of the SRSG Process Working Group (PWG) is to set the Strategic Direction for the development and execution of Processes within the Southampton Research Software Group (SRSG).

## Duration

The PWG is intended to be a perpetual persistent feature of the SRSG and therefore the PWG will exist in some form for as long as the SRSG exists.

## Changes

These Terms of Reference may be changed at any time by the SRSG Directors. Any changes should be made with the agreement of the PWG.

## Membership

Membership of the PWG is open to all members of the SRSG and invited external persons. There are no specific restrictions on the number of PWG members. Individuals within the SRSG may volunteer themselves to work on the PWG or may be requested to join the PWG to accomplish a specific task. There is no fixed term of service, that is, members may choose to join and leave (and potentially rejoin) at any time.

The PWG shall self select a member to Chair PWG meetings. The PWG Chair shall ensure that appropriate records of meetings are kept. The Chair may delegate record keeping to a nominated Secretary.

## Accountability

The PWG is Accountable to the SRSG Directors. The SRSG Directors will agree the Vision and set Objectives for the PWG.

In case of disagreements between PWG members and the SRSG Directors then the views of SRSG Directors shall take precedence on all matters.

It is desirable that at least one SRSG Director should be a member of the PWG at all times. It is desirable that at least one SRSG Director should attend PWG meetings. 

## Budget

The PWG has no allocated budget. All anticipated effort and expenses associated with any PWG initiated work shall be agreed with the SRSG Directors prior to commencement.

## Working Method

The PWG should meet once a month to discuss the Strategic Direction of process work within the SRSG. A quorum of 3 people, including either the Chair or an SRSG Director, should be present at PWG meetings. The Chair may appoint a Secretary to take notes during the meeting. The PWG may task individuals or groups of people within the SRSG to perform offline tasks (provided that broad approval to do so has been received from the SRSG Directors).

It is essential that SRSG Processes are owned by the whole of the SRSG. To enable this the PWG shall actively consult with members of the wider SRSG and regularly (nominally every few months) report back to the wider SRSG. This reporting may be done, for example, during the Weekly Meeting or at an All Hands Meetings. The PWG shall make all records of meetings available to all SRSG members (for example, minutes of meetings being made available via Google Documents).

## Process Change Control Board (CCB)

A key Responsibility of the PWG is to create and maintain the SRSG Quality Management System (QMS). To facilitate this, the PWG shall oversee the work of a Process Change Control Board (CCB).

The Process CCB will have delegated authority with regard to managing the QMS (which may be overuled by the PWG). The Process CCB shall perform the day to day management of the QMS by adding, updating and deleting parts of the QMS as necessary.

The responsibilities of the Process CCB include:

- Assessing Change Requests (CRs). In principle, anybody can raise a CR on the QMS. The CRs will be documented in the form of GitHub Issues. Where necessary the Process CCB shall obtain clarifications from the person who raised the CR.
- Prioritising and sanctioning the CRs for work. Effectively acting as a Product Owner, the Process CCB shall organise the CRs into a ranked list and identify the next CRs to be progressed.
- Reviewing and approving the actual changes made. That is, reviewing and merging Github Pull Requests related to a CR.

The main communication lines and responsibility chain of the Process Working Group are as follows, to further highlight the position and role of the CCB.

```{mermaid}
block-beta
  columns 3
  dir("SRSG Directors"):3
  space blockArrowId1<[" "]>(y) space
  pwg("Process Working Group"):3
  blockArrowId2<[" "]>(y) space blockArrowId3<[" "]>(down) 
  ccb("Change Control Board") blockArrowId4<[" "]>(x) pl("Process Area Lead")
```

In this diagram, the "Process Area Lead" refers to the person of persons designated to lead the development of a specific area of the process documentation, and act as the reviewer(s) of any changes made by the CCB to documents covering their given area(s).

## GitHub Guidelines for CRs

Any modifications to the GitHub repository containing these process documents shall follow the guidelines set out below, in order to maintain a comprehensive commit history and ensure that any and all modifications to the processes have been agreed upon and reviewed by the relevant people and/or groups.

- Each CR shall take the form of a GitHub Issue and at least one Git branch.  The branch name shall start with the number of the issue in order for the two to be associated with each other.
- For more complex CRs, the CR may be decomposed into several issues, each of which is accompanied by a matching Git branch to be created from the branch associated to the original CR issue.
- Issues associated with a CR may be created either by the person to raise the CR or by a member of the CCB.  The associated branch shall be created only by a member of the CCB.
- When a CCB member assesses that a CR-related Git branch is ready to merge into the Process Documents proper, they shall create a Git Pull Request (PR).  The PR shall be reviewed by (at minimum) one additional member of the CCB and the lead for the associated Process Working Group.
- No changes shall ever be pushed directly to the GitHub Main branch.  All changes shall have an associated CR, Issue, Branch and reviewed PR.
- All Git commits should be atomic, and shall have a commit message explaining the change(s).  Each commit does not need to contain a complete change, i.e. it is fine for a CR's branch to consist of multiple commits so long as each commit is sufficiently documented.  Each commit message should start with a `#` followed by the number of the associated CR's associated GitHub issue.
