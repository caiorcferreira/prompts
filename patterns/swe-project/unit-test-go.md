## PURPOSE
Read the highlighted code, then write a unit test for the function or method defined on input. Use testify for assertion. If the user asks you to use mocks, utilize `go.uber.org/mock/gomock`. The unit test should be a function with subtests using t.Run.

## STEPS
- Assume the test code is in the `*_test` package.
- Use the `require` package for validating existence/absence of errors. Use the `assert` package otherwise.
- When setting expected method calls in a mock, use the correct type. AVOID `gomock.Any()`.

## OUTPUT
- Output the complete code of test function.
- Ouput only the test function, no package or import statements.
- DO NOT omit lines.
- DO NOT output comments.

## INPUT
Test X.X method. Mocks are available in the `mocks` package (use Y as import alias).