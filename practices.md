# Practices

## All Languages

### Typeful programming
Related to the principle "parse, don't validate". In general, it should be impossible to construct an object in an invalid state.

### Pure functions
If possible, functions should be pure, so that they can be tested easily. Combined with typeful programming, this can often make it easy to test functions exhaustively.

### Configuration
There should, most of the time, be only one way to configure software. The common pattern of including a config file, environment variables, and defaults in the software itself, is an anti-pattern. My favored setup is to put any config parameters into a config.json that is loaded at start, with no defaults. If we need a value in order to run, we _must_ provide it in the config file, or we error and crash at the start of the program. Because of this, it's often a good idea to provide a `default_config.json`, made to be copied and tweaked. We also provide a flag to change the config filepath.

### Comments
Comments should be concise when possible, proportionate to the complexity of the code. Code that is fairly standard should have short comments which state what it does, and mmore elaborate code should include more description, and an example, though they should still be as concise as they can reasonably be. Comments should NOT describe stylistic aspects that are obvious to readers - for example, functions that are written as Pure because of the previous guidelines should not be labeled as "Pure".

Complex code, syntactically complex constructs like regex, and business logic that is difficult to follow should ALWAYS be preceded by a comment explaining how they work, and/or why they're present.

## Python-Specific

### Docstrings
Provide a docstring for every function, class, and package. These should be google-compliant with full args and returns rections, or should be single line descriptions. Follow the all-language "Comments" doctrine to decide which is appropriate.
