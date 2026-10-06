# Practices

## Typeful programming
Related to the principle "parse, don't validate". In general, it should be impossible to construct an object in an invalid state.

## Pure functions
If possible, functions should be pure, so that they can be tested easily. Combined with typeful programming, this can often make it easy to test functions exhaustively.

## Configuration
There should, most of the time, be only one way to configure software. The common pattern of including a config file, environment variables, and defaults in the software itself, is an anti-pattern. My favored setup is to put any config parameters into a config.json that is loaded at start, with no defaults. If we need a value in order to run, we _must_ provide it in the config file, or we error and crash at the start of the program. Because of this, it's often a good idea to provide a `default_config.json`, made to be copied and tweaked. We also provide a flag to change the config filepath.
