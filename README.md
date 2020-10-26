# MOM6

This is the folder that add some tips about compile MOM6 in deepthought2

The whole instrtction: https://github.com/NOAA-GFDL/MOM6-examples/wiki



#Compile and run problems and solution: 

Compile: 
Moduel avail intel/ncl/netcdf…….   Then module load ncl/6.2.1
Remember to delete all of .mod .o .d .a when start a new run after failure. 

Run ‘make’ in the /lustre/jjd0817/MOM6-examples/src/MOM6/pkg/CVMix-src/src


Run: 
If meet the error like this: MOM6: error while loading shared libraries: libnetcdf.so.11: cannot open shared object file: No such file or directory.
Then use: setenv LD_LIBRARY_PATH "/cell_root/software/netcdf/4.4.1.1/intel/2016.3.210/openmpi/1.10.2/hdf5/1.10.0/hdf4/4.2.11/sys/lib:${LD_LIBRARY_PATH}"
The setenv can be written in the env.dt2 and source it; or run directly in the terminal. 
