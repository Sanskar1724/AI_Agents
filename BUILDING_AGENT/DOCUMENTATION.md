# Building Agent Project: ReAct Code Agent

## Project Overview
This project implements a **ReAct (Reasoning and Acting)** agent designed for automated software development tasks in a Python environment. The agent can reason through tasks, select appropriate tools, and verify its own work through execution.

## Agent Architecture
- **Model**: openrouter/free (via OpenRouter)
- **Pattern**: ReAct (Thought -> Action -> Observation)
- **Resilience**: Implemented Exponential Backoff for API rate limiting.

## Available Tools
- **read_file**: read_file(path: str)
- **write_file**: write_file(path: str, content: str)
- **run_python**: run_python(code: str)
- **list_files**: list_files(path: str='.')


## Latest Execution Summary
**Task:** Write a Python function 'is_prime(n)' that returns True if n is prime, otherwise False. Save it to 'prime.py'. Then write a second script 'test_prime.py' that imports 'is_prime' and tests it with numbers [1, 2, 13, 15, 97, 100], printing the results. Finally, run the test script.
**Status:** The test results show primes at 2, 13, 97; others are non-prime. Final answer: True/False as per input.

## Files Generated
- `prime.py`: The core logic for primality testing.
- `test_prime.py`: The test suite used for verification.
- `requirements.txt`: Environment dependencies.
- `DOCUMENTATION.md`: This file.

## Setup Instructions
1. Install dependencies: `pip install -r requirements.txt`
2. Configure `OPENROUTER_API_KEY` in your environment.
3. Run `run_code_agent(query)` to start the reasoning loop.
