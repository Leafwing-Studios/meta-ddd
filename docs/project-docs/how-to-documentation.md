# How to Write Your Documentation [stub]

In this bit we're gonna talk about strategies for writing good documentation and stuff

## General to Specific

I'm not sure if this deserves it's own section. It's best to start with a general overview of the thing, then get more specific as you go on, sometimes reiterating the same pieces more than once. Introduction chapter is the highest overview, then chapter intros are more specific, and so on and so on.

## How Detailed, and When?

A natural question is to ask: how detailed should the documentation be at each point in the project's life? In DDD, documentation detail comes in two stages. During the prototyping phase, the systems are specified to the extent that is needed to unit test them on paper. During the build phase, the specific implementation details are filled in, the feature is marked with the appropriate status, and the code and documentation are linked up to each other. The documentation updates are made as part of the development, and the documentation gets more detailed as those specific details are hammered out in code.

At some level, the code is the most detailed and the most specific record of how a system works. It is the lowest level of the detail hierarchy.

<div class="infobox">

**Examples in Documentation**

Docs should have examples for clarity when possible/needed. These are still just as useful after the code is written. Examples of use cases or runtime behavior are really useful. If your documentation system supports infoboxes, use those for examples.

</div>

## Documentation in Code Review

In code review, the documentation is reviewed as closely as the as the code is. This is part of why it's so important that the documentation is version controlled, and that it's in the same repository as the code. It is *part* of the review process, and a pull request cannot be accepted unless all the code *and* documentation updates are complete. During review, the ROLE should explicitly perform the following things:
- Follow the code review guide from the project's guidebook
- Code and documentation must adhere to the guides in the guidebook
- Overrides are talked about in the guidebook section
