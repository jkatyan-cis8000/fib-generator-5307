# Fibonacci Generator Architecture

## Overview
A Python program that generates Fibonacci numbers up to a given limit, developed collaboratively by 2 teammates.

## Modules

### 1. `fib.py` (fibonacci_generator teammate)
**Responsibility**: Core Fibonacci generation logic

**Functionality**:
- `generate_fibonacci(limit)`: Returns a list of Fibonacci numbers up to `limit`
- `get_fibonacci_at(n)`: Returns the nth Fibonacci number
- Iterative implementation for efficiency

**Interfaces**:
- Input: integer limit (positive number)
- Output: list of integers

### 2. `cli.py` (cli_interface teammate)
**Responsibility**: Command-line interface and main entry point

**Functionality**:
- Parse command-line arguments for the upper limit
- Validate input (must be a positive integer)
- Call `generate_fibonacci()` and display results
- Handle errors gracefully with informative messages

**Interfaces**:
- Command-line: `python cli.py <limit>`
- Uses `fib.generate_fibonacci()`

### 3. `test_fib.py` (shared ownership via cli_interface)
**Responsibility**: Unit tests for Fibonacci functions

**Functionality**:
- Test `generate_fibonacci()` with various inputs
- Test edge cases (0, 1, 2, large numbers)
- Test `get_fibonacci_at()` for correctness

## File Ownership
- `fib.py`: fibonacci_generator teammate
- `cli.py`: cli_interface teammate
- `test_fib.py`: cli_interface teammate (tests closely tied to CLI validation)

## Shared Resources
- Both modules import from `fib.py`
- Tests import from `fib.py`
