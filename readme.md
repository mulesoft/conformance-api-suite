# Conformance Testing Repo

## What is this?
Conformance testing repo is a repo containing multiple projects with test case files 
consumed by teams which want to maintain compatibility on their toolsets.

Projects contain at least a main file and a testcase.json file.

## Who uses this?

- Teams:
    - Api Designer Team





## Layout
Projects is the main folder from where projects are stored. Inside projects folder 
we observe 2 more folders , OAS and RAML.

OAS and RAML projects should be located inside their respective folders.

`testcase.json` file is **optional**. If a `testcase.json` file is located inside the project`s
folder then assertions inside will be checked.

Make sure , if no `testcase.json` is placed, to maintain your main api file as : `api.raml`



## The testcase.json file
The `testcase.json` file includes such info such as:

- metadata {}:
    - mainFile
    - language (optional)

- files [] (optional):
    - fileName {}:
        - errorData (optional)
        - warningData (optional)
        - **nErrors**
        - **nWarnings**
        - suggestions (optional)
        - resourceAssertions (optional)

*bold means fully implemented

### Testcase.json file example
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

## Adding a project
If you need a project added to this repo for conformance testing, refer to our [contact list](#contact)
or create a new PR with the following requirements met :

- Branch must respect following naming convention : `PROJECTADD_PROJECTNAME`
- Project must be placed inside correct folder (`./projects/OAS` or `./projects/RAML`)
- `Testcase.json` is optional, but must not contain errors if included


## Contact
Refer to the following for project adding, removal or any problems you may encounter
with this repo.

[flosardo@mulesoft.com](mailTo:flosardo@mulesoft.com)
