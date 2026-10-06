# Practices

- Typeful programming: related to the principle "parse, don't validate". In general, it should be impossible to construct an object in an invalid state.
- Pure functions: if possible, functions should be pure, so that they can be tested easily. Combined with typeful programming, this can often make it easy to test functions exhaustively.
