---
title: "Mad Scientist 1"
subtitle: "Four conditional model results above event COP 1.15"
author: "Hob Nilre & Bo C. Herlin"
date: "2026-10-09"
abstract: |
  Four declared event models give simulated receiver work above 1.15 times
  their modelled starting energy and gross external event input. Representative
  COPs are 1.18827 for a falling-weight lever, 1.57080 for a third-derivative
  contact law, 17.92044 for a signed-residue port, and 1.67992 for an
  unconstrained fitted port. We executed 201 new integrations with independent
  methods, work quadrature, endpoint accounts and separate confirmation cases.
  Prospective instrument budgets retain an above-threshold margin. These
  results distinguish additional gravitational descent, hypothetical internal
  laws and an approximation that disagrees with its passive reference.
keywords:
  - event coefficient of performance
  - numerical simulation
  - work and energy
  - higher-order dynamics
  - active impedance
---

\begingroup\scriptsize
\noindent PDF created: \pdfbuildtimestamp\par
\noindent Latest on GitHub: \url{https://github.com/hobnilre/physics-mad-scientist-1}\par
\endgroup

# Four predictions to investigate {-}

The target is **event COP greater than 1.15**. Divide net useful receiver work
by modelled prepared energy above a declared reference, plus every specified
gross external input during the event. Report endpoint stores separately.
Preparation efficiency, reset and unknown internal component accounts remain
explicit further questions.

The following order gives priority to direct measurement and a clear model
interpretation, then to the larger electrical predictions. It is an investigation
ranking, not an ordering of hardware success probabilities.

1. **Falling-weight lever:** a loaded descent delivers more work than the
   initial height reference, with the extra descent recorded. [OP-CT-HW-01]
2. **Third-derivative contact:** an assumed internal force sustains resistance
   work through the first stop. [OP-LR34-02]
3. **Signed-residue port:** a specified active terminal law drives a receiver
   and grows the remaining electrical stores. [OP-LR15-01]
4. **Unconstrained fitted port:** a finite-band approximation predicts work
   that its supplied passive reference does not. [OP-LR35-02]

Each treatment develops a stated model into an executed event study. The last
three use hypothetical internal laws whose physical energy accounts remain
open. The fitted law's result applies to that law; its reference is calculated
alongside it. These are concrete signals and model differences to investigate,
with no measured hardware performance implied.

\newpage

# The falling-weight lever

A teeterboard turns downward arrivals into an upward launch. Timing, leg
compression and board flexibility change the outgoing motion. The question
begins with an endpoint comparison, then asks what work the complete contact
trajectory actually delivers to a receiver.

![Illustrative equal-mass launch comparison. Continued descent and deformation connect the incoming and outgoing kinetic terms.](figures/lever-observation.pdf){#fig:lever-observation width=98%}

For two incoming masses and one outgoing mass, each $70\,\mathrm{kg}$,
speeds of $5$ and $8\,\mathrm{m/s}$ give $K_{\rm in}=1750$ J and
$K_{\rm out}=2240$ J: ratio $32/25$. Gravity, compliance and active forces
can contribute during contact. An ideal fixed pivot supplies impulse at zero
work. The trajectory is therefore the interesting missing measurement.

## A calculated loaded descent

Our adaptation has two $1$ kg vertical drivers, contact arms $a=-0.5$ m,
lever inertia $I=0.15\,\mathrm{kg\,m^2}$, torsion stiffness
$50\,\mathrm{N\,m/rad}$ and bearing damping $0.1\,\mathrm{N\,m\,s}$.
The receiver arm is $a_R=0.8$ m. With upward heights $y_i$, angle $\phi$,
compression $\delta_i=[a\sin\phi-y_i]_+$ and contact force $f_i=k\delta_i$,
Newton's equations during the free event are
\begin{equation}
\begin{split}
m\ddot y_i&=-mg+f_i,\\
I\ddot\phi&=-\sum_i f_i a\cos\phi-50\phi-0.1\dot\phi
-b(a_R\cos\phi)^2\dot\phi.
\end{split}
\label{eq:lever-model}
\end{equation}
Here $g=9.81\,\mathrm{m/s^2}$, $v_R=a_R\cos\phi\,\dot\phi$ and the
external viscous receiver takes $P_R=bv_R^2$.

The event starts with simultaneous release from $y_1=y_2=0.30$ m,
$\phi=0$ and zero velocities. It ends $1.5$ s later, immediately before
the previously specified reset. The original ready plane defines gravitational
zero; we retained that reference and event window. There is no external event
actuator, and $D_{\rm event}=2mgH=5.886$ J. Independently evaluated storage is
\begin{equation}
U=\tfrac12m\sum_i\dot y_i^2+mg\sum_i y_i
+\tfrac12I\dot\phi^2+25\phi^2+\tfrac12k\sum_i\delta_i^2.
\label{eq:lever-store}
\end{equation}

![Executed lever event and separately declared confirmation cases. The store includes gravity relative to the original ready plane. Lines on the right connect the computed endpoints.](figures/lever-event.pdf){#fig:lever-event width=98%}

\FloatBarrier

At $k=500$ N/m and $b=32$ N s/m, receiver work is **6.994139 J**,
giving **COP 1.188267**. Bearing heat is $0.034598$ J. Final storage is
$-1.142737$ J: gravitational energy $-2.244651$ J plus $1.101914$ J of
kinetic and elastic storage. The drivers end $0.114406$ m below the ready
plane. Their additional descent supplies the difference from the starting
reference; the independently calculated account closes numerically.

| Contact $k$ (N/m) | Receiver $b$ (N s/m) | Useful work (J) | Event COP |
| --: | --: | --: | --: |
| 500 | 32 | 6.994139 | 1.188267 |
| 450 | 30 | 7.013120 | 1.191492 |
| 450 | 34 | 7.017282 | 1.192199 |
| 550 | 30 | 6.974505 | 1.184931 |
| 550 | 34 | 6.978687 | 1.185642 |

Table: Representative event and four separate confirmation cases, each executed at three solver settings.

**Make the margin visible.** A scale and ruler determine initial energy;
a load cell and encoder give $W_R=\int F_R\,ds_R$. Predicted peaks are
$52.40$ N and $1.637$ m/s, with $0.156$ m receiver excursion. Assume a
calibrated 200 Hz response, 2 kHz sampling and at most $0.1$ ms channel skew.
Including gain, offset, timing, loading and reference allowances gives
$B_{\rm in}=0.02943$ J and $B_{\rm out}=0.06608$ J. The conservative COP
is **1.171**, above 1.15; all four confirmation cases also pass.
The predicted threshold margin is $0.225239$ J. In the retained full history,
reset requires another $2.210180$ J gross input; its COP is $0.995077$.

\newpage

# A third-derivative contact law

A mass, spring and resistance describe a familiar impact approximation.
A higher-order extension adds an internal force proportional to jerk, the
rate of change of acceleration. Dimensional construction permits this term;
its physical realization is the open question. It gives a precise way to ask
what resistance work the assumed law predicts before the moving mass stops.

![Declared force model and receiver boundary, shown schematically. The internal jerk element has an assigned force law; its physical storage and preparation remain open.](figures/cubic-observation.pdf){#fig:cubic-observation width=98%}

Let displacement be $x$, velocity $v$, mass $m$, spring stiffness $k$ and
receiver resistance $d$. Add the constitutive force $F_X=Xx'''$, with
$X=\alpha md/k$ in kg s. Newton's law becomes
\begin{equation}
Xx'''+mx''+dx'+kx=0,\qquad P_R=dv^2,\qquad P_X=Xx'''v.
\label{eq:cubic-model}
\end{equation}
The sign of $P_X$ measures work entering the internal element from the
resolved motion. It is computed from that force law, independently of the
kinetic and spring stores.

At $\alpha=1$, the operator factors as
$(dD+k)((m/k)D^2+1)$, where $D$ means time differentiation. This is also the
boundary between stable and unstable roots in the normalized cubic control
when $d^2=mk$. Root stability and physical realizability are separate questions.

## First contact to first stop

We used $m=0.5$ kg, $k=5000$ N/m, $x(0)=0$, $v(0)=1$ m/s and
$x''(0)=0$. The event ends at the first positive-time zero of $v$.
No external forcing is specified. Prepared kinetic energy is $0.250$ J;
resistance work is the useful output. Permanent nail penetration is outside
this spring-resistance model.

For $\alpha=1$, the independent exact reference is
\begin{equation}
\omega=\sqrt{k/m},\quad x=\frac{v_0}{\omega}\sin\omega t,
\quad t_*=\frac{\pi}{2\omega},\quad
\frac{W_R}{mv_0^2/2}=\frac{\pi d}{2\sqrt{mk}}.
\label{eq:cubic-exact}
\end{equation}
The simulation, rather than substitution alone, supplies the plotted work.
At $d=50$ N s/m, it reaches the first stop in $15.708$ ms, after $10.000$ mm
travel. Receiver work is **0.392699 J**, and **COP is 1.570796**.

![Executed first-stop work and derivative-coefficient comparison. At the reference point the kinetic-plus-spring sum remains 0.250 J while the receiver accumulates work.](figures/cubic-results.pdf){#fig:cubic-results width=98%}

\FloatBarrier

| $\alpha$ | $d$ (N s/m) | Receiver work (J) | Event COP |
| --: | --: | --: | --: |
| 0, ordinary control | 50 | 0.175391 | 0.701564 |
| 0.5 | 50 | 0.307903 | 1.231611 |
| 1 | 50 | 0.392699 | 1.570796 |
| 2 | 50 | 0.510642 | 2.042569 |

Table: Four of the declared comparisons. All cases and independent integrations were retained.

At the reference stop, kinetic energy is zero and spring energy is $0.250$ J.
The known-store remainder $\Delta U+W_R$ is $+0.392699$ J. Independently
integrated internal force-work is $W_X=-0.392699$ J. This locates the modeled
transfer without assigning a hidden store or an external balancing supply.
What material or controlled mechanism could implement $F_X$ is still open.

**A short, measurable pulse.** Peak receiver force is $50$ N and incoming
speed is $1$ m/s. A load cell, displacement encoder or photogates, and a
synchronous DAQ can resolve those scales. The final prospective specification
uses a characterized 5 kHz force response, 40 kHz sampling and at most
$1\,\mu$s skew. Zero pre-contact sensor state was included. An earlier
2 kHz response exceeded its allowance in some cases and was retained as a
failed instrumentation comparison.

With input bound $0.005$ J and output bound $0.00841$ J, conservative COP
is **1.507**. Four new confirmation cases at $\alpha=0.9,1.1$ and
$d=45,55$ N s/m give COP $1.36188$--$1.79145$ and pass the same criteria.
Across both stages, all 14 declared configurations were executed with three
solver settings. Preparation of the acceleration state and the internal
component's energy account remain concrete subjects for the next investigation.

\newpage

# A signed-residue electrical port

A terminal impedance can hide several internal relaxation modes. Positive
residues admit familiar resistor-capacitor constructions. Signed residues
extend the mathematical family: some combinations remain positive real,
while others predict delivery from the internal port. The useful question is
whether that specified law can deliver work to an actual modeled receiver.

![The signed-residue impedance and its declared loaded extension. The negative-real region grows with the residue scale. The boundary diagram identifies the prepared store and outside receiver.](figures/signed-port-observation.pdf){#fig:signed-port-observation width=98%}

The two-state terminal law is
\begin{equation}
\begin{split}
\tau_j\dot z_j&=i-z_j,\qquad v_X=0.35i+R_1z_1+0.55z_2,\\
(\tau_1,\tau_2)&=(0.08,0.18)\ \mathrm{s},\qquad
R_1=-0.738869257399\alpha\ \Omega.
\end{split}
\label{eq:signed-port}
\end{equation}
Thus $Z(s)=0.35+R_1/(1+0.08s)+0.55/(1+0.18s)$ ohm.
The numerical boundary scale is $\alpha=1$; slightly below it the real
part is nonnegative at every frequency. We retained that control and extended
the explicitly signed law into its active region. This is a conditional
terminal model, with its internal component stores and physical implementation
still unspecified.

## Delivering work into a load

Connect this port in series with $L=1$ H, $C=0.02$ F and an external
receiver $R_L$. Kirchhoff's laws give
\begin{equation}
\dot q=i,\qquad L\dot i=-q/C-R_Li-v_X,
\qquad P_R=R_Li^2,\qquad P_X=v_Xi.
\label{eq:electrical-event}
\end{equation}
Initially $q=0.100$ C, $i=0$ and $z_1=z_2=0$. The prepared capacitor
contains $0.250$ J. The event is the declared $0$--$10$ s interval, ending
before any disconnection; no reset or external event supply is specified.
Known electrical storage is $U=q^2/(2C)+Li^2/2$. The internal port's
physical energy account remains open rather than being assigned zero.

We executed six residue scales $\alpha=0.99,1,1.01,1.2,1.5,2$ and three
receivers $R_L=0.01,0.05,0.1\ \Omega$. The representative
$\alpha=2$, $R_L=0.1\ \Omega$ case gives **4.480110 J** useful work and
**event COP 17.920440**.

![Computed work, independent known stores and internal-port delivery; receiver comparisons use the same 10 s event. The dotted line on the right is COP 1.15.](figures/signed-port-results.pdf){#fig:signed-port-results width=98%}

\FloatBarrier

| Residue scale $\alpha$ | Receiver work (J) | Final $L/C$ store (J) | Event COP |
| --: | --: | --: | --: |
| 0.99 | 0.150541 | 0.086090 | 0.602163 |
| 1 | 0.153998 | 0.090979 | 0.615992 |
| 1.5 | 0.643562 | 1.395023 | 2.574247 |
| 2 | 4.480110 | 21.075454 | 17.920440 |

Table: Executed residue comparisons at $R_L=0.1\ \Omega$. Remaining storage is separate from useful output.

The representative trajectory ends with $20.678461$ J in the capacitor and
$0.396993$ J in the inductor. Direct integration gives
$W_X=-25.305564$ J. Consequently $\Delta U+W_R+W_X$ is numerically small,
while the partial-store remainder $\Delta U+W_R$ is $25.305564$ J.
Both values matter: the calculation resolves the specified terminal transfer,
and leaves the internal physical account for investigation.

**Signals for the bench.** The receiver reaches $0.603$ V and $6.032$ A;
capacitor voltage reaches $45.474$ V. A calibrated shunt, differential voltage
channels and synchronized DAQ can integrate the actual receiver voltage-current
product. Assume 200 Hz characterized channels, 2 kHz acquisition and
$0.1$ ms maximum skew. Input bound $0.005$ J and output bound $0.09067$ J
leave conservative COP **17.213**. The threshold margin is $4.192610$ J.
Four separate cases at $\alpha=1.8,2.2$ and $R_L=0.08,0.12\ \Omega$
give COP $7.24467$--$43.73809$ and pass the same checks. All 22 configurations
were executed with three solver settings. The next physical step is to
identify a port realization and measure its own energy transfers alongside
those already specified.

\newpage

# When an impedance fit delivers work

A model can fit terminal measurements while changing the work it predicts.
This investigation starts with a specified passive reference and an
unconstrained four-pole approximation. The approximation develops a negative
real impedance band. Connecting both laws to the same prepared circuit turns
that spectral difference into a measurable work comparison.

![Calculated real impedance of the fitted law and its passive reference. Negative values belong to the fitted law; they are not a property transferred to the reference.](figures/fitted-port-observation.pdf){#fig:fitted-port-observation width=98%}

The reference has three parallel RLC branches in series with $0.18\ \Omega$:
\begin{equation}
Z_{\rm ref}(s)=0.18+\sum_{j=1}^{3}
\frac{a_js}{s^2+2\zeta_j\omega_js+\omega_j^2},
\label{eq:fitted-reference}
\end{equation}
with $a=(0.90,0.60,0.35)\,\Omega/\mathrm{s}$, $\zeta=(0.08,0.15,0.30)$ and
$\omega=(0.7,2,6)\,\mathrm{rad/s}$. Each term has nonnegative real part.
An unconstrained real least-squares fit on 321 logarithmic frequencies from
$0.03$ to $4\,\mathrm{rad/s}$ uses poles
$p=(-0.25,-0.8,-2.5,-8)\,\mathrm{s^{-1}}$ and gives
\begin{equation}
\dot z_j=p_jz_j+i,\qquad
v_X=D_0i+\sum_j c_jz_j,\qquad D_0=2.85295645\ \Omega,
\label{eq:fitted-law}
\end{equation}
where $c=(-0.24049188,-2.08682151,17.41370233,-49.90285714)$
in $\Omega/\mathrm{s}$. Calculations retained full precision.
The fit's relative complex error is $0.823897$ on its fitting band.
Its minimum sampled real impedance is $-0.326217\ \Omega$ near
$4.571\,\mathrm{rad/s}$. This gives a concrete prediction to challenge,
with the supplied passive reference as an independent control.

## One fixture, two terminal laws

We used the series circuit of \eqref{eq:electrical-event}, with $L=1$ H,
variable $C$ and $R_L$, $0.250$ J initially in the capacitor, zero current
and zero internal states. Both laws evolve for the same declared $10$ s event,
without an external event supply. The fitted states have no assigned physical
stores; its terminal power $v_Xi$ is integrated directly. The reference also
has independently evaluated branch stores and resistor losses.

For $C=0.05$ F and $R_L=0.1\ \Omega$, the fitted law gives **0.419981 J**
receiver work and **COP 1.679922**. The matched reference delivers
**0.061818 J**, giving **COP 0.247271**. The difference is a result about
these two model laws. It cannot establish above-one performance for the
passive reference.

![Executed work and capacitance comparisons. The same initial energy and receiver are used for both terminal laws.](figures/fitted-port-results.pdf){#fig:fitted-port-results width=98%}

\FloatBarrier

| Law | $C$ (F) | Receiver work (J) | Event COP |
| :-- | --: | --: | --: |
| Fitted | 0.03 | 0.330435 | 1.321742 |
| Fitted | 0.05 | 0.419981 | 1.679922 |
| Fitted | 0.08 | 0.245376 | 0.981502 |
| Reference | 0.05 | 0.061818 | 0.247271 |

Table: Actual loaded calculations at $R_L=0.1\ \Omega$, including a below-threshold fitted case and the matched reference.

The representative fitted case leaves $0.907188$ J in its known $L/C$
stores and gives $W_X=-1.077168$ J by direct terminal-power integration.
The reference ends with $0.010018$ J total storage and exports $0.178164$ J
through its other resistors. These separate endpoint accounts explain exactly
which transfers each law specifies.

**Measure the disagreement.** Predicted fitted-case peaks are $0.1285$ V
at the receiver, $1.285$ A, and $6.014$ V across the capacitor. The same
200 Hz, 2 kHz and $0.1$ ms prospective acquisition requirements used above
apply. Input bound $0.005$ J and output bound $0.008958$ J give conservative
COP **1.611**, with a $0.132481$ J threshold margin. Four separately declared
fitted cases at $C=0.04,0.06$ F and $R_L=0.08,0.12\ \Omega$ give COP
$1.28211$--$1.83204$ and pass. All 13 circuits were executed for both laws
and three solver settings. Measure a realized port's terminal response and
energy history together: that decides which law describes the apparatus.

\newpage

# A common event and measurement account {-}

Each model was developed from its force or circuit laws. Energy closure was
checked afterward. The denominator and receiver are fixed before comparison:
\begin{equation}
D_{\rm event}=E_{\rm start}+\sum_k\int_{t_0}^{t_1}
[P_{k,\rm external}]_+\,dt,\qquad
\mathrm{COP}_{\rm event}=\frac{W_{\rm useful}}{D_{\rm event}}.
\label{eq:event-account}
\end{equation}
Prepared stores are counted once. Specified external sources contribute gross
inward work; returns are recorded separately. Receiver backflow is subtracted
from useful delivery; the four selected laws have none. The input floor is
$10^{-9}$ J. All representative events have zero specified external input,
with their initial stores and references stated in their treatments.

| Representative event | Input (J) | Useful work (J) | Event COP | Conservative COP |
| :-- | --: | --: | --: | --: |
| Lever | 5.886 | 6.994139 | 1.188267 | 1.171 |
| Third-derivative contact | 0.250 | 0.392699 | 1.570796 | 1.507 |
| Signed-residue port | 0.250 | 4.480110 | 17.920440 | 17.213 |
| Fitted port | 0.250 | 0.419981 | 1.679922 | 1.611 |

Table: Four conditional model predictions. Conservative ratios use simultaneously applicable prospective input and output bounds.

**Independent work and storage.** For a specified account, compute
$r_E=U(t_1)-U(t_0)-\int\sum_kP_k\,dt$, with powers positive inward.
The lever includes gravity and elastic stores. For each hypothetical internal
law, integrate its force-velocity or voltage-current product independently.
The remaining physical component account stays unknown. A reproducible
partial-store remainder is reported as such; it is neither silently assigned
to a source nor called integration error. Event performance also remains
separate from preparation efficiency, reset and repeatability.

**Numerical evidence.** We completed 201 integrations over 67 declared
configurations, including passive and below-threshold controls. DOP853 and
Radau provide independent methods; tighter tolerances and maximum steps check
sensitivity. Accepted-step 8- and 16-point Gaussian quadrature checks integrated
work states. Matrix exponentials independently check all three linear families;
the cubic reference also matches its exact first-stop solution. Endpoints come
from the actual states. Each family passed its declared numerical gates;
refinement supplies error estimates, not certified bounds or physical-law
uncertainty. Earlier sensor-response failures were retained and followed up.

**What the instrument bounds mean.** Lever input uncertainty is 0.5%; the
other initial-energy bounds are 2%. Lever output allowances cover 0.3% force
gain, 0.2% displacement gain, 0.02 N force offset, sampled timing errors,
0.2% bandwidth/loading and 0.01 J resolution/boundary allowance. Other outputs
allocate 0.5% each to the two measured gains, bandwidth/loading and timing/
sampling, plus 0.5 mJ offset/resolution. Gain errors are composed
multiplicatively. Filtering and synchronization controls fit these allocations.
For simultaneous bounds $B_{\rm in},B_{\rm out}$ we require
$(W_{\rm useful}-B_{\rm out})/(D_{\rm event}+B_{\rm in})>1.15$.
The assumed calibrations must be demonstrated on an apparatus. They establish
a concrete measurement target for each conditional prediction.
