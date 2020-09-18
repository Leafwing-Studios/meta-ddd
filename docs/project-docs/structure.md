# DDD Project Structure

## Key Uncertainties
At all times, the team keeps a list of the open questions and problems to be addressed, called **key uncertainties.** These might be things like “we need a system to handle X” or “Y proposal has a problem with it that needs to be addressed”. The team refers back to this list periodically when determining what to write proposals for, and what to discuss during design meetings. The key uncertainties are for information that needs to be discussed, and problems that need proposals written for them. Smaller changes and issues should be managed in the [Issue Tracker]().

## Code and Documentation
The code and the documentation for a DDD project are stored in tandem. Code is stored in a repository, with the documentation for that code in the same repository. The documentation does not have to follow the structure of the code, but it must be clear how different pieces of documentation and code relate to one another. For example, the documentation for a project may be contained in a root level `docs` folder, with the remainder of the project in a `code` folder next to it.

The documentation itself must have the following features:
- Markings for each feature/subheading to indicate status. For example: Planned, In-Progress, Completed.
- Organizational structure that makes sense conceptually. Putting a bunch of separate design documents into a single folder is not sufficient. Pages must be able to be grouped and linked between easily
- Searchability, both by document name, document headings, and document text. (Ideally prioritizing in that order.)
- The documentation must be able to be versioned in your VCS of choice. Markdown documentation builders such as [docsify](https://docsify.js.org/#/), [MkDocs](https://www.mkdocs.org/), and [Docusaurus](https://docusaurus.io/en/) are great options for this (at time of writing).

Additionally, the DDD system benefits from the following documentation features, although they are not required:
- Markdown highlighting for *italic* and **bold** text
- Ability to include tables and charts
- Infoboxes for small asides
- Ability to mark sections as stubs, indicating that they are not finished and need expanding

## Version Control System
The project's version control system, or VCS is software that manages different versions of a single piece of software, with features for concurrent feature branches and tools for merging branches together. The most popular VCS platform is [Github](https://github.com/). The VCS branch structure of a DDD project should branch by subassembly (if any), then by individual features. Code should never be committed directly to the *master* branch. 

When merging in a branch, the *pull request* must be reviewed by the team's [keeper](). These both ensure code quality, and ensure the documentation is being kept up to date for all features, no matter how small. Pull requests should be merging up **one level at most.** Branches that are used for lab tests, unit tests, or failed proposals are never merged up to the parent branch, but they should be pushed to the remote server for record keeping.

<div class="infobox">

**Additional Accountability: Personal Branches**

Optionally, DDD teams may want to include a branch for each team member. When doing this, members move their branches to be children of the current feature branch they are working on. All that employee's changes are done on their branch, then they make a pull request to the feature branch. These are useful for:
- Tests and experiments that shouldn't be pushed up
- Doing pull requests and review on a more granular level
- Constructing proposals using the main documentation system

</div>

## Issue Tracking [stub]
Small things that need to be done that don't need discussion on solutions. May use more than one system/platform. Used for:
- "This proposal has been accepted. Write it up proper in the documentation. Assigned to Alice."
- "There is a bug on this screen in the UI. Bob should fix it and make a pull request."
- "We need to be able to add tables to our documentation, but the current tooling is insufficient. Scribe Charlie to contact Librarian Denise about the new functionality."
- Endpoint for end users to report bugs and make feature requests.

## Test documentation
Unit and lab test are documented in their own system. Must be searchable. Each test record must contain the following information (at least):
- Short, descriptive, relatively unique name
- Why was this test ordered?/What is this testing?
- Who ordered this test? When?
- Who conducted this test? When?
- What was the procedure?
- What were the test results?
- What type of test is this? (Lab, unit, integration?, proposal)

The framework as a whole must be able to handle:
- Lab tests: Parsimonious tests for specific questions or uncertainties, especially technological limitations.
- Unit tests: Testing a specific proposal or subsystem. Involves testing for desired behavior and integration with other parts.
- Rejected proposals: That were axed, but didn't fail their unit tests

## The Guidebook

**The Guidebook** is the documentation for all the teams **Guides.** This system holds information which is uncovered and important, but not specific to a single system or test. Guidebooks are talked about more in [SECTION](). The important thing to understand right now is that they're stored in their own organizational scheme, although the exact organization is not terribly important. The Guidebook may be stored in an external system, but it is commonly part of the code documentation, in its own section at the end.

<div class="infobox">

**The Distributed Guidebook [stub]**

Instead of collecting the whole guidebook in one place, the guidebook may instead by **distributed.** Assimilation does this. Constraints, criteria, and key uncertainties are stored in the individual pages of their relevant systems, instead of a single place for all gudies and information. This has advantages (faster lookup) and disadvantages.

</div>
