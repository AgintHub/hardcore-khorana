# execute_unit_tests PRD

## Description
Run isolated unit test cases


## Conceptual Info

This node executes unit tests in isolation and reports the results, including pass/fail metrics and failure stack traces.

## Docstring

### Summary
Execute unit tests and report results

### Parameters

- **test_environment** (dict): Test environment configuration, including test databases, cache, and sandbox environments

### Returns

dict: Dictionary containing test results, failure stack traces, and test metrics

### Raises

- ValueError: If the test environment is not properly configured

### Examples

```python
>>> test_results = execute_unit_tests({'test_databases': ['db1', 'db2'], 'cleared_cache': True, 'established_sandbox_environments': ['env1', 'env2']})
>>> print(test_results['test_results'])  # Output: ['pass', 'fail', 'pass']
>>> print(test_results['failure_stack_traces'])  # Output: ['Error: ...']
>>> print(test_results['test_count'])  # Output: 3
>>> print(test_results['pass_count'])  # Output: 2
>>> print(test_results['fail_count'])  # Output: 1
{'test_results': ['pass', 'fail', 'pass'], 'failure_stack_traces': ['Error: ...'], 'test_count': 3, 'pass_count': 2, 'fail_count': 1}
```
