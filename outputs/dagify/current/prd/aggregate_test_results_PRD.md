# aggregate_test_results PRD

## Description
Consolidate outputs from all test categories


## Conceptual Info

This node consolidates test results from unit, integration, and end-to-end tests, calculating the overall pass rate and identifying overlapping test failures.

## Docstring

### Summary
Aggregate test results from multiple test categories, including unit, integration, and end-to-end tests.

### Parameters

- **unit_test_results** (List[str]): List of unit test results
- **integration_test_results** (str): Results of the integration tests
- **e2e_test_success_rate** (float): End-to-end test success rate as a percentage

### Returns

dict: A dictionary containing the consolidated test results, including the list of all test results, test failures, overall pass rate, and failure overlaps.

### Raises

- ValueError: If any of the input test results are invalid or missing.

### Examples

```python
>>> unit_test_results = ['pass', 'fail', 'pass']
>>> integration_test_results = 'pass'
>>> e2e_test_success_rate = 90.0
>>> aggregate_test_results(unit_test_results, integration_test_results, e2e_test_success_rate)
{'test_results': ['pass', 'fail', 'pass', 'pass'], 'test_failures': ['fail'], 'pass_rate': 0.75, 'failure_overlaps': []}
```
