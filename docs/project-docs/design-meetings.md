# Running Design Meetings

**Design Meetings** are core to the DDD process. These are the space where the team discusses proposals, and works together to find the best solutions. They are, in many ways, the most difficult part of DDD, and the hardest to get right. 

## Phases and frequency

DDD projects have 2 distinct phases: **prototyping** and **build.** During the prototyping phase, the teams are working on documentation, conducting small tests, and churning through proposals. Once the documentation is well-defined and stable, the team enters the build phase, where the product is actually made, and code is written. 

During prototyping, design meetings are frequent (about daily) and long (several hours, with short breaks). The team is working almost exclusively to develop the documentation, ensuring the system is functional before it is created.

During the build phase, design meetings need not be so much of the team's time. By this stage, the team should all trust that the documented system is sufficient and robust, and all that remains is actually finishing the thing. Design meetings should still be called regularly, to discuss issues discovered and any controversial implementation details. However, they can be much less frequent (about once a week) and a little shorter (about an hour). While design meetings during the build phase still require all participants, the non-engineers can expect to have more of their time allocated to other projects, as problems with construction are less likely to need their expertise.

## Design Meeting Structure

Here we define the structure for what work and which tasks are completed during, before, or after design meetings:

### Team members bring into design meetings:
- Constraints from your domain of expertise
- Desired properties or goals for systems to be constructed
- Proposals for systems or parts of systems
- Test results
- Issues discovered with active or accepted proposals
- New key uncertainties

### During design meetings, team members:
- Argue and debate over which proposals or methods are best
- Update proposals with new information or strategies
- Scrap proposals that did not work
- Uncover problems in systems that the team has already prototyped, **calling** for an addition to the key uncertainties
- Uncover uncertainties about the market, architecture, technology used, etc., **calling** for lab tests as needed
- Uncover related either domains which are not present at the table, or uncertainties that no one is knowledgeable about, **calling** for expertise as needed
- Accept proposals to the master documentation (ideally by consensus)
  - There cannot be any issues for this proposal in the key uncertainties
  - The team must define criteria for this system's unit tests, referring to the desired properties and any [entangled systems](link?)
  - Assign responsibilities for:
    - Fully writing up the accepted system and documenting it in the master documentation
    - Conducting unit tests as defined
- Discuss desired properties and constraints, determining if they should be added to the guidebook
- Discuss guidebook changes that may affect older systems, **calling** for a refresh if needed.

### Between design meetings, team members:
- Update documentation with accepted proposals
- Update the Guidebook with new properties
- Conduct refreshes on old systems
- Conduct lab tests
- Conduct unit tests
- Formulate proposals

## Design Meeting Actions
During design meetings any team member, at any time, may make any of the following **Calls**:
- **Call for an addition to the key uncertainties:** Adds a specific question or problem to the key uncertainties list. This should be used for things that need further discussion, not small tasks, as those belong on the [Issue Tracker](/)
- **Call for a lab test**: Define a single, small question to be resolved by a [lab test](/)
- **Call for expertise**: Bring in a source of information that isn't part of the team to use as reference. When calling for expertise, the findings must be verified by lab tests after research is finished. The exact expertise called may take many forms:
  - A member of the brass who can answer questions about available resources for the project
  - An expert in the field from outside the company
  - Literature, such as scientific studies or blog posts
  - Documentation from another, similar project
- **Call a refresh:** A **refresh** refers to the act of going back over older sections of the system and checking that they are still up to the standards of the team. These should be called regularly to ensure the entire system is up to the current standards, and to make sure that new changes don't inadvertently break older systems. Generally, refreshes are called under the following circumstances: 
  - New properties or constraints have been added to the Guidebook that older systems may not be following
  - An active system has been changed, and its [entangled systems](/) may be affected
  - A long time has passed since an older system has been looked at by anyone

### Metadata

#### Constraints

- TMP

#### Tolerances

- TMP

#### Uncertainties

- TMP