# Python-Lab---Google-Cybersecurity

## About

These labs demonstrate the application of Python fundamentals to practical security tasks: automating repetitive checks, validating input against approved lists, and building small algorithms that combine conditionals, loops, and functions. Each lab applies a core Python concept to a realistic security analyst scenario, building from single variables up to a complete login-verification algorithm.

## Summary

These labs work through Python fundamentals from the perspective of a security analyst automating everyday tasks. Rather than teaching syntax in isolation, each activity is framed around a security problem: tracking login information, deciding whether a device needs an update, checking IP addresses against an allow list, standardising employee and device IDs, analysing failed login patterns, and matching users to their assigned devices.

The series is progressive. It starts with assigning variables and inspecting data types, moves through conditional logic and loops, then introduces string manipulation and functions, and finishes by combining all of these into a reusable algorithm that verifies both a user's identity and their assigned device. A reference guide summarising the Module 1 concepts is included as a quick lookup.

## Knowledge gained

- **Variables and data types** — assigning and reassigning variables, and using `type()` to identify strings, lists, integers, and Booleans.
- **Conditional logic** — controlling program flow with `if`, `elif`, and `else`, and combining conditions using `and`, `or`, `not`, and the `in` membership operator.
- **Iteration** — repeating actions with `for` and `while` loops, controlling repetition with `range()`, and exiting early with `break`.
- **String handling** — converting types with `str()`, measuring length with `len()`, concatenating with `+`, slicing and indexing with bracket notation, and locating substrings with `.index()`.
- **Functions** — defining functions with `def`, passing parameters, adding parameters incrementally, returning values with `return`, and reusing returned values in later logic.
- **List operations** — adding and removing elements with `.append()` and `.remove()`, finding positions with `.index()`, and linking two synchronised lists by shared index.
- **Algorithm design** — combining conditionals, loops, functions, and list operations into a nested, reusable login-verification routine.
- **Security application** — applying each concept to practical analyst tasks such as allow-list checks, anomaly alerts, and ID standardisation.

## Labs

| # | Lab                                                                             | Focus                                         | Key concepts |
| --- | ---                                                                           | ---                                           | ---                             |
| 01 | [Assign Python variables](01_Assign_Python_variables.md)                        | Tracking login information                   | Variables, `type()`, data types |
| 02 | [Create a conditional statement](02_Create_a_conditional_statement.md)          | OS update checks, access control             | `if`/`elif`/`else`, `in`, `and`/`or` |
| 03 | [Create loops](03_Create_loops.md)                                              | Connection attempts, IP checks, ID generation| `for`, `while`, `range()`, `break` |
| 04 | [Work with strings](04_Work_with_strings.md)                                    | Employee IDs, device IDs, URLs               | `str()`, `len()`, slicing, `.index()` |
| 05 | [Define and call a function](05_Define_and_call_a_function.md)                  | Alerts, list-to-string conversion            | `def`, function calls, concatenation |
| 06 | [Create more functions](06_Create_more_functions.md)                            | Analysing failed logins                      | `sorted()`, `max()`, parameters, `return` |
| 07 | [Develop an algorithm](07_Develop_an_algorithm.md)                              | Matching users to devices                    | `.append()`, `.remove()`, `.index()`, nested conditionals |
| 08 | [Python concepts reference (Module 1)](08_Python_concepts_reference_module_1.md)| Quick reference                              | Comments, functions, conditionals, loops |
| 09 | [Define and call a function (alternate)](09_Define_and_call_a_function_alt.md)  | Printing inside vs outside a loop            | Loop output behaviour |

