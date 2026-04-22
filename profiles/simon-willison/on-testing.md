# Simon Willison — On Testing

## The Perfect Commit Includes a Test

Willison's "perfect commit" standard makes testing non-negotiable: a commit that fixes a bug without adding a test that would have caught the bug is not a complete commit. The test is part of the change, not a follow-up task. Without a test, the bug can be reintroduced by a future change without detection.

The testing discipline: when fixing a bug, write the test that catches the bug first. Verify the test fails. Apply the fix. Verify the test passes. Commit the test and the fix together. The commit message explains why the bug occurred; the test documents that it was fixed.

## Tests Against Real Databases, Not Mocks

Willison's backend testing philosophy: tests that run against a real database engine find bugs that tests against mocks cannot find. SQLite, PostgreSQL, and MySQL differ in edge case behaviour around NULL handling, string collation, integer overflow, and transaction isolation. A mock that returns perfect SQL results never finds these differences.

The testing discipline: run tests against a real database. Use SQLite for fast local tests (it spins up in milliseconds, requires no server, and can be in-memory). Use the production database engine in CI. Tests that find a bug only in PostgreSQL are useful bugs to find.

## Datasette's Testing Pattern: CLI and HTTP

Datasette's test suite tests the application at two levels: the Python API (unit tests for individual functions and classes) and the HTTP API (integration tests that start a local server and make real HTTP requests). The HTTP tests verify that the full stack — routing, authentication, database queries, JSON serialisation, caching headers — works correctly end to end.

The testing pattern: for web applications, write tests at the HTTP level. An HTTP test that sends a GET to `/api/users` and verifies the JSON response exercises the full stack simultaneously. It is slower than a unit test and finds different bugs — both are necessary.

## Document Your Examples: Doctest and Executable Documentation

Willison uses Python's doctest module extensively: embedding example usage directly in docstrings, then verifying that the examples produce the correct output. The documentation is the test. If the documentation example is wrong, the test fails.

The testing discipline: every code example in documentation is a maintenance liability unless it is executed as a test. Use doctest, pytest-doctest, or equivalent to execute documentation examples in CI. A documentation example that does not run is a documentation example that will eventually be wrong.

## Testing AI-Powered Features: Evaluation as Testing

Willison has written about the testing challenge of LLM-powered features: you cannot write a traditional unit test for a function that calls an LLM, because the output is non-deterministic and depends on a model that changes. The correct testing approach is evaluation: a dataset of inputs with expected outputs, scored against quality criteria, run against the current implementation.

The testing discipline for AI features: define what "good" looks like before building. Create a representative dataset of inputs. Score outputs against criteria (correctness, relevance, tone). Run evaluation in CI with a threshold — if the pass rate drops below X%, the evaluation fails like a test. This is not a traditional test, but it is the closest analogue that works for LLM-powered code.

## Sources
- ["The Perfect Commit" — simonwillison.net](https://simonwillison.net/2022/Oct/29/the-perfect-commit/)
- [Datasette — GitHub, tests directory](https://github.com/simonw/datasette)
- [simonwillison.net — testing and AI evaluation posts]
- [Python doctest module documentation](https://docs.python.org/3/library/doctest.html)
