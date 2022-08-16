# Stitch_ROMS_GLORYS
Codes used to reformat GLORYS grid into ROMS grid

Before running the following code, Climate Data Operators (cdo) needs to be installed ("sudo port install cdo" in your terminal). 

After doownloading both ROMS and GLORYS data using the codes provided in seperate repos, we can either reformat GLORYS to a grid similar to ROMS data and verse-verca using the following line code:

for i in $(ls); do cdo remapbil,grid.txt ${i} regrid/${i}wgs.nc; done

Where we can specify the grid in file grid.txt
