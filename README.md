# fastsim-vehicles
Repository for [FASTSim](https://www.nrel.gov/transportation/fastsim.html) vehicles.  
Public version of this repo: https://github.com/NREL/fastsim-vehicles

# Release Process

When a vehicle or set of vehicles in the `to_be_released/` folder is ready for release from the `private` git branch:
1. Move the vehicle to the `public/` folder, add the new file in git, and commit the change. 
2. Push the change to github.nrel.gov/MBAP/fastsim-vehicles in the `private` branch.  
3. Create a Pull Request (PR) to merge the `private` branch into `main`.
4. Pull `main` from github.nrel.gov/MBAP/fastsim-vehicles and then push `main` to github.com/nrel/fastsim-vehicles.  

This works because the `private/` and `to_be_released/` folders were deleted as part of a commit in main.  **Note that the `private` branch should never be pushed to any repo outside of NREL and that `main` should never be merged into `private`.**

# Calibration and Validation Nomenclature
| Level | Calibration | Validation | 
| --- | --- | --- | 
| 0 | Vehicle is parameterized without any fitting to performance data.  Maybe we should call this parameterization.  | N/A | 
| 1 | Vehicle parameters are adjusted so that model results reasonably match test data for aggregate, cycle-level data (e.g. fuel usage, net SOC change) | Model results reasonably match at least some aggregate, cycle-level test data not used in any calibration process |
| 2 | Vehicle parameters are adjusted so that model results reasonably match test data for time-resolved test data (e.g. instantaneous fuel usage, instantaneous cumulative fuel usage, instantaneous SOC) | Model results reasonably match at least some time-resolved test data not used in any calibration process |

## TODO: 
- [ ] link to example of properly filled out yaml file with detailed explanation of everything
- [ ] link to template yaml file 
