# fastsim-vehicles
Repository for [FASTSim](https://www.nrel.gov/transportation/fastsim.html) vehicles.

# Release Process

When a vehicle or set of vehicles in the `to_be_released/` folder is ready for release in the `private` git branch:
1. Move the vehicle to the `public/` folder, add the new file in git, and commit the change.
1. Create a Pull Request (PR) to merge the `private` branch into `main`.
1. Push `main` to github.com/nrel/fastsim-vehicles.  

This works because the `private/` and `to_be_released/` folders were deleted as part of a commit in main.

# Documentation Nomenclature
| Level | Calibration | Validation | 
| --- | --- | --- | 
| 0 | Vehicle is parameterized without any fitting to performance data.  Maybe we should call this parameterization.  | N/A | 
| 1 | Vehicle parameters are adjusted so that model results reasonably match test data for aggregate, cycle-level data (e.g. fuel usage, net SOC change) | Model results reasonably match at least some aggregate, cycle-level test data not used in any calibration process |
| 2 | Vehicle parameters are adjusted so that model results reasonably match test data for time-resolved test data (e.g. instantaneous fuel usage, instantaneous cumulative fuel usage, instantaneous SOC) | Model results reasonably match at least some time-resolved test data not used in any calibration process |