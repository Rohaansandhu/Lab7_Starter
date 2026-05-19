## 1.

Automated tests should be put into a Github action so that it can be on a standardized and consistently testable environment. By having the tests run in a Github action, we can ensure that no code is merged before having passing tests. You should also manually run them before pushing code, but you definitely need the Github action tests for consistency with environments and between developers.

## 2.

No, for an individual function you would only need a unit test to ensure that when given correct inputs it gives the correct output (or given bad inputs it fails appropriately). End to end tests should involve multiple functions working in tandem.





