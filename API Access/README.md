# Introduction
- The Econometric application is Decision support software for the evaluation of fertiliser strategies that can assist farm consultants and their clients to determine pastoral agriculture fertiliser policies. It is designed to model and compare the effect of alternative fertiliser programmes on soil nutrient levels over a 10 year timeframe.
- The Econometric.Api provides a single endpoint which exposes key functionality (scenario creation) of the Econometric application.
- The Econometric.Api is hosted in PureFarming, for further developer information about PureFarming refer to the [developer documentation](https://developer.purefarming.com/home/)

## Econometric.Api scenario creation

- See section on [Authentication](Authentication.md)

------------------------------------------------------------------------------------------

#### Endpoint to create a new Econometric scenario

<details>
 <summary><code>POST</code> <code>/models/econometric/Scenario/CreateScenario/New</code></summary>

##### Parameters

> | name      |  type     | data type               | description                                                           |
> |-----------|-----------|-------------------------|-----------------------------------------------------------------------|
> | scenarioType      |  required | string   | valid values: "UserDefined", "Zero", "Constant", "Maintenance", "Optimum", "Constrained" |

#### Request body

- For a description of the format of the json to be provided here refer to the example json provided in the schema folder


##### Responses

> | http code     | content-type                      | response                                                            |
> |---------------|-----------------------------------|---------------------------------------------------------------------|
> | `200`         | `application/json`       `        | See below                                |
> | `400`         | `text/html;charset=utf-8`         | Access token not supplied                            |
> | `405`         | `text/html;charset=utf-8`         | None                                                                |

##### Response Body
- For a description of the contents of the Response Body see the following section on [Response Body](Response_Body.md)
- For an example response body refer to this [file](response_1681773827049.json)

</details>

------------------------------------------------------------------------------------------
