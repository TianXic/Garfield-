OBJDIR = $(GARFIELD_HOME)/Object
SRCDIR = $(GARFIELD_HOME)/Source
INCDIR = $(GARFIELD_HOME)/Include
HEEDDIR = $(GARFIELD_HOME)/Heed
LIBDIR = $(GARFIELD_HOME)/Library

# Compiler flags
CXX = `root-config --cxx`
CFLAGS = `root-config --cflags` \
	-O3 -W -Wall -Wextra -Wno-long-long \
	-fno-common \
	-I$(INCDIR) -I$(HEEDDIR)

# Debug flags
# CFLAGS += -g

LDFLAGS = -L$(LIBDIR) -lGarfield
LDFLAGS += `root-config --glibs` -lGeom -lgfortran -lm

SpaceChargeEffiect: SpaceChargeEffiect.C
	$(CXX) $(CFLAGS) -c SpaceChargeEffiect.C
	$(CXX) $(CFLAGS) -o SpaceChargeEffiect SpaceChargeEffiect.o $(LDFLAGS)
	rm SpaceChargeEffiect.o

