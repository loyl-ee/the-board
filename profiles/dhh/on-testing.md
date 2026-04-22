# DHH — On Testing

## Test-Induced Design Damage

DHH's most provocative contribution to the testing debate: Test-Driven Development, applied dogmatically, causes design damage. When developers write tests first and let testability drive architecture, the result is often code that is unnecessarily decoupled — interfaces and abstractions that exist only to enable mocking, not because the domain requires them. The test suite becomes the customer, not the user.

The testing principle: design should be driven by the domain and the use case, not by what is easy to test. If a design decision is justified only by testability (not by domain clarity, maintainability, or correctness), it is test-induced damage.

## System Tests Over Unit Tests

DHH has argued for system tests (integration tests that exercise the full stack) over unit tests for web applications. A system test that clicks a button and verifies the database was updated exercises every layer simultaneously: the controller, the model, the database query, the view rendering. A unit test that mocks the database exercises only the code path that calls the mock.

The testing discipline: for a web application, a test suite of system tests that exercise real user flows provides higher confidence than a test suite of unit tests that exercise individual methods. The system test finds integration bugs; the unit test finds logic bugs but misses integration bugs.

## The Mock Controversy

DHH has criticised the overuse of mocks. A test that mocks the database, mocks the email service, and mocks the external API is a test that verifies only that the code calls its mocks in the expected order. It does not verify that the code works. When a real database query changes behaviour, the mock does not catch it.

The testing principle: only mock what cannot be reasonably invoked in a test environment. External services with side effects (sending real emails, charging real credit cards) should be mocked. Databases, internal services, and filesystem operations should not — use a real test database, a real filesystem, and real internal services.

## Confidence, Not Coverage

DHH has rejected line coverage as a meaningful testing metric. 100% line coverage does not mean the code is correct — it means every line was executed by at least one test. A test that executes a line without asserting the correct outcome is not a useful test.

The testing principle: the goal of a test suite is confidence that the code does what it should. Measure confidence by asking: when this test suite passes, do I trust the code? If the answer is no — because the tests are too shallow, too mocked, or too disconnected from real user flows — the test suite has failed at its purpose regardless of its coverage number.

## The Testing Pyramid Is Upside Down for Rails Apps

DHH has argued that the conventional testing pyramid (many unit tests, few integration tests, fewer system tests) is wrong for Rails applications. Rails' conventions mean the framework handles much of what unit tests would verify. The unique value of Rails tests is in verifying the application-specific behaviour — which system tests exercise best.

The testing discipline for Rails: write system tests for the user-facing flows that matter most. Write unit tests for complex domain logic (models, service objects) that has no UI. Do not write controller tests — they test Rails' routing and rendering, which is already tested by the framework.

## Sources
- ["TDD is Dead. Long Live Testing." — DHH, 2014](https://dhh.dk/2014/tdd-is-dead-long-live-testing.html)
- ["Test-induced design damage" — DHH, 2014](https://dhh.dk/2014/test-induced-design-damage.html)
- [Rails Testing Guide — rubyonrails.org](https://guides.rubyonrails.org/testing.html)
- [Is TDD Dead? — DHH, Kent Beck, Martin Fowler conversation](https://martinfowler.com/articles/is-tdd-dead/)
