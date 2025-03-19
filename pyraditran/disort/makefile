# ==============================================================================
# makefile
# Author: Ken Hirata, ken.hirata@colorado.edu
# Description: 	Makefule made from a bash file originally distributed in the 
# 				DISORT package
# ==============================================================================

# Compiler
FC = gfortran

# Compiler flags
FFLAGS = -O3 -g -fcheck=all -fdump-core -fbounds-check -Wall

# Source files
SRC = DISOTESTAUX.f90 DISORT.f90 BDREF.f90 DISOBRDF.f90 ERRPACK.f90 LINPAK.f90 LAPACK.f90 RDI1MACH.f90

# Output executable
OUT = disort4_unit_tests.exe

# Default target
all: $(OUT)

# Combine source files and compile
$(OUT): disort_main.f90 $(SRC)
	cat $(SRC) > code.f90
	$(FC) $(FFLAGS) disort_main.f90 code.f90 -o $(OUT)
	chmod u+x $(OUT)

# Clean up
clean:
	rm -f $(OUT) *.mod *code.f90
	rm -rf *.exe.*
