# Test Summary Report – E-commerce Application

## 1. Document Information

| Field               | Details                    |
| ------------------- | -------------------------- |
| Project             | E-commerce Web Application |
| Testing Phase       | System Testing             |
| Environment         | Test Environment           |
| Browser             | Google Chrome              |
| Test Cases Executed | 20                         |
| Passed              | 17                         |
| Failed              | 2                          |
| Blocked             | 1                          |
| Defects Identified  | 3                          |
| Status              | Completed                  |

---

## 2. Testing Summary

A total of 20 test cases were executed during the testing cycle.

The test execution focused on the main user flows of the application, including authentication, registration, product search, product management, shopping cart functionality and checkout.

### Test Execution Results

| Result  | Count |
| ------- | ----: |
| Passed  |    17 |
| Failed  |     2 |
| Blocked |     1 |
| Total   |    20 |

### Pass Rate

**85%**

The pass rate was calculated based on the total number of executed test cases.

---

## 3. Defects Summary

Three defects were identified during testing.

| Defect ID | Description                                     | Severity | Priority | Status |
| --------- | ----------------------------------------------- | -------- | -------- | ------ |
| BUG-001   | Login accepts invalid password                  | Critical | High     | Open   |
| BUG-002   | Product total not updated after quantity change | Major    | High     | Open   |
| BUG-003   | Typo in checkout confirmation message           | Minor    | Low      | Open   |

---

## 4. Failed Test Cases

The following test cases failed during execution:

### TC-002 – Login with invalid password

**Result:** Failed

The application allowed authentication using an incorrect password.

**Related Defect:** BUG-001

---

### TC-016 – Update product quantity

**Result:** Failed

The shopping cart did not correctly update the product total after changing the quantity.

**Related Defect:** BUG-002

---

## 5. Blocked Test Case

### TC-017 – Checkout with valid information

**Result:** Blocked

The test could not be completed because the payment/checkout environment was unavailable during the test execution.

No additional defect was raised because the issue was related to the test environment rather than confirmed application behavior.

---

## 6. Test Coverage

The following application areas were covered:

* User authentication
* User registration
* Product search
* Product details
* Shopping cart
* Checkout
* Logout
* Input validation
* Error handling

---

## 7. Quality Assessment

The majority of the planned test cases passed successfully.

However, the presence of a critical authentication defect and a major shopping cart calculation defect represents a significant risk to the application.

BUG-001 should receive immediate attention because it may allow unauthorized access to user accounts.

BUG-002 should also be prioritized because incorrect pricing information may negatively affect the checkout process and user trust.

---

## 8. Recommendations

The following actions are recommended before release:

1. Resolve the critical authentication defect.
2. Resolve the shopping cart calculation defect.
3. Correct the checkout confirmation message.
4. Execute regression testing after fixes are implemented.
5. Re-run all failed test cases.
6. Re-test the blocked checkout scenario once the environment is available.
7. Perform additional exploratory testing around authentication and checkout.

---

## 9. Release Recommendation

**Release Recommendation: NOT RECOMMENDED**

The application should not be considered ready for production release until the critical authentication defect and major shopping cart defect have been resolved and successfully verified through regression testing.

---

## 10. Conclusion

The testing cycle provided useful coverage of the application's main user journeys.

Although most test cases passed, the identified critical and major defects represent unacceptable risks for a production release.

Additional testing should be performed after defect resolution to confirm that the reported issues have been fixed and that no regressions have been introduced.
