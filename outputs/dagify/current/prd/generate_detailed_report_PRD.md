# generate_detailed_report PRD

## Description
Create structured summary of test outcomes.


## Conceptual Info

This node generates a comprehensive report of test outcomes, including pass rates, failure heatmaps, and dependency graphs.

## Docstring

### Summary
Generates a detailed report of test outcomes based on the aggregated test results.

### Parameters

- **test_results** (List[str]): List of test results
- **test_failures** (List[str]): List of test failures with error messages
- **pass_rate** (float): Overall pass rate of all tests
- **failure_overlaps** (List[str]): List of overlapping test failures

### Returns

dict: A dictionary containing the test summary, pass rates, failure heatmaps, dependency graphs, and overall coverage.

### Raises

- ValueError: If the input test results are invalid or incomplete.

### Examples

```python
>>> test_results = ['pass', 'fail', 'pass']
>>> test_failures = ['error1', 'error2']
>>> pass_rate = 0.8
>>> failure_overlaps = ['overlap1', 'overlap2']
>>> report = generate_detailed_report(test_results, test_failures, pass_rate, failure_overlaps)
{'test_summary': '2/3 tests passed', 'pass_rates': [0.8], 'failure_heatmaps': 'heatmap', 'dependency_graphs': 'graph', 'overall_coverage': 0.8}
```
