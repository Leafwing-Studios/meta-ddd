# Global Metadata

## Constraints
- [expected] Build only what is necessary
- [desired] DDD should induce minimal overhead on the development team
- [desired] Prefer simple solutions over complex ones
- [desired] Prefer modular systems over entangled ones

## Tolerances
- DDD should tolerate teams from 1 member to a few hundred

## Uncertainties
- How do we handle introduction chapters? These are really useful for clarity, but mean documentation duplication. Furthermore, how should metadata be handled across an explanation tree, where systems are talked about in general in the intro, then in specific in their own pages?
- Use transparency to remove the need for recursive "whip-cracking" behavior. (Many companies do this to ensure Work Is Done:tm:.) How to make this clear?
  - VCS contains the past, key uncertainties contain the future
  - Issue tracking contains things that need to be done, but do not require discussion or debate. This includes both things that are already discussed, but need to be finished out, and things that are so small an simple to not merit discussion at all (like tiny bug fixes)
- System for performing aftercare (to help with difficult design discussions). Do we even need this?
  - Do we want safewords?
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