# Hands-on experiments at HRC(BL12), NM school 2021, Day 1

## Introduction
This webpage shows the outline of the on-line hands-on training of HRC spectrometer in MLF of J-PARC and sample programs for the training. 

### How to get scripts for problems
If you are familiar with git, just clone this repository.
If not, click the green "Code" button above and choose the "Download ZIP" option.

### Gnuplot
We will use gnuplot plogram in this training course. Please download and install gnuplot from the following url. 

* for Windows: https://sourceforge.net/projects/gnuplot/files/gnuplot/5.4.2/
* for macOS:
    1. Install The Homebrew package manager. https://brew.sh/
    2. Open "Terminal" app. and type 
```bash
brew upgrade
brew install gnuplot
```

## Section 1: A brief review of inelastic neutron scattering.
 A lecture on inelastic neutron scattering will be given by Prof. Itoh in the morning session on Tuesday. Here, we recall basic equations on energies and momenta of neutrons and excited quasi-particles (phonons, magnons etc.).

<img width="500" src="https://user-images.githubusercontent.com/50174733/144694194-b51a3b0f-40ba-4fbf-a6f7-4b8b69a635a2.png">


## Section 2: Overview of HRC spectrometer. 
 HRC is the High-Resolution Chopper spectrometer at BL12 in MLF of J-PARC. Key parameters of the spectrometer are following. 
![HRC_layout_v7](https://user-images.githubusercontent.com/50174733/144195316-b9001709-d7bf-494f-983b-67f8ff7748ef.png)
* L<sub>1</sub> (neutron source (moderator) to sample) : 15.0 m
* L<sub>2</sub> (sample to detector) : 4.0 m
* L<sub>3</sub> (Fermi chopper to sample) : 1.03 m
* L<sub>T0</sub> (neutron source (moderator) to T0 chopper) : 9.0 m
* Coverage of the wide-angle detectors : 3.0 - 64.16 deg

## Section 3: Examples of experiments at HRC 
* Hybridization of longitudinal and transverse spin excitations in CsFeCl<sub>3</sub> under pressure
    - https://www.science.org/doi/10.1126/sciadv.aaw5639
* Neutron Brillouin scattering on SrRuO<sub>3</sub>
    - https://www.nature.com/articles/ncomms11788
 
## Section 4: Components of an inelasitc neutron scattering instrument
### Sec. 4-1: Fermi chopper - single E<sub>i</sub> -
Fermichopper determines the energy of the incident neutron beam. In the following, we study how a Fermi chopper works.

### Problem 1: 
Draw a Time-of-flight (TOF) diagram using the [gnuplot script for problem 1](/problem1/plot_TOF_diagram_single.txt), and check how the TOFs depends on the energies of the incident and scattered neutrons.

* Open "plot_TOF_diagram_single.txt".
* Write down appropriate equations for the variables "vi" and "vf", which are the velocities of incident and scattered neutrons. Note that in gnuplot you can use built-in functions such as sqrt(x) and x**2.0.
* Load the script in gnuplot:
```
gnuplot> load 'plot_TOF_diagram_single.txt'
```
then a png file named 'HRC_TOF_diagram_01.png' will be generated (or updated).

<img width="500" src="https://user-images.githubusercontent.com/50174733/144691625-6982c7f0-c7aa-453f-af1c-d95c2c16dd8d.png">

* Draw TOF diagrams for (1) E<sub>i</sub>=20 meV, E=10 meV (TOF_max=40 ms), and (2) E<sub>i</sub>=100 meV, E=10 meV. You can see how the phase offset of the Fermi chopper changes when changing E<sub>i</sub>. Suppose you are going to measure excitations at 10 meV with E<sub>i</sub>s of 20 and 100 meV. Which will have the higher energy resolution? 
 
### Sec. 4-2: Fermi chopper - multi E<sub>i</sub> -
In problem 1, we assume that the Fermi chopper opens only once for a neutron pulse. But actually, the rotation frequency of the Fermi chopper can be higher than the repitition frequency of the neutron pulse generation, which is 25 Hz in MLF. Then, we can utilize multiple E<sub>i</sub> as we study in the following.

### Problem 2: 
Draw a Time-of-flight (TOF) diagram using the [gnuplot script for problem 2](/problem2/plot_TOF_diagram_multiE.txt), and check how the TOFs depends on the energies of the incident and scattered neutrons.
* Open "plot_TOF_diagram_multiE.txt".
* Run this script in gnuplot. A png file named 'HRC_TOF_diagram_02.png' will be generated (or updated).
* By changing the value of "f" in the script, you can see how the 2nd and 3rd incident energy change with the frequency of the Fermi chopper.
* The variable "E" is the energy of the excitation (energy transfered from the incident neutrons). Please check how the neutron velocities, which are the slopes of the TOF lines, change with the inelastic scattering process with fixed E. 

<img width="500" src="https://user-images.githubusercontent.com/50174733/144692177-502d1961-dc0e-42ee-b405-3e58ae29a977.png">


### Sec. 4-3: Detector coverage
Accessible Q-E range is determined by the detector coverage of the instrument. In the following, we calculate _Q-E_ trajectories for a measurement of a powder sample at HRC. 

### Problem 3: 
Calculate Q-E trajectories using the [gnuplot script for problem 3](/problem3/plot_QEtraj_powder.txt), and check how the accessible Q-E range changes with the energy of the incident neutrons.
* Open "plot_QEtraj_powder.txt".
* Write down appropriate equations for the functions "Q1(t)" and "Q2(t)", which are the Q values measured by the lowest and highest scattering angles, respectively.
* You can see how the accessible Q-E range changes with the incident energy.


![HRC_QErange_s](https://user-images.githubusercontent.com/50174733/144360311-dd88f13f-3ee0-4847-8b9b-2a45c5c782d5.png)

