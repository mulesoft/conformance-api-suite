# Conformance Api Suite


test


## What is this?
Conformance Api Suite is a repo containing multiple projects with test case files 
consumed by teams which want to maintain compatibility on their toolsets.

Projects contain at least a main file and a testcase.yaml file.


## Who uses this?

- Teams:
    - Api Designer Team



## Layout
`projects` is the main folder from where projects are stored. Inside `projects` folder 
we observe 2 more folders , `oas` and `raml`.

`oas` and `raml` projects should be located inside their respective folders.

`testcase.yaml` file is **optional**. If a `testcase.yaml` file is located inside the project`s
folder then assertions inside will be checked.

Make sure , if no `testcase.yaml` is placed, to maintain your main api file as : *`api.raml`*



## The testcase.yaml file
The `testcase.yaml` file includes much of the projects metadata such as **language**
, **main file** and **file assertions**.
This include usually **api requests**, **suggestions in code editors** and such.
For more info on how a `testcase.yaml` file works please refer to :

[TestCase.yaml](docs/TESTCASE.YAML.md)


-----

## Example project

An example project is available at `projects/raml/exampleProject`

[Example Project](projects/simpleInvalid)

## Adding a project
If you need a **project added** to this repo for conformance testing, refer to our [contact list](#contact)
or create a new PR with the following requirements met :

- Branch must respect following naming convention : `PROJECTADD_PROJECTNAME`
- Project must be placed inside projects folder
- `testcase.yaml` is needed

## Jobs Using Conformance Api Suite
<h3> Api Designer Conformance </h3>


[![Build Status](https://jenkins.build.msap.io/buildStatus/icon?job=APITooling%2FTestCafe%2Fapi-designer-conformance%2Fmaster)](https://jenkins.build.msap.io/job/APITooling/job/TestCafe/job/api-designer-conformance/job/master/)
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[![Allure Report](./img/allure.png)](https://jenkins.build.msap.io/job/APITooling/job/TestCafe/job/api-designer-conformance/job/master/Allure_20report/)


## Contact
Refer to the following for project adding, removal or any problems you may encounter
with this repo.

[flosardo@mulesoft.com](mailTo:flosardo@mulesoft.com)


