## Response Body

- Below is detailed the structure of the Response Body json


> | name      |  type     | value               | description                                                           |
> |-----------|-----------|-------------------------|-----------------------------------------------------------------------|
> | Id      | string  | 0   |  |
> | Name      | string  | "Maintenance"   | The name of the scenario created |
> | ScenarioType      | string  | "Maintenance"   | The scenario created |
> | Block      | array of Block object  |    | See the description of the Block Object |
> | OptimumParams      | object  |    | See the description of the OptimumParams Object |
> | Reports      | array of Report Object  |    | Farm level reports, see the description of the different Report Object(s) below |
> | ConstantAmounts      | array of ConstantAmount object  |    | See the description of the ConstantAmount Object |

### Block Object
> | name      |  type     | value               | description                                                           |
> |-----------|-----------|-------------------------|-----------------------------------------------------------------------|
> | Id      | string  | 0   | Unique identifier of the block |
> | Name      | string  | "Block 1"   | The name of the block |
> | Nutrients      | array for each nutrient of Nutrient Object  |    | See the description of the Nutrient Object |
> | Reports      | array of Report Object  |    | Block level reports, see the description of the different Report Object(s) below |

### Nutrient Object
> | name      |  type     | value               | description                                                           |
> |-----------|-----------|-------------------------|-----------------------------------------------------------------------|
> | Name      | string  | "P"   | Nutrient Name e.g. P, K, S, Rpr, ElementalS, Ca |
> | ListOfYears      | array of 10 Year Object  |    | See the description of the Year Object |

### Year Object
> | name      |  type     | value               | description                                                           |
> |-----------|-----------|-------------------------|-----------------------------------------------------------------------|
> | Value      | string  |    | Nutrient value or Quantity (Indicated in the report)  (Double) |
> | Year      | string  |    | Year value 1..10, represents modelled future years where 1 is the current year |


### Report Object - YearValueReport
> | name      |  type     | value               | description                                                           |
> |-----------|-----------|-------------------------|-----------------------------------------------------------------------|
> | $type      | string  |  "Econometric.Schema.ScenarioModal.YearValueReport, Econometric.Schema"  | Value indicates Report Type |
> | ListOfYears      | array of 10 Year Object  |    | See the description of the Year Object |
> | TypeOfReport | string  | e.g. "GrossReturns, "MilkProduction", "GrossMargin", "RelativeYield", "OlsenP", "Fertiliser", "StockingRate", "StockAdjustments", "Npv", "Irr" | The Econometric report type |

### Report Object - NutrientReport
> | name      |  type     | value               | description                                                           |
> |-----------|-----------|-------------------------|-----------------------------------------------------------------------|
> | $type      | string  |  "Econometric.Schema.ScenarioModal.NutrientReport, Econometric.Schema"  | Value indicates Report Type |
> | Nutrients      | array of for each nutrient Nutrient Object  |    | See the description of the Nutrient Object |
> | TypeOfReport | string  | e.g. "Applied", "Costs", "Soil", "Loss", "Inputs" | The Econometric report type |

### Report Object - WorkSpaceReport
> | name      |  type     | value               | description                                                           |
> |-----------|-----------|-------------------------|-----------------------------------------------------------------------|
> | $type      | string  |  "Econometric.Schema.ScenarioModal.WorkSpaceReport, Econometric.Schema"  | Value indicates Report Type |
> | RelativeYield      | RelativeYieldReport  |    | See the description of the RelativeYieldReport |
> | OlsenP      | RelativeYieldReport  |    | See the description of the RelativeYieldReport |
> | QuickTestK      | RelativeYieldReport  |    | See the description of the RelativeYieldReport |
> | QuickCa      | RelativeYieldReport  |    | See the description of the RelativeYieldReport |
> | TypeOfReport | string  | "WorkSpace" | The Econometric report type |

### Report Object - RelativeYieldReport
> | name      |  type     | value               | description                                                           |
> |-----------|-----------|-------------------------|-----------------------------------------------------------------------|
> | Nutrients      | array of for each nutrient Nutrient Object  |    | See the description of the Nutrient Object |
> | TypeOfReport | string  | One of "RelativeYield", "OlsenP", "QuickTestK", "QuickCa" | The Econometric report type |

### OptimumParams Object
#### The optimum params used if the scenario is an Optimum scenario, see modelrequest section
> | name      |  type     | value               | description                                                           |
> |-----------|-----------|-------------------------|-----------------------------------------------------------------------|
> | Constraint      | string  |  dollar constraint numeric  | Only used for Constrained optimum  |
> | ElementalMin      | string  | numeric value   | Minimum value of Elemental S, optional only if S required |
> | ElementalRatio      | string  | numeric value   | Ratio of Elemental S to Sulphate S, optional only if S required |
> | MaxValues | string  | array of Max Value Object | See the description of the Max Value Object |
> | PScenario      | string  | None, Rpr, SolubleRpr, SolubleP   | Source of fertiliser P |

### Max Value Object
> | name      |  type     | value               | description                                                           |
> |-----------|-----------|-------------------------|-----------------------------------------------------------------------|
> | Value      | string  |  constraint numeric  | Max Value of Nutrient |
> | Nutrient      | string  | P   | Nutrient identifier one of P, K, S, Rpr, Ca |

### ConstantAmount Object
#### The constant params used if the scenario is an Constant scenario, see modelrequest section
> | name      |  type     | value               | description                                                           |
> |-----------|-----------|-------------------------|-----------------------------------------------------------------------|
> | Fertiliser      | string  |  1  | Integer index of Fertiliser from Fertiliser database, may be null for a non constant scenario  |
> | Rate      | string  | numeric value   | Rate of fertiliser |
> | NutrientValues | string  | array of Nutrient Item Object | See the description of the Nutrient Item Object |

### Nutrient Item Object
> | name      |  type     | value               | description                                                           |
> |-----------|-----------|-------------------------|-----------------------------------------------------------------------|
> | Value      | string  |  Nutrent rate numeric  |  |
> | Nutrient      | string  | P   | Nutrient identifier one of P, K, S, Elemental S, Rpr, Ca |