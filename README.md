# A Model of the Rat Phrenic Motor Neuron

**B. Amini**[^1], **A. Bidani**[^2], **J.B. Zwischenberger**[^3], [**J.W. Clark, Jr.**](http://www-ece.rice.edu/ece/faculty/Clark.html)[^4]

<sup>1</sup> Department of Neurobiology and Anatomy, University of Texas Health Science Center at Houston, Houston, TX, USA
<sup>2</sup> Department of Internal Medicine, University of Texas Health Science Center at Houston, Houston, TX, USA
<sup>3</sup> Department of Surgery, University of Texas Medical Branch, Galveston, TX, USA
<sup>4</sup> Department of Electrical and Computer Engineering, Rice University, Houston, TX, USA

---

## Abstract

We have developed a model for the rat phrenic motor neuron (PMN) that robustly replicates many experimentally observed behaviors of PMNs in response to pharmacological, ionic, and electrical perturbations using a single set of parameters. Our model suggests that the after-depolarization (ADP) response seen in action potentials is a result of the slow deactivation of the fast sodium channel in the range of the ADP coupled with the activation of the L-type calcium channel (I<sub>CaL</sub>). This current and its interactions with the small and large conductance calcium-activated potassium currents (I<sub>KCaSK</sub> and I<sub>KCaBK</sub>, respectively) is also important in the generation of spike frequency adaptation in the repetitive firing mode of activity. Other aspects of the model conform very well to experimental observations in both the action potential and repetitive firing mode of activity, including the role of I<sub>KCaSK</sub> in the medium after-hyperpolarization (AHP), and the role of I<sub>KCaBK</sub> in the fast AHP. We have made a number of predictions using the model, including the existence of two putative sodium currents (fast and persistent), as well as, functional roles for the N- and T-type calcium currents.

## Computational Aspects

Simulations were performed on PCs running Linux and Windows XP and solved using a 5<sup>th</sup> order Runge-Kutta-Merson numerical integration algorithm that includes an automatic step-size adjustment based on error estimates. The tolerance for the integration was 0.5×10<sup>-6</sup>.

The equations were coded in the C language and compiled using the GNU C-compiler and Microsoft Visual C++ (for Linux and Windows XP, respectively). The executable (AApmn.exe) looks for a parameter file (pmn_parsed.d) and an initial condition file (pmn_init_cond.d) in the same directory. The parameters in pmn_parsed.d are in the following order: simulation duration (ms), baseline injected current (nA, for adjusting resting membrane potential), stimulation current (nA), stimulation start time (ms), stimulation end time (ms), followed by the maximal conductances for I<sub>Na</sub>, I<sub>CaL</sub>, I<sub>K</sub>, I<sub>A</sub>, I<sub>D</sub>, I<sub>R</sub>, I<sub>BNa</sub>, I<sub>BCa</sub>, I<sub>NaK</sub>, I<sub>CaP</sub>, I<sub>NaCa</sub>, I<sub>KCaSK</sub>, I<sub>KCaBK</sub>, and I<sub>NaP</sub>.

The simulation output is written to a text file (pmn_result.dat). Each row of this file has time as the first column followed by membrane potential, intracellular calcium, I<sub>Na</sub>, I<sub>CaL</sub>, I<sub>K</sub>, I<sub>A</sub>, I<sub>D</sub>, I<sub>R</sub>, I<sub>BNa</sub>, I<sub>BCa</sub>, I<sub>NaK</sub>, I<sub>CaP</sub>, I<sub>NaCa</sub>, I<sub>KCaSK</sub>, I<sub>KCaBK</sub>, I<sub>NaP</sub>, and I<sub>total</sub>. A Matlab (MathWorks, Natick, MA) M-file (ReadResults.m) reads the output file and assigns variable names to the columns.

## Files to Download

The aforementioned files can be downloaded as a tar.gz archive, [pmn.tar.gz](http://www.ece.rice.edu/~jwc/PMN/pmn.tar.gz) (8 KB). A separate archive, [pmnMS.zip](http://www.ece.rice.edu/~jwc/PMN/pmnMS.zip) (46 KB), is presented for the convenience of Microsoft Visual C++ users. Microsoft Windows users without access to Visual C++ can run the executable (AApmn.exe) found in the Release directory (see below). This directory also contains the initial condition and parameter files needed by the program.

The archive contents are shown below.

### pmn.tar.gz

|   |   | Name             |
|---|---|------------------|
|   | 📁 | **pmn**          |
|   |  └─| makefile         |
|   |  └─| pmn_current.c    |
|   |  └─| pmn_deriv.c      |
|   |  └─| pmn_driver.c     |
|   |  └─| pmn_reader.c     |
|   |  └─| pmn_runge_kutta.c|
|   |  └─| pmn_subs.h       |
|   |  └─| pmn_init_cond.d  |
|   |  └─| pmn_parsed.d     |
|   |  └─| ReadResults.m    |

### pmnMS.zip

|   |   | Name              |
|---|---|-------------------|
|   | 📁 | **pmnMS**         |
|   |  └─| **Release**       |
|   |    └─| AApmn.exe       |
|   |    └─| pmn_init_cond.d |
|   |    └─| pmn_parsed.d    |
|   |    └─| ReadResults.m   |
|   |  └─| AApmn.dsp        |
|   |  └─| AApmn.dsw        |
|   |  └─| AApmn.ncb        |
|   |  └─| AApmn.opt        |
|   |  └─| AApmn.plg        |
|   |  └─| pmn_current.c    |
|   |  └─| pmn_deriv.c      |
|   |  └─| pmn_driver.c     |
|   |  └─| pmn_reader.c     |
|   |  └─| pmn_runge_kutta.c|
|   |  └─| pmn_subs.h       |

---

Last modified August 16th, 2003 by Behrang Amini.
Please feel free to contact me at [zyryab@rice.edu](mailto:zyryab@rice.edu?subject=PMN%20Model%20Web%20Page) with any questions regarding these files.

---

2025-05-27 – Standardized to Markdown.

[^1]: http://www.uth.tmc.edu/nba/
[^2]: http://www.uth.tmc.edu/schools/med/imed/pulmo/index.htm
[^3]: http://www.utmb.edu/surgery/
[^4]: http://www.ece.rice.edu/