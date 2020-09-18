# How to Conduct Your Tests [stub]

- There should be a system for this
- There should be stuff in the guidebook for conducting tests
- Generally prefer the lightest environment when testing. Literal pen and paper is typically superior. However, some tests may require (or be easier) to do with other software tools or small code prototypes. Some testing tools can be reused after created. This may be a worthwhile investment.

The final test documentation system must contain the following information for each test:
- Short, descriptive, relatively unique name
- Why was this test ordered?/What is this testing?
	- For lab tests: a simple sentence describing the ambiguitiy it is resolving
	- For unit tests: “Unit test for `[PROPOSAL NAME](link/to/proposal)`”
- Who ordered this test? When?
- Who conducted this test? When?
- What was the procedure?
- What were the test results?
- What type of test is this? (Lab, unit, integration?, proposal)

The final test documentation must be able to handle the following cases for information to be filed in it:
- Lab tests: Parsimonious
- Unit tests: Testing a specific proposal or subsystem. Involves testing for desired behavior and integration with other parts.
- Rejected proposals: That were axed, but didn't fail their unit tests
