# Metadata

The **metadata** of a system or project is the design information that describes the system from the designer's point of view. This includes information about:

- **what they system was aiming to do**
- **what rules it must follow** in its design
- **what functions it must be able to accomplish**
- **what things would be "nice to have"** for the system
- **how robust the system is to changes around it**

Every system has associated metadata, which should be stored alongside the system's **definition.** Ideally, these should be in the same file. Metadata generally does not dictate precisely how a system works, but how the system _should_ work. It defines properties and goals that the system ought fill, but it doesn't specify an exact design to fill those goals. Designs are created when [writing proposals](/link).

Additionally, there is some metadata that is stored _globally_. This is for things that reach across the whole project, such as uncertainties about systems that haven't been made yet, or the projects overall goals. Metadata generally functions and "looks" the same whether it is global or not, but the two locations operate on a different level of abstraction. Global metadata is typically stored in the Guidebook, but it doesn't have to be.

Naturally, there is some overlap between the various metadata fields. This is ok, and crew members should "go with their gut" when sorting something into a metadata field, as the system is tolerant to small ambiguities in metadata classification.

The metadata framework is as follows:

## Constraints
_Dig your holes before you fill them_

**Constraints** are a list of rules that the system must follow. These include both things the system is _not_ allowed to do, and things the system _must_ be able to do. Together these define the intended function and limitations of the system. Notably, constraints are _inherited,_ where other metadata properties generally are not. This means that constraints in the global metadata must be followed by all systems.

Every constraint in the list is labeled as either **required, expected,** or **desired,** which indicate how flexible the constraint is. We recommend ordering constraints by flexibility.
- **Required:** The system must have this property or follow this rule
- **Expected:** The system doesn't _need_ to have this property, but it should if reasonable to do
- **Desired:** The system doesn't need this property, but it would be nice to have

It is important to not only the goals of the system, but what boundaries it must work within. Constraining the design space in this way forces better solutions, and makes the problem easier to get a handle on. Through constraints, large, complex problems are broken down into more manageable pieces. The constraints give designers something to hold on to when starting to scaffold the system. It's much easier to fill a hole after you've dug it.

<div class="infobox">

**Constraints Examples**

- The system can never use more than 10000 rows in the database [required]
- The system must follow the _code style_ guide (typically inherited from the global metadata) [required]
- The system should provide a place for test results to be documented [required]
- The system cannot have many call sites in the code [expected]
- The system must only use 4 basic arithmetical operations, so it is easy to understand [expected]
- Cycle efficiency is more important than memory efficiency [desired]
- The user should be able to change their color scheme [desired]
- The system should use the X library, since other systems are already using it [desired]

</div>

## Tolerances

_If you can't make it perfect, at least make it adjustable_

**Tolerances** are all about how robust the system is to changes around it, defining its range of operation. The term comes from engineering, where it is defined as "[the] allowable amount of variation in a specified quantity, especially in the dimensions of a machine or part." In short, tolerances list which variations (in the rest of the project) are acceptable, and which ones are not. As mentioned, there is some overlap between categories, and some tolerances may be defined in the required properties, indicating that the system must be tolerant to certain conditions.

Some useful questions when trying to find tolerances of a system:

- What assumptions does this system make about the rest of the project's structure?
- What are the maximum and minimum values that this system can handle (for example, considering integer overflow limits)
- What different formats can this system accept in its input?
- Which parts of the architecture is this system independent from?
- Which parts of this system can be easily changed to suit future needs?
- What use cases was this system designed to handle, and what is it unable to handle?
- What are the circumstances under which this system could break?

<div class="infobox">

**Tolerances Examples**

- This system assumes that there will never be more than 100 users connected to the server at the same time.
- This system can load data in the `.json` and `.csv` format, but not in the `.sql` format
- Changing `experiencePerLevel` field adjusts the overall pacing for character advancement, without any other changes needed. `experiencePerLevel` can accept any value between 1 and `UNSIGNED_INT_MAX`, inclusive.

</div>

## Uncertainties

_What do we still need to figure out?_

**Uncertainties** are open questions, problems, and requirements that have yet to be addressed. Notably, this is _not_ a list of tasks to be completed. The uncertainties are for issues that need to be discussed. The team refers back to this list(s) when determining what to write proposals for, and what to discuss during design meetings.

Unlike other metadata fields, uncertainties look a little different depending on whether they are part of the global uncertainties, or a system's uncertainties.

| Location | What do the uncertainties look like?                                                                            |
| -------- | ------------------------------------------------------------------------------------------------------------------- |
| Global   | Functionality that needs to be designed, potential avenues for improvement, open questions about architecture, etc. |
| System   | Smaller bugs in the system, holes in the system that need to be filled, technical unknowns, etc.                    |

<div class="infobox">

**Uncertainties Examples**

- The project is lacking a system to handle X user case
- Proposal Y has a problem in it that needs to be addressed
- Should we include functionality to do Z? If so, how would that system look?

</div>

### Metadata

Metadata for the metadata documentation system

#### Constraints

- Cannot require an external system [required]
- Must be able to easily list per system, and globally [required]
- Must be able to contain all design information that the team may need to reference back to [required]
- Metadata should live with the documentation should live with the code [required]
- Doesn't require its own database [expected]
- Same framework for global and system-specific metadata [expected]
- Shorter is better. Remember, low overhead [desired]

#### Tolerances

- Does not require rigorously defined differences between metadata categories
- Assumes expansion/detraction from the metadata fields list will be infrequent (as it is a costly operation)
- Works with systems at nearly any level of abstraction
- A system and its metadata can be defined in either order

#### Uncertainties

- What additional metadata do proposals need? (Special tasks or Refreshes called for on acceptance, Help needed, Justifications?, others?, Uncertainties Solved?)
- Often, when writing out uncertainties, they have a few obvious paths forward to investigate. How should these paths be documented? (In uncertainties in parenthesis, on the proposal's stub)
- Should uncertainties have UUIDs for reference in external systems (and in proposals)? How would we go about this scalably?
- How do we ensure visibility for inherited properties?
- Do tolerances contain the tolerances and assumptions of this system, or do they contain the stuff that the system gets for "free" from outside? Should we have both of these?
- Should there be an explicit "goals" section of the metadata?
