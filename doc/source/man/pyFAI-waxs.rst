Integration tool: pyFAI-saxs
============================

Purpose
-------

Azimuthal integration for WAXS users.

pyFAI-waxs is the script of pyFAI that allows data reduction (azimuthal integration) for 
Wide Angle Scattering to produce X-Ray Powder Diffraction Pattern with output axis in 2-theta space.

Usage: 
------
pyFAI-waxs -p param.poni [options] file1.edf file2.edf ...

Options:
--------
  --version             show program's version number and exit
  -h, --help            show this help message and exit
  -p PONIFILE           PyFAI parameter file (.poni) MANDATORY
  -n NPT                Number of points in radial dimension
  -w WAVELENGTH, --wavelength=WAVELENGTH
                        wavelength of the X-Ray beam in Angstrom
  -e ENERGY, --energy=ENERGY
                        energy of the X-Ray beam in keV (hc=12.398419292keV.A)
  -u DUMMY, --dummy=DUMMY
                        dummy value for dead pixels
  -U DELTA_DUMMY, --delta_dummy=DELTA_DUMMY
                        delta dummy value
  -m MASK, --mask=MASK  name of the file containing the mask image
  -d DARK, --dark=DARK  name of the file containing the dark current
  -f FLAT, --flat=FLAT  name of the file containing the flat field
  -P POLARIZATION_FACTOR, --polarization=POLARIZATION_FACTOR
                        Polarization factor, from -1 (vertical) to +1
                        (horizontal), default is None for no correction,
                        synchrotrons are around 0.95
  --error-model=ERROR_MODEL
                        Error model to use. Currently on 'poisson' is
                        implemented
  --unit=UNIT           unit for the radial dimension: can be q_nm^-1, q_A^-1,
                        2th_deg, 2th_rad or r_mm
  --ext=EXT             extension of the regrouped filename (.xy)

