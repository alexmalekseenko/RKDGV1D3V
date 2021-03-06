PROG = rkdg1d3vMPI.a

SRCS =	basis_fun_mod.f90 blzmHOV1D_main.f90 boundary_cond_mod.f90 \
	common_variables_mod.f90 DGV_collision_mod.f90 DGV_commvar.f90 \
	DGV_dgvtools_mod.f90 DGV_distributions_mod.f90 DGV_miscsetup.f90 \
	DGV_mpiroutines.f90 DGV_readwrite.f90 DGV_sf02.f90 distrib_mod.f90 \
	gaussian_mod.f90 gaussquad.f90 misc_setup_mod.f90 mpi_routines.f90 \
	nrroutines_mod.f90 nrtype.f90 nrutil.f90 poly_tool_mod.f90 \
	read_write_tools_mod.f90 right_side_mod.f90 sol_integr_mod.f90 \
	source_f_mod.f90 spatial_operator_mod.f90 spectral_tools_mod.f90 \
	time_integrator_mod.f90 algama.f

OBJS =	basis_fun_mod.o blzmHOV1D_main.o boundary_cond_mod.o \
	common_variables_mod.o DGV_collision_mod.o DGV_commvar.o \
	DGV_dgvtools_mod.o DGV_distributions_mod.o DGV_miscsetup.o \
	DGV_mpiroutines.o DGV_readwrite.o DGV_sf02.o distrib_mod.o \
	gaussian_mod.o gaussquad.o misc_setup_mod.o mpi_routines.o \
	nrroutines_mod.o nrtype.o nrutil.o poly_tool_mod.o \
	read_write_tools_mod.o right_side_mod.o sol_integr_mod.o \
	source_f_mod.o spatial_operator_mod.o spectral_tools_mod.o \
	time_integrator_mod.o algama.o

LIBS =  	

CC = cc
CFLAGS = -O
FC = mpiifort
FFLAGS = -O3
F90 = mpiifort
F90FLAGS = -O3 -mkl  
LDFLAGS = -O3 -mkl

%.o: %.mod

all: $(PROG)

$(PROG): $(OBJS)
	$(F90) $(LDFLAGS) -o $@ $(OBJS) $(LIBS)

clean:
	rm -f $(PROG) $(OBJS) *.mod

.SUFFIXES: $(SUFFIXES) .f90

.f90.o:
	$(F90) $(F90FLAGS) -c $<

basis_fun_mod.o: nrtype.o
blzmHOV1D_main.o: DGV_commvar.o DGV_miscsetup.o DGV_mpiroutines.o \
	common_variables_mod.o misc_setup_mod.o mpi_routines.o nrtype.o \
	read_write_tools_mod.o sol_integr_mod.o time_integrator_mod.o
boundary_cond_mod.o: DGV_commvar.o common_variables_mod.o distrib_mod.o \
	nrtype.o spectral_tools_mod.o
common_variables_mod.o: nrtype.o
DGV_collision_mod.o: DGV_commvar.o DGV_dgvtools_mod.o DGV_distributions_mod.o \
	nrtype.o
DGV_commvar.o: nrtype.o
DGV_dgvtools_mod.o: DGV_commvar.o DGV_distributions_mod.o gaussian_mod.o \
	nrtype.o
DGV_distributions_mod.o: nrtype.o
DGV_miscsetup.o: DGV_commvar.o DGV_dgvtools_mod.o DGV_readwrite.o \
	gaussian_mod.o gaussquad.o nrtype.o
DGV_mpiroutines.o: DGV_collision_mod.o DGV_commvar.o DGV_dgvtools_mod.o \
	DGV_distributions_mod.o DGV_miscsetup.o DGV_readwrite.o nrtype.o
DGV_readwrite.o: DGV_commvar.o DGV_dgvtools_mod.o nrtype.o
DGV_sf02.o: nrtype.o
distrib_mod.o: nrtype.o
gaussian_mod.o: nrtype.o nrutil.o
misc_setup_mod.o: DGV_commvar.o DGV_sf02.o basis_fun_mod.o \
	common_variables_mod.o gaussian_mod.o nrtype.o poly_tool_mod.o \
	spectral_tools_mod.o
mpi_routines.o: DGV_collision_mod.o DGV_commvar.o DGV_mpiroutines.o \
	DGV_sf02.o boundary_cond_mod.o common_variables_mod.o nrtype.o \
	read_write_tools_mod.o right_side_mod.o spatial_operator_mod.o \
	spectral_tools_mod.o
nrroutines_mod.o: 
nrutil.o: nrtype.o
poly_tool_mod.o: nrtype.o
read_write_tools_mod.o: DGV_commvar.o common_variables_mod.o nrtype.o
right_side_mod.o: DGV_collision_mod.o common_variables_mod.o nrtype.o \
	spectral_tools_mod.o
sol_integr_mod.o: basis_fun_mod.o common_variables_mod.o gaussian_mod.o \
	nrtype.o poly_tool_mod.o spectral_tools_mod.o
source_f_mod.o: nrtype.o
spatial_operator_mod.o: DGV_commvar.o DGV_sf02.o boundary_cond_mod.o \
	common_variables_mod.o nrtype.o right_side_mod.o spectral_tools_mod.o
spectral_tools_mod.o: basis_fun_mod.o gaussian_mod.o nrtype.o poly_tool_mod.o
time_integrator_mod.o: DGV_commvar.o common_variables_mod.o nrtype.o \
	spatial_operator_mod.o
