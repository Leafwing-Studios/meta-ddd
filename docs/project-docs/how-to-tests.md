# How to Conduct Your Tests [stub]

All tests are documented. 

### Metadata

#### Constraints

- [required] Documented tests must have the following information
  - Short, descriptive, relatively unique name
  - What type of test is this? (Lab, unit, integration?, proposal)
  - Why was this test ordered?/What is this testing?
  	- For lab tests: a simple sentence describing the ambiguitiy it is resolving
  	- For unit tests: “Unit test for `[PROPOSAL NAME](link/to/proposal)`”
	- Who ordered this test? When?
  - Who conducted this test? When?
  - What was the procedure?
  - What were the test results?
- [various] Must be able to handle the following types of tests:
  - [required] Lab tests: Parsimonious
  - [required] Unit tests: Testing a specific proposal or subsystem. Involves testing for desired behavior and integration with other parts.
  - [expected] Rejected proposals: That were axed, but didn't fail their unit tests
- [expected] Should prefer the lightest environment possible when testing.
- [expected] Should incentivize heavier environments when they are needed, and especially if the work in the heavier environment can be reused

#### Tolerances

- TMP

#### Uncertainties
- What is the exact framework for test documentation?
- Should the default guidebook contain information on test procedure (Similar to the PR steps)? What information is important to provide?