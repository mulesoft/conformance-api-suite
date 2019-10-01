#Testcase.json file
Testcase json file is the file which contains metadata and assertions 
for the project it is stored in.
`testcase.json` file should be stored inside the root folder of the project.

The `testcase.json` file includes such info such as:

- metadata : MetaData
    - mainFile : string
    - language  : string (?)

- files : File []
    - fileName : File
        - errorData  : FileError (?)
        - warningData : FileWarning (?)
        - nErrors : number
        - nWarnings : number
        - suggestions  : FileSuggestions (?)
        - resourceAssertions : ResourceAssertions (?)


.(?) Means optional

-----

## Testcase.JSON Data types
For more info on the datatypes shown above please refer to :

[TESTCASE.JSON DATATYPES](TESTCASE.DATATYPES.md)

## Testcase.json file example
```json
    {
      "metadata":{
        "mainFile" : "flickr.raml",
        "language": "RAML10"
      },
      "files": {
        "flickr.raml": {
          "errorData": [
            {
              "detail": "Error 1 description",
              "line": 5
            },
            {
              "detail": "Error 2 description",
              "line": 18
            }
          ],
          "warningData": [
            {
              "detail": "Warning 1 description",
              "line": 2
            },
            {
              "detail": "Warning 2 description",
              "line": 20
            }
    
          ],
          "suggestions": [
            {
              "col": 0,
              "row": 4,
              "mustContain": ["baseUriParameters","mediaType","protocols","schemas","securedBy"]
            }
          ],
          "resourceAssertions": [
            {
              "url": "/rest",
              "method": "GET",
              "tryIt": true,
              "parameters": [
                {
                  "name": "method",
                  "value": "flickr.test.echo"
                }
              ]
            }
          ]
        }
      }
    }

```
