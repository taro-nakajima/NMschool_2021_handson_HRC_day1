# Hands-on experiments at HRC(BL12), NM school 2021

## Introduction
This webpage shows the outline of the on-line hands-on training of HRC spectrometer in MLF of J-PARC and sample programs for the training. 

## Gnuplot
We will use gnuplot plogram in this training course. Please download and install gnuplot from the following url. 

for Windows: https://sourceforge.net/projects/gnuplot/files/gnuplot/5.4.2/

for macOS:
1. Install The Homebrew package manager. https://brew.sh/
2. Open "Terminal" app. and type 
```bash
brew upgrade
brew install gnuplot
```

## Section 1: A brief review of inelastic neutron scattering.
 A lecture on inelastic neutron scattering will be given by Prof. Itoh in the morning session on Tuesday. Here, we recall basic equations on energies and momenta of neutrons and excited quasi-particles (phonons, magnons etc.).

## Section 2: Overview of HRC spectrometer. 
 HRC is the High-Resolution Chopper spectrometer at BL12 in MLF of J-PARC. Key parameters of the spectrometer are following. 


3. Examples of experiments at HRC (CsFeCl<sub>3</sub> under pressure, SrRuO<sub>3</sub> Neutron Brillouin scattering) 
4. Procedures of neutron inelastic scattering experiment.
    1. How to make a plan for an inelastic scattering experiment.
    2. How to determine an appropriate incident energy (TOF diagram)
    3. Multi-Ei method.
    4. _Q-E_ trajectories in a 2D reciprocal lattice space (single crystal). 

### Problem 1: 
Calculate a phase offset for the target _E_<sub>i</sub>. 

[gnuplot script for problem 1](/problem1/plot_TOF_diagram_single.txt).

### Problem 2: 
Calculate other Eis when the target Ei of 160 meV is obtained by rotating the Fermi chopper with a frequency of 200 Hz. gnuplot script 

### Problem 3: 
Calculate Q-E trajectories for Ei=160 meV.  gnuplot script 
 
