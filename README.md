# IEA10MW in OpenFAST for FOOS

[![Status: Work in Progress](https://img.shields.io/badge/Status-Work%20In%20Progress-yellow)](https://github.com/yourusername/repo)

[![Tested with: OpenFAST v4.0.4](https://img.shields.io/badge/Tested%20with-OpenFAST%20v4.0.4-success)](https://github.com/openfast/openfast/releases/tag/v4.0.4)

A modified OpenFAST model of the offshore reference wind turbine developed under [IEA Wind Task 37](https://github.com/IEAWindSystems/IEA-10.0-198-RWT) has been created specifically for the **FOOS (VLADBC7)** project. 

These models are compatible with [OpenFAST v4.0.4](https://github.com/openfast/openfast/releases/tag/v4.0.4).

## Subsoil conditions

Model modifications deal with subsoilconditions, to be adapted to a representative location in the Belgian North Sea. The water depth and soil profile are assumed as defined in the [WILLOW-Norther data set](https://zenodo.org/records/11093262) which has made publicly available by OWI-Lab.

The soil lateral reaction is modeled using distributed lateral springs along the embedded length of the monopile. Several model variations are implemented to reflect different soil–structure interaction (SSI) frameworks, each used to derive the corresponding *p–y curves*. The model assumes initial (i.e., small-strain) soil stiffness values, as **SubDyn** in OpenFAST only supports linear elastic soil springs. Soil springs are defined
each 0.5 m. 

### PISA rule based-method

[![Version: Beta](https://img.shields.io/badge/Version-Beta-blue)](https://github.com/yourusername/repo)

- The [PISA model](pisa/) implements the soil reaction curves according to the
PISA rule-based method.
- The assumed lateral and rotational stiffness profile used to represent the soil reaction—accounting for both soil properties and monopile diameter—is provided in [PISA stiffness data (csv)](Foundation%20stiffness/pisa.csv).