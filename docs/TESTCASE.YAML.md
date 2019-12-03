# Testcase.yaml file
Testcase yaml file is the file which contains metadata and assertions 
for the project it is stored in.
`testcase.yaml` file should be stored inside the root folder of the project.

The `testcase.yaml` file includes such info such as:

```yaml
    assertions:
      -
        name: <name for assertion?
        expectThat: <type of eval>
        value: <value Expected, could be an object>
```



-----


## Testcase.yaml file example
```yaml
    assertions:
        -
            name:number of errors
            expectThat : greaterThan
            value: 8
        -
            name: number of errors
            expectThat: lessThan
            value: 9


```
