# Testcase.yaml file
Testcase yaml file is the file which contains metadata and assertions 
for the project it is stored in.
`testcase.yaml` file should be stored inside the root folder of the project.

The `testcase.yaml` file includes such info such as:

```yaml
    name: <project's name>
    description: <project's description>
    language: <project's language (raml1.0 | raml0.8 | oas)
    assertions:
      -
        given: <name for assertion?
        expectThat: <type of eval>
        value: <value Expected, could be an object>
```



-----


## Testcase.yaml file example
```yaml
    name: SimpleApiExample
    description: An example project for conformance repo
    language: raml1.0

    assertions:
        -
            given: numberOfErrors
            expectThat : greaterThan
            value: 8
        -
            given: numberOfErrors
            expectThat: lessThan
            value: 9


```
