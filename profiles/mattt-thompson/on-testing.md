# Mattt Thompson — On Testing

## Documentation-Driven Testing

Thompson's testing philosophy connects directly to his documentation discipline: a test is a form of documentation. A test named `testFetchingUserWithInvalidTokenReturns401` documents that the function handles a 401 response. A test named `testFetchUser3` documents nothing. The discipline: write test names that a reader could use to understand the system's behaviour without reading the implementation.

The testing standard: the test suite should be human-readable documentation of the system's behaviour. If the test names and test structure do not describe the system clearly, both the tests and the documentation have failed.

## Test at the Public Interface

Thompson's NSHipster principle — "understand before using" — extends to testing: test a module at its public interface, not its private implementation. A test that reaches into private internals to verify implementation details will break when the implementation changes, even if the public behaviour is unchanged. The test is coupled to the wrong thing.

The testing discipline: the unit under test is the public interface. Every test should call public methods and assert on public outputs. Private methods are tested indirectly, through the public methods that call them. If a private method is so complex that it seems to need its own test, that is a signal to make it a separate, independently testable component.

## HTTP API Testing: Test Against a Real Server

Thompson's backend testing philosophy: test HTTP API clients against a real API server, not against a mocked response. The differences between a mocked response (perfect JSON, correct status code, no network latency, no timeouts) and a real API (imperfect JSON, unexpected status codes, network errors, timeouts) are exactly the failure modes that matter in production.

The testing discipline for network code: use a local API server or a recorded session (VCR-style) for tests. Never assert only against a mock — mocks verify that you called them correctly, not that you handled their real-world behaviour correctly.

## Alamofire's Testing Infrastructure

Alamofire's test suite is itself a reference for iOS networking testing. It includes a local server (built on top of Vapor) that the tests run against, a set of response types designed to test specific HTTP scenarios (slow responses, redirects, authentication challenges), and assertion helpers specific to HTTP responses.

The testing pattern: when testing networking code, the infrastructure investment is the local server. With a controllable server, you can test every HTTP scenario — not just the happy path, but the error paths that occur in production but are hard to reproduce with a real server.

## Test Naming and the Failing Test Message

Thompson's test naming discipline: a failing test should be self-explanatory without reading the test body. The failure message "XCTAssertEqual failed: ("nil") is not equal to ("John")" tells you nothing. The test named `testUserProfileName_returnsFirstAndLastName_whenBothArePresent` tells you exactly what broke.

The testing standard: name tests as three-part descriptions: the method or behaviour being tested, the condition under which it is being tested, and the expected result. When the test fails, the name is the bug report.

## Sources
- [NSHipster — nshipster.com](https://nshipster.com/)
- [Alamofire — GitHub, tests directory](https://github.com/Alamofire/Alamofire)
- [Swift API Design Guidelines — naming conventions](https://swift.org/documentation/api-design-guidelines/)
- [XCTest documentation — Apple Developer](https://developer.apple.com/documentation/xctest)
