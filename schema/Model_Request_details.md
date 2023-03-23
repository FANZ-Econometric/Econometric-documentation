Level | Entity name | Description | Required | Units
--- | --- | --- | --- | ---
FarmEconomics | Reference | Your reference to this file | Can be empty | 
 | Year | Starting or current year | Yes | 
 | SRequired | Includes S in the scenarios | Yes | 
 | Krequired | Includes K in the scenarios | Yes | 
 | LimeRequired | Includes lime in the scenarios | Yes | 
 | RprAvailable | Includes RPR in the scenarios | Yes | 
 | DiscountRate | Discount rate for NPV and optimisation | Yes | 
 | Region | For elemental S release rate | Required when using S | 
Blocks | Reference | Name of the block | Yes | 
BlockEconomics | Area | Area of the block in ha | Yes | ha
 | IsDairy | If there are dairy animals on the block = true.  | Yes | 
 | Rain | Annual rainfall mm | Yes | mm
 | Irrigation | Annual irrigation mm |  | mm
 | Drainage | Profile drainage class. Use default = -1, Free = 0, Intermediate = 1, Poor = 2 | Yes | 
SoilInputs | SoilGroupDesc | Use soil group or order, not both. Soil groups: Sedimentary, Volcanic, Pumice, Podzols, Sands, Peats | Required if order not provided | 
 | SoilOrderDesc | Use soil group or order, not both. Soil orders: Allophanic, Brown, Gley, Granular, Melanic, Organic, Oxidic, Pallic, Podzol, Pumice, Raw, Recent, Semiarid, Ultic | Required if group not provided | 
 | Slope | Topography: 0 = Flat, 2 = Rolling, 3 = Easy Hill, 4 = Steep Hill | Yes | 
SoilTest | OlsenP | Olsen P soil test result | Yes | 
 | PESo | Organic S soil test result. 1 of 3 options, use PESo (Extractable Organic S), QTSO4 or TotalS | Required when using S | 
 | QTSO4 | Quick test sulphate soil test result. 1 of 3 options, use PESo (Extractable Organic S), QTSO4 or TotalS. (This is used as a way to estimate Organic S and therefore must not be influenced by S fertiliser.) | Required when using S | 
 | TotalS | Total S soil test result. 1 of 3 options, use PESo (Extractable Organic S), QTSO4 or TotalS | Required when using S | 
 | Qtk | Quick test K | Required when using K | 
 | Ph | Soil pH | Required when using Lime or RpR | 
 | QtMg | Quick test Mg soil test result. Used by RPR model | Required when using Rpr | 
 | TbkReserveK | TBK test. One of 2 K options, units = me/100g. If entered as 0 then the default is used | Required when using K | 
 | KReserveStatusOption | Use default = -1, High = 0, Medium = 1, Low = 2, Very Low = 3, Extremely Low = 4. If TbkReserveK is entered, this will not be used | Required when using K | 
 | KLeaching | K leaching potential. If this equals 0, the default based on the soil and rainfall is used | Required when using K | 
 | PastureIntake | Pasture consumed by the enterprises kg DM/ha. Used to calculate the dry matter intake (DMI). If not provided is defaulted to 550 |  | 
StockTypes | StockClass | Dairy = 1, Sheep = 2, Beef = 3, Deer = 4 | Yes | 
 | EffectiveStockingRate | Stocking rate in RSU/ha | Yes | 
 | BlockGrossMarginSU | Gross margin per RSU | Yes | 
 | CapitalValueSU | Capital value per RSU |  | $/RSU
 | MilkPerHa | Milk solids kg/ha | Required when entering Dairy | kg/ha
 | LiveWgtKgPerHa | Live weight sold in kg/ha. Used for determining animal product loss | Yes | kg/ha
Fertiliser/Lime | LimePerpH | T (Lime/pH unit) | Required when using Lime | T
 | AcidificationRate | Inorganic Soil Pool H from Overseer block report | Required when using Lime | 
 | LimeQuality | Lime neutralising value | Required when using Lime | 
Sulphur | Selemrelease | Elemental sulphur release rate based on fert product and region | Required when using S | 
History | Elemental | Amount of Elemental S applied in the two previous years. 1 year ago, 2 years ago | Required when using S | kg/ha
 | Sulphate | Amount of Sulphate S applied in the two previous years. 1 year ago, 2 years ago | Required when using S | kg/ha
Rpr | RprName | Name of the fertiliser being applied for this analysis | Required when using Rpr | 
 | RprHistories | RPR applied in the previous 5 years, latest to earliest | Required when using Rpr | 
Costs | K, etc | Fertiliser cost nutrient $/kg | Yes | $/kg
 | Spreading | The total cost of transport and spreading /ha |  | $/ha
UserDefinedParams | NutrientInputs | Additional nutrient inputs, such as supplements imported. kg/ha |  | kg/ha
 | NutrientOutputs | Additional nutrient outputs, such as supplements made. kg/ha |  | kg/ha
 | FertiliserInputs | Additional nutrient outputs from applied fertiliser. kg/ha |  | kg/ha
RprFertilisers | Name | Name of the fertilisers that are being applied on the blocks. This must match the name used at the block level | Required when using Rpr | 
 | CrF | CR / F, where CR is Phosphate concentration at the RPR surface, measured by the Watkinson test, and F is the fractional P content (F) of the RPR | Required when using Rpr | 
 | Rho | The density of RPR rock particles | Required when using Rpr | 
 | DissolutionRates | Dissolution rates of the fertiliser | Required when using Rpr | 
 |  |  |  | 
# Scenarios
Level | Entity name | Description | Required | Units
--- | --- | --- | --- | ---
OptimumParams |  | Inputs required for the Optimum or Constrained Scenarios | Yes | 
 | Constraint | $/year | Yes | $/year
 | ElementalMin | Minimum amount of Elemental S kg/ha | Yes | kg/ha
 | ElementalRatio | Ratio of Elemental S % | Yes | %
 | MaxValues | Maximum values for each nutrient as per the scenario set up. One item for each nutrient. e.g k: 120.0, p: 120.0, s: 120.0, rpr: 120.0 kg/ha/year, ca:10 T/ha/year | Yes | kg/ha
 | PScenario | Soluble P only = SolubleP, Soluble and Rpr-P = SolubleRpr, Rpr-P only = Rpr | Yes | 
ConstantAmountParams |  | Fertiliser settings for each block when using the Constant Scenario. Must be entered in the same order of the blocks. | Yes | 
 | Fertiliser | Identifier of the fertiliser input e.g. 1 | Yes | 
 | Rate | Application rate in kg/ha | Yes | kg/ha
 | NutrientValues | Nutrient content of the fertiliser kg/ha. One item for each nutrient: P, K, S, ElementalS, Rpr, Ca | Yes | 
Scenarios |  | Scenario inputs for User defined values | Yes | 
 | Name | Name of the Scenario | Yes | 
 | ScenarioType | Type of Scenario = UserDefined | Yes | 
Blocks | Name | Name of the block | Yes | 
 | Id | Unique identifier for the block | Yes | 
Nutrients | Name | Name of the nutrient: p, k, s, rpr | Yes | 
ListOfYears | Value | Amount of nutrient kg/ha to 1 d.p. | Yes | kg/ha
 | Year | Year value: 1 - 10 | Yes | 
