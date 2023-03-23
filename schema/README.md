# Econometric Model scenarios request schema

This schema defines the data input structure for the FANZ Econometric model. 
Further information is provided here for required fields that have dependencies on scenarios selected.

FarmEconomics 
* Year
* SRequired
* KRequired
* LimeRequired
* RprAvailable

Blocks
* Reference

BlockEconomics
* Area
* Rain
SoilInputs

* Group or Order
* Slope

P only
* OlsenP

K
* Qtk
* TbkReserveK or KReserveStatusOption
* KLeaching

S
* PESo or QTSO4 or TotalS

Lime
* Ph

RPR
* QtMg
* Ph

StockClass
* StockClass
* EffectiveStockingRate
* BlockGrossMarginPerRsu required for Optimum and Constrained.
* MilkPerHa required if the stock class = 1 (Dairy)
* LiveWgtKgPerHa

Fertiliser
* Lime all required if Lime is selected
* Sulphur
 * Selemrelease

 * Rpr 
	* RprName

* Costs required for each nutrient selected

RprFertilisers
* Name
* CrF
* Rho
* DissolutionRates

OptimumPrams required for the nutrients selected when an Optimum or Constrained scenario is run
* Constraint required if running a Constrained scenario

