# Metadata

The **metadata** of a system or project is the design information that describes the system from the designer's point of view. This includes information about:
- **what they system was aiming to do**
- **what rules it must follow** in its design
- **what functions it must be able to accomplish**
- **what things would be "nice to have"** for the system
- **how robust the system is to changes around it**

Every system has associated metadata, which should be stored alongside the system's **definition.** Ideally, these should be in the same file. Additionally, there is some metadata that is stored *globally*. This is for things that reach across the whole project, such as key uncertainties about systems that haven't been made yet, or the projects overall goals. Metadata generally functions and "looks" the same whether it is global or not, but the two locations operate on a different level of abstraction. Global metadata is typically stored in the Guidebook, but it doesn't have to be.

An important distinction is that metadata generally does not dictate precisely how a system works, but how the system *should* work. It defines properties and goals that the system ought fill, but it doesn't specify an exact design to fill those goals. That work comes in [writing proposals](/link).

Naturally, there is some overlap between the various metadata fields. This is ok, and crew members should "go with their gut" when sorting something into a metadata field, as the system is tolerant to small ambiguities in metadata classification.

The metadata framework is as follows:

## Key Uncertainties
*What do we still need to figure out?*

**Key uncertainties** are open questions, problems, and requirements that have yet to be addressed. Notably, this is *not* a list of tasks to be completed. The key uncertainties are for issues that need to be discussed. The team refers back to this list(s) when determining what to write proposals for, and what to discuss during design meetings.

Unlike other metadata fields, key uncertainties look a little different depending on whether they are part of the global key uncertainties, or a system's key uncertainties.
Location | What do the key uncertainties look like?
--- | ---
Global | Functionality that needs to be designed, potential avenues for improvement, open questions about architecture, etc.
System | Smaller bugs in the system, holes in the system that need to be filled, technical unknowns, etc.

<div class="infobox">

**Key Uncertainties Examples**

- The project need a system to handle the X user case
- Proposal Y has a problem in it that needs to be addressed
- Should we include functionality to do Z? If so, how would that system look?

</div>

## Design Constraints
*Dig your holes before you fill them*

**Design constraints** are a list of things that the system's design is *not* allowed to do. These constraints may be in place for technical reasons, for design reasons, for unification, or to better fit the **properties** of the system. Whichever the case, the system must obey all of its design constraints (although teams are allowed to remove constraints when prototyping). Notably, design constraints are *inherited,* where other metadata properties generally are not. This means that design constraints in the global metadata must be followed by all systems.

<div class="infobox">

**Design Constraints Examples**

- The system can never use more than 10000 rows in the database
- The system cannot have many call sites in the code
- The system must follow the *code style* guide (typically inherited from the global metadata)
- The system must only use 4 basic arithmetical operations, so it is easy to understand

</div>

## Required Properties
*What we need it to do*

The **required properties** of a system are, simply, the things that the system must be able to do. These are, in some sense, the opposite of the design constraints. These can sometimes be thought of as the goals or function of the system.

<div class="infobox">

**Required Properties Examples**

- The system must accurately calculate the distance between two objects
- The system must take input in X format

</div>

## Desired Properties
*What we want it to do*

The **desired properties** of a system are properties that would be nice to have, but are not required. This generally includes optimization criteria, additional non-essential functionality, and any other subjective preferences on how the system should be put together. The only difference between required and desired properties is that desired properties are flexible, but required properties are not. Some project opt to store these properties in a single "properties" metadata field, and then tag each one as "required" or "desired". 

<div class="infobox">

**Desired Properties Examples**

- Since this system runs in the main loop, cycle efficiency is very valuable
- The user should be able to change their color scheme
- The system should use the X library, since other systems are already using it

</div>


## Tolerances
*If you can't make it perfect, at least make it adjustable*

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

### Metadata
Metadata for the metadata documentation system

#### Key Uncertainties
- What additional metadata do proposals need? (Special tasks or Refreshes called for on acceptance, Help needed, Justifications?, others?)
- Often, when writing out key uncertainties, they have a few obvious paths forward to investigate. How should these paths be documented? (In key uncertainties in parenthesis, on the proposal's stub)
- Should key uncertainties have UUIDs for reference in external systems (and in proposals)? How would we go about this scalably?
- How do we ensure visibility for inherited properties?
- What are some more examples?

#### Design Constraints
- Cannot require an external system

#### Required Properties
- Must be able to easily list per system, and globally
- Must be able to contain all design information that the team may need to reference back to

#### Desired Properties
- Shorter is better. Remember, low overhead
- Same framework for global and system-specific metadata

#### Tolerances
- Does not require rigorously defined differences between metadata categories
- Assumes expansion/detraction from the metadata fields list will be infrequent (as it is a costly operation)
- Works with systems at nearly any level of abstraction
- A system and its metadata can be defined in either order