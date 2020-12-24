# Global Metadata

## Constraints
- [desired] Minimize overhead

## Tolerances
- The system should tolerate teams from 1 member to a few hundred

## Uncertainties
- Pull request review
  - Who reviews normal team pull requests? (Keeper, Sage, Scribe, literally anyone)
  - Who reviews pull requests for subassemblies coming into a larger branch/assembly?
  - Who reviews pull requests for systems/assemblies coming into master?
- What is the exact framework for test documentation?
- What is the framework for the issue tracker?
  - What information does it need to have?
  - How does it integrate with system metadata?
- Does the section on team structure need an example?
  - Should that be inline, or in the supplemental repo?
- The team structure section isn't very clear that DDD teams are autonomous and don't need or have traditional management oversight
- We want to communicate that traditional management structures are usually a lot of overhead for little benefit
- Are there any other Brass roles we should define?
  - Battlemaster equivalent? (Since we have the Quartermaster)
- Use transparency to remove the need for recursive "whip-cracking" behavior. (Many companies do this to ensure Work Is Done:tm:.) How to make this clear?
  - VCS contains the past, key uncertainties contain the future
  - Issue tracking contains things that need to be done, but do not require discussion or debate. This includes both things that are already discussed, but need to be finished out, and things that are so small an simple to not merit discussion at all (like tiny bug fixes)
- System for performing aftercare (to help with difficult design discussions). Do we even need this?
  - Do we want safewords?
- What is the expected audience we are writing this guide for? Other software engineers? Business people? Laypeople?
- Somewhere we need to make clear that a **project** contains one or more **teams** which contain several **crew members** and other roles
- In a multi-team project, which team is responsible for guidebook updates that affect everyone (such as changes to the code style guide)
  - Handled at the check-in?
  - Handled by the highest team?
  - Proposed, then must be accepted by all teams?
  - Anyone can modify at any time?
- Should we use the term "system worldbuilding" instead of metadata?
- Projects will occasionally call in freelance work, because of skill holes in their team. What framework should we provide for this? Should we provide any?
- Should we have a mascot? Like ferris, the rust crab
- Currently, we have 3 "refresh-like" actions (Calling a refresh, the "meta-refresh", and the check-in). How can we better unify these systems?
- We need a system to have the Librarian/Scribe/Someone else(?) review the documentation and clean it up.
- Should the automation section be part of the principles, or should it be standalone?
  - Should include that if you automate testing and data analysis tools, and open them to the team, you don't need the overhead of data scientists and manager approval to run these tests (only to spit out reports that most people don't even understand).
- We should have a place in the DDD system where teams can define their internal reserved words/jargon (ex: "system metadata", "closed loop", etc.)
- Weirdness with key uncertainties system
  - We need some kind of workflow for when someone has an idea that might improve a system, but that isn't inherently tied to a problem or question in the key uncertainties. (Make a "should we..." uncertainty, and then make a proposal for it, Make a proposal without a related uncertainty)
  - We need a system to link proposals to uncertainties
  - Some key uncertainties are of the form "should we do [thing]?". How do we handle proposals which simply say "no, we should not"
- We need a proposal status between "accepted" and "fully written and all the additional steps have been followed"
- Many problems often start with some non-trivial requirements gathering. Should we have a system for this?