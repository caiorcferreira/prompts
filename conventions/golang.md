# Golang Coding Conventions

## General

- Follow the [Uber Go Style Guide](https://github.com/uber-go/guide/blob/master/style.md).
- Use Go modules (`go.mod`) for dependency management.
- Keep packages small and focused.
- Use `internal/` to restrict visibility when appropriate.

## Testing

- Use [`testify`](https://github.com/stretchr/testify) for assertions and mocks.
- Use `t.Run` to split subtests by logical test case.
- Prefer `require` over `assert` when test execution should stop on failure.

<details>
<summary>Example</summary>

```go
func TestMyFunc(t *testing.T) {
    tests := []struct {
        name  string
        input int
        want  int
    }{
        {"basic", 1, 2},
        {"negative", -1, 0},
    }

    for _, tc := range tests {
        t.Run(tc.name, func(t *testing.T) {
            got := MyFunc(tc.input)
            require.Equal(t, tc.want, got)
        })
    }
}
```

</details>

## Logging

- Use the standard library's `log/slog` for structured logging.
- Always expect a `*slog.Logger` instance to be injected via constructor.
- Use appropriate levels: `Info`, `Error`, `Debug`, `Warn`.

## Library Preferences

- Use `aws-sdk-go-v2` when working with AWS.
  - Do not use `aws-sdk-go` v1 unless absolutely necessary.
- For CLI or terminal apps, prefer `urfave/cli`.
- For REST APIs use `github.com/go-chi/chi/v5`

## Error Handling

- Handle errors explicitly.
- Use `errors.Join`, `errors.Is`, and `errors.As` from Go 1.20+ when applicable.
- Do not silently ignore errors.

## Naming

- Follow Go naming conventions.
- Acronyms should be uppercase (e.g., `HTTPServer`, `ID`, `URLParams`).

## Comments

- Exported functions/types must have doc comments starting with the name of the item.
- Use `//` for single-line comments. Avoid block comments (`/* */`) except for license headers.

## Performance

- Avoid premature optimization.
- Benchmark critical paths using the `testing.B` framework.