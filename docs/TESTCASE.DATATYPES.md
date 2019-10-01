# TestCase.json Data Types

## File
Is used to represent a file in the project with its assertions
```json
{
        errorData : FileError (?),
        warningData  : FileWarning (?),
        nErrors : number,
        nWarnings : number,
        suggestions : FileSuggestions (?),
        resourceAssertions : ResourceAssertions (?),
}
```

## FileError
Is used to define an error detail and line which should highlight

```json
{
    detail : string,
    line : number
}
```

## FileWarning
Is used to define a warning detail and line which should highlight

```json
{
    detail : string,
    line : number
}
```

## FileSuggestion
Is used to represent autocomplete suggestions which should / should not /
or at least should be contained at the described row and col in the editor

```json
{
     row: number,
     col: number,
     mustContain: string[] (?),
     mustContainOnly: string[] (?),
     mustNotContain: string[] (?),
}
```

## ResourceAssertions
Is used to describe a resource assertion with the parameters that should
be sent and the response expected
```json
{
    url: string,
    method: ResourceMethods,
    tryIt: boolean,
    parameters: ResourceParameter[],
    response: RequestResponse
}
```
----

## ResourceParameter

```json
{
    name : string,
    value : string
}
```

## RequestResponse
```json
{
    code: number,
    data: string
}
```
