# RayTracingGW
Ray tracing model for atmospheric gravity waves


## to compile 
just ' sh compile '

## configuration 

< Header files >

Grid.h -- Background grid number and location
RayT.h -- The maximum number of ray tracers and time integration
Pcon.h -- Standard physical constants (no need to modify)

If you edit any of these, do not forget to compile again. 


< Namelist files >

calc.conf ( see inside for detail )

Change in namelist parameters do not require re-compilation.

< Input file for initial conditions >

init.dat
- First raw is not read as input data 
- Each raw below 2nd contains initial conditions for each wave packet  
- You can add arbitrary number of waves below

< Input file for background variables >

 example :: SPARC/temp.ascii SPARC/wind.ascii

 if you use other external files,
 set cbgmode='file' in calc.conf and modify io.f90

 u,v and T in xyz coordinate are needed as BG variables.
