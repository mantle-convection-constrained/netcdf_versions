# NetcdfVersions for Terra

Repository for documenting the version history of the structure of netCDF files that are written out by Terra and read in by TerraTools.

NetCDFVersions repo: [https://github.com/mantle-convection-constrained/netcdf_versions](https://github.com/mantle-convection-constrained/netcdf_versions)<br>
TerraTools repo: [https://github.com/mantle-convection-constrained/terratools](https://github.com/mantle-convection-constrained/terratools)

## About
In its current implementation, Terra writes out data files in the NetCDF format serially - i.e 1 file per MPI process. Historically these files were then used directly by individuals for analysis using their own software. TerraTools now provides an interface for users to access the data in these NetCDF files. As the use of Terra changes so too will the data that is written to NetCDF files. We use this repo as an archive of Terra NetCDF file structures which will help in ensuring TerraTools maintains the ability to read historic Terra NetCDF files 

## Version Number and File Types
The version number of a file is stored as a global attribute of type `float` in each file. Files which predate the version history (v0) are identified by their lack of a version number. 

There are currently 3 main Terra NetCDF file types. 

- TCV:   Contain temperature, composition and flow velocity fields
- Seis:  Contains temperature, composition, converted seismic velocity and converted density fields.
- Layer: Contains temperature, flow velocity and another field

The version number is linked to all file types, so changes to one file type will enact a change in version number for all files. 

Please keep track of all changes here and consider contributing to TerraTools to help deal with the changes. 

## Acknowledgement and Support
This project is supported by [NERC Large Grant MC-squared](https://www.cardiff.ac.uk/research/explore/find-a-project/view/2592859-mc2-mantle-circulation-constrained).
