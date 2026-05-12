ShopperStack API Automation Project
End-to-end API testing suite with bug detection and performance monitoring

Postman
API Testing
Performance
Bug Detection
E-commerce
🔁
End-to-End Testing
⚡
Performance Monitoring
🐛
Bug Detection
📊
Automated Reports
What is this project?
For freshers: Think of an API like a waiter in a restaurant. You (the client) ask the waiter (API) for food, and the kitchen (server) prepares it. This project automates checking that the waiter delivers the right food, in the right time, every single time — without a human manually placing orders.

ShopperStack is a fictional/real e-commerce platform. This project tests its backend APIs — the invisible layer that handles user registration, product browsing, cart management, and order placement.

It validates that every API response is correct (right status codes, right data), within acceptable time limits, and catches regressions (bugs introduced by new code changes).

In a real company, a QA Automation Engineer or SDET (Software Development Engineer in Test) would own a project exactly like this.

Tech stack & tools
Postman / Newman
API test creation & CLI execution
JavaScript (Postman Scripts)
Pre-request & test assertion scripts
Git & GitHub
Version control & source hosting
Newman HTML Reporter
Auto-generated test execution reports
Environment Variables
Secure token & URL management
CI/CD Integration (optional)
GitHub Actions pipeline trigger
What APIs are covered? (typical e-commerce test suite)
POST
/api/auth/register
Create new user account
POST
/api/auth/login
Authenticate & get token
GET
/api/products
List all products
GET
/api/products/:id
Get product details
POST
/api/cart
Add item to cart
PUT
/api/cart/:id
Update cart quantity
POST
/api/orders
Place an order (checkout)
GET
/api/orders/:id
Fetch order status
DELETE
/api/cart/:id
Remove item from cart
How a test works — step by step
1
Send a request
Postman fires an HTTP request to the API endpoint (e.g., POST /api/auth/login) with the required body or headers.

2
Receive a response
The server returns a response — a status code (like 200 OK or 401 Unauthorized) and a JSON body with data.

3
Run assertions (test scripts)
JavaScript test scripts check: Is the status code correct? Does the response body have the expected fields? Is the response time under 2000ms?

4
Chain requests with variables
A token from login is saved as an environment variable ({{authToken}}) and automatically used in subsequent protected requests.

5
Generate a report
Newman (Postman's CLI runner) executes the entire collection and outputs an HTML report showing pass/fail counts, response times, and error details.

IT standards & professional concepts covered
REST API principles
Correctly uses HTTP verbs (GET, POST, PUT, DELETE), status codes (2xx success, 4xx client error, 5xx server error), and JSON payloads — industry-standard REST conventions.

Auth & token management
Tests Bearer token-based authentication (JWT), validating that protected routes reject unauthorized calls with 401 and allow authenticated ones correctly.

Performance benchmarking
Monitors response times against defined SLA thresholds (e.g., < 2s). Flags any endpoint that consistently exceeds acceptable limits — a non-functional testing practice.

Test collection structuring
Organizes tests into folders by domain (Auth, Products, Orders), following ISTQB-aligned test design principles: positive cases, negative cases, boundary validation.

Environment & data separation
Uses Postman environments (dev, staging, prod) to keep base URLs and secrets out of test scripts — aligns with the 12-Factor App configuration standard.

Version control discipline
Collection JSON and environment files committed to GitHub with meaningful commit messages — demonstrates professional Git workflow and enables team collaboration.

How to present this in interviews
Problem statement: "I built an automated test suite to validate the ShopperStack e-commerce platform's APIs end-to-end, ensuring correctness, security, and performance without manual testing."

What you tested: "I covered the full user journey — registration, login, browsing products, cart operations, and order placement — validating both happy paths and negative scenarios like invalid tokens."

Technical implementation: "I used Postman collections with JavaScript test scripts, chained requests using environment variables, and used Newman CLI to generate HTML reports for each test run."

Business impact: "Automated testing reduces regression time from hours to minutes, catches bugs before production deployment, and gives stakeholders confidence in every release."

Suggested improvements to strengthen the project
Add CI/CD pipeline — plug Newman into GitHub Actions so tests auto-run on every push. This shows DevOps awareness, a major differentiator for fresher candidates.

Data-driven testing — use Postman's CSV/JSON data files to run the same test with multiple input sets (e.g., 10 different user credentials), showing scale awareness.

Schema validation — add tv4 or ajv JSON Schema validation in test scripts to assert API response structure, not just values.

Documented bugs found — add a BUGS.md file listing real or simulated defects caught during testing with severity, steps to reproduce, and expected vs actual behavior.

Expand the README — add setup instructions, a folder structure explanation, and screenshots of the Newman HTML report. A well-documented repo signals professional maturity.

github.com/Sunny-Atre/ShopperStack-API-Automation-Project
by Sunny Atre
