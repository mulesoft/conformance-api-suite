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
The `testcase.json` file includes much of the projects metadata such as language
, main file and file assertions.
This include usually api requests, suggestions in code editors and such.
For more info on how a `testcase.json` file works please refer to :

[TestCase.json](docs/TESTCASE.JSON.md)

[TestCase.json Datatypes](docs/TESTCASE.DATATYPES.md)

-----


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
