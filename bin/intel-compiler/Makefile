##intel
# F90=mpiifort
F90=mpiifx
#GFORTRAN
#F90=mpif90
LD=$(F90)
# ifdef HPCTOOLKIT
#    $(info HPCToolkit is loaded - building version for profiling)
#    DBGFLAGS=-g -debug inline-debug-info
# else
#    $(info HPCToolkit is not loaded - building release version)
#    DBGFLAGS=
# endif




OFLAGS= 
#intel compilers
# debug run--------------------NOTE: switch to mpiifort for intel instead of mpiifx for full debug runs
# FFLAGS=-i4 -r8 -O0  -g  -debug all -traceback -qopenmp -qopenmp-link=static -check all -fp-model strict -debug inline-debug-info -zero 
# production run
#FFLAGS=-i4 -r8 -ipo -O3 -march=core-avx2 -fp-model precise -zero -qopenmp  -qopenmp-link=static 	# AMD cpus
FFLAGS=-i4 -r8 -ipo  -xHost -O2 -fp-model precise -zero -qopenmp  -qopenmp-link=static      #	Intel cpus


#gfortran
#debug run
#FFLAGS=-ffree-line-length-none -fdefault-real-8 -fopenmp -Wall  -fbounds-check -finit-local-zero  -fdump-parse-tree -fdump-core -fbacktrace -fdefault-double-8 -fbackslash  -O0 -fcray-pointer -Wno-lto-type-mismatch 
#production run
#FFLAGS=-fdefault-real-8 -fdefault-double-8 -fbackslash -fopenmp -ffree-line-length-none -finit-local-zero -fimplicit-none -flto -fcray-pointer -O3 -march=native -Wno-lto-type-mismatch   

#aocl
#FFLAGS= -O3 -Mfreeform -Mallocatable=03 -Mdaz -fdefault-real-8 -fopenmp -mavx2 -march=znver2 
#FFLAGS= -O2 -mp -fdefault-real-8 -flto -fopenmp -mavx2 -march=znver2 

#gnu hybrid static dynamic
#LIBS = -Wl,-Bstatic libparmetis.a libmetis.a libtecio.a -Wl,-Bdynamic -lstdc++ -lpthread -lm -ldl -lc -lmpi 

#intel static linking
LIBS = libparmetis.a libmetis.a libtecio.a  -lstdc++ 


include Makefile_common


 
