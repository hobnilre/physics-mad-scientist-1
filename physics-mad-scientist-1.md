---
title: "Mad Scientist 1"
subtitle: "Seeking four measurable results above event COP 1.2"
author: "Hob Nilre & Bo C. Herlin"
date: "2026-10-09"
abstract: |
  We seek four distinct open problems with clear simulated event COP
  greater than 1.2 and predictions measurable with ordinary instruments.
  We computed preparation, loaded operation and reset for four starting
  mechanisms: a falling-weight lever, switched transformer, contact chain
  and coil release. The lever's complete-history COP reached 0.9951;
  transformer commutation reduced input by 6.90% at matched receiver delivery.
  Graphs and work tables establish the baseline. The tested models'
  complete-history COP values remain below one. Event-based selection now
  requires reassessment; four qualifying results remain to be found.
keywords:
  - coefficient of performance
  - numerical simulation
  - mechanical contact
  - transformer switching
  - coupled coils
---

\begingroup\scriptsize
\noindent PDF created: \pdfbuildtimestamp\par
\noindent Local draft; the GitHub destination below is planned, not published.\par
\noindent Latest on GitHub: \url{https://github.com/hobnilre/physics-mad-scientist-1} (planned destination)\par
\endgroup

# The search for four {-}

The selection target is **event COP greater than 1.2**: useful receiver work
divided by **prepared starting energy plus gross external input during a declared
event**. State the boundary and energy reference; report remaining stores.
Preparation efficiency, reset and unknown component accounts can remain open.

These four starting questions alternate mechanical and electrical investigations.
The final selection is open across domains: replace any candidate that misses
the COP or measurement criterion until four qualify.

1. **The falling-weight lever.** Timed descent and compliance concentrate
   motion into a loaded takeoff arm. [OP-CT-HW-01]
2. **The switched transformer.** Physical commutation changes the receiver's
   return path and the source-work history. [OP-TRF-02]
3. **The contact chain.** Mass order and gaps reshape the passage of motion
   into a terminal load. [OP-LR54-03]
4. **The coupled-coil release.** Release phase, clamp voltage and winding
   orientation determine where a prepared electrical state goes. [OP-LR48-03]

We integrated 69 initial cases and 17 exploratory coil extensions, refined the
leading cases and compared independent numerical methods. Exact examples explain
the motivating observations; computed graphs and work tables report the finite
models. Their reported COPs retain complete-history accounting; event-COP
reassessment is pending. Useful receivers sit outside each machine boundary.

A qualifying result must survive numerical checks and be measurable with
ordinary instruments at uncertainty small enough to resolve the margin above
1.2. Investigate surprising findings directly through their work integrals and
changing stores. Let the evidence choose the four.

\newpage

# The falling-weight lever

A teeterboard turns downward arrivals into an upward launch. Timing, leg
compression and board flexibility affect the outgoing motion. The motivating
question is whether that concentration can become useful work exceeding the
input needed to prepare and repeat it.

![Illustrative equal-mass endpoint comparison. Continued descent and deformation are part of the contact history.](figures/lever-observation.pdf){#fig:lever-observation width=98%}

**The observation.** For two incoming masses and one outgoing mass, each
$70\,\mathrm{kg}$, speeds of $5$ and $8\,\mathrm{m/s}$ give
\begin{equation}
K_{\mathrm{in}}=1750\,\mathrm{J},\qquad
K_{\mathrm{out}}=2240\,\mathrm{J},\qquad
K_{\mathrm{out}}/K_{\mathrm{in}}=32/25.
\label{eq:lever-observation}
\end{equation}
The selected kinetic terms differ by $490\,\mathrm{J}$. During contact,
gravity continues doing work, springs compress, and active forces may act.
The missing information is the trajectory connecting those endpoints.
An ideal fixed pivot supplies impulse at zero work; it leaves the descent,
rotation and contact forces to determine the delivery.

## Calculated descent, delivery and return

We replaced the performers with two $1\,\mathrm{kg}$ vertical drivers at arm
$a=-0.5\,\mathrm{m}$. The balanced rigid lever has inertia $I=0.15\,\mathrm{kg\,m^2}$,
a $50\,\mathrm{N\,m/rad}$ torsion spring and bearing damping
$0.1\,\mathrm{N\,m\,s}$. Its opposite arm, $a_R=0.8\,\mathrm{m}$, drives
an outside viscous receiver: $v_R=a_R\cos\phi\,\dot\phi$ and
$P_R=bv_R^2$. This loaded adaptation has its own scope alongside the human launch.

With upward driver heights $y_i$, contact compression is
$\delta_i=a\sin\phi-y_i$ and $f_i=k[\delta_i]_+$,
where $[z]_+=\max(z,0)$.
The equations integrated were
\begin{equation}
\begin{split}
m\ddot y_i&=-mg+f_i+u_i,\\
I\ddot\phi&=\tau_a-\sum_i f_i a\cos\phi
-50\phi-0.1\dot\phi-b(a_R\cos\phi)^2\dot\phi.
\end{split}
\label{eq:lever-model}
\end{equation}
Actuator powers were $u_i\dot y_i$
and $\tau_a\dot\phi$. We used $g=9.81\,\mathrm{m/s^2}$.

The drivers rose $0.30\,\mathrm{m}$ during the first second, then released
with a delay of $0$, $0.10$ or $0.20\,\mathrm{s}$. Stiffnesses were $500$
and $1500\,\mathrm{N/m}$; receiver damping was $2$, $8$ or
$32\,\mathrm{N\,s/m}$. At $2.5\,\mathrm{s}$, finite actuator trajectories
returned the machine to its initial positions and velocities by $3.5\,\mathrm{s}$.
Preparation and return followed quintic position curves with continuous velocity;
all their positive and negative work was integrated separately.

![Computed lever results. Left: the best full-history case, including its driven reset. Right: the nine $k=1500\,\mathrm{N/m}$ cases; $b$ is in $\mathrm{N\,s/m}$. The dotted horizontal line is COP $=1$.](figures/lever-results.pdf){#fig:lever-results width=98%}

\FloatBarrier

**What the calculation delivered.** Simultaneous arrival with $k=1500$ and
$b=32$ gave the highest COP among the 18 cases. Its lifting input was exactly
$2mgH=5.886\,\mathrm{J}$. Before reset, the receiver had collected
$6.866664\,\mathrm{J}$: a resolved operating-window ratio of **1.1666**.
At that instant the machine store was $-1.014425\,\mathrm{J}$ relative to
its initial reference, including the drivers' lower gravitational positions.

| Interval | Gross input (J) | Useful output (J) |
| :-- | --: | --: |
| Lift, $0$--$1$ s | 5.886000 | 0.000000 |
| Descent/delivery, $1$--$2.5$ s | 0.000000 | 6.866664 |
| Driven return, $2.5$--$3.5$ s | 2.080219 | 1.060545 |
| Complete history | **7.966219** | **7.927209** |

Table: Computed work for the best lever case. Output during return is counted and identified explicitly.

The full-history COP was **0.995103**. Other exported heat was
$0.038999\,\mathrm{J}$ and actuator return $0.000011\,\mathrm{J}$.
With the same stiffness and simultaneous release, reducing $b$ to $2$ produced
an upward arm speed of about $5.46\,\mathrm{m/s}$ but COP $0.8971$.
A $0.10\,\mathrm{s}$ delay at $b=32$ reduced COP to $0.5990$.
Contact timing gives strong motion and almost complete useful delivery in the
best full-history case. Event-COP reassessment must specify the initial stores
and event inputs; the calculated restoration cost remains a separate result.

\newpage

# The switched transformer

A tapped transformer offers different physical terminal pairs to a receiver.
The motivating mechanical analogy is a gear train with several moving members:
a receiver responds to the difference across its chosen connection. Electrical
taps make the analogous voltage difference directly accessible.

![Ideal opposed-tap observation. The two terminal-pair voltages belong to one trajectory; a loaded return change creates a different circuit.](figures/transformer-observation.pdf){#fig:transformer-observation width=98%}

**The observation.** Winding 1 joins $a,c$ and winding 2 joins $b,a$.
For an opposed ideal turns ratio $-4$,
\begin{equation}
V_b-V_c=(V_b-V_a)+(V_a-V_c),\qquad
V_b-V_a=-4(V_a-V_c).
\label{eq:tap-identity}
\end{equation}
At $V_a-V_c=1\,\mathrm{V}$, the two readouts are $-4$ and $-3\,\mathrm{V}$.
This invites a cycle that uses different connections at different times.
A potential-zero shift leaves both differences unchanged; a physical return
selector changes the currents and stored fields.

Fixed-tap descriptions leave that transition unspecified. Winding currents,
stray charge, finite conductance and driver supplies participate in it.
Earlier bounded switching comparisons do not give a universal supply ordering.
We calculated an explicit finite selector to determine its ordering at a
matched receiver service.

## Calculated finite commutation

We grounded $c$ and used nodes $(a,b,r)$, each with $2\,\mathrm{mF}$ to ground.
Currents run $a\to c$ and $b\to a$. The reciprocal winding matrix and series
resistances were
\begin{equation}
\mathbf L=\begin{pmatrix}0.05&-0.19\\-0.19&0.8\end{pmatrix}\!\mathrm{H},
\qquad \mathbf R=\operatorname{diag}(0.05,0.2)\,\Omega,
\qquad \mathbf L\dot{\mathbf i}+\mathbf R\mathbf i=\mathbf A^T\mathbf v.
\label{eq:transformer-model}
\end{equation}
The incidence matrix $\mathbf A$ has $+1$ at current entry and $-1$ at exit.
Kirchhoff's node equations determine the three capacitor voltages.
The source was $V_s=A_s\sin(4\pi t)$ through $0.2\,\Omega$ for $0<t<1$ s,
then zero through the same resistor. The useful receiver resistor joins $b,r$.

The selector joins $r$ to $a$ or ground through
$G=0.001+49.999x$ siemens, where $\dot x=(\sigma-x)/(2\,\mathrm{ms})$.
Each gate is a $1\,\mu\mathrm{F}$ capacitor driven through $2\,\mathrm{k}\Omega$
from $5\sigma$ volts; its supply power was included. During operation,
$\sigma_a=1$ when $\sin(4\pi t+\psi)\geq0$ and
$\sigma_c=1-\sigma_a$. Both commands went to zero at $1$ s.
A third gate added $x$ siemens to each node's permanent $0.001$ S bleeder
from $1$ to $10$ s. Integration continued to $12$ s.

![Computed transformer results. Left: switched $R=4\,\Omega$, $\psi=\pi$; the early history is shown, while totals include the full 12 s. Right: all twelve commutated cases at unit source amplitude.](figures/transformer-results.pdf){#fig:transformer-results width=98%}

\FloatBarrier

We computed fixed returns $a,c$ and four phases
$\psi\in\{0,\pi/2,\pi,3\pi/2\}$ at receiver resistances $1$, $4$ and
$16\,\Omega$: 18 cases. Among switched cases at $4\,\Omega$, phase $\pi$
gave the highest COP. For the comparison below, we adjusted each fixed case's
source amplitude and reran it to match the switched receiver's full-history
$0.388864\,\mathrm{J}$. Load and total interval remained the same; instantaneous
receiver-power traces were allowed to differ. The fitted source amplitudes were
$0.971127$ V for fixed $a$ and $1.106268$ V for fixed $c$, against $1$ V
for commutation.

| Return path | Gross input (J) | Useful output (J) | COP |
| :-- | --: | --: | --: |
| Fixed $a$ | 0.972101 | 0.388864 | 0.400025 |
| Fixed $c$ | 0.946703 | 0.388864 | 0.410756 |
| Commutated, $\psi=\pi$ | **0.905044** | **0.388864** | **0.429663** |

Table: Calculated matched-service comparison, including gate power and finite reset.

Commutation reduced gross input by **6.90%** against fixed $a$, and **4.40%**
against fixed $c$. Its source return was $0.004690\,\mathrm{J}$ and other heat
$0.511491\,\mathrm{J}$; final magnetic, capacitive and gate storage was below
$10^{-20}\,\mathrm{J}$. Across all 18 unit-amplitude cases, fixed $a$ at
$16\,\Omega$ reached the largest COP, $0.433787$.

This calculation supplies an affirmative result for the switching idea:
physical commutation can improve useful delivery per unit of gross input.
The gain belongs to a specified circuit and service comparison. Its complete
work account remains a baseline; event-COP selection requires a declared
initial-energy reference and integration interval.

\newpage

# The contact chain

A disturbance passing through unequal masses can reverse one body and accelerate
another. Contact release and re-engagement add a timing variable that a permanent
spring does not possess. The COP question concerns how much of that rearranged
motion reaches a useful receiver over a repeatable cycle.

![Exact elastic-contact example. Opposite momenta increase the magnitude sum while preserving the signed total.](figures/chain-observation.pdf){#fig:chain-observation width=98%}

**The observation.** A mass $m$ arrives at speed $u>0$ and strikes a stationary
mass $3m$ through a lossless spring contact of stiffness $k$.
During compression and recovery,
\begin{equation}
v_1=\frac{u}{4}(1+3\cos\theta),\qquad
v_2=\frac{u}{4}(1-\cos\theta),\qquad
\theta=t\sqrt{\frac{4k}{3m}}.
\label{eq:chain-reference}
\end{equation}
At separation, $\theta=\pi$, the momenta are $-mu/2$ and $3mu/2$.
Their magnitude sum has doubled; the signed sum is still $mu$.
Endpoint kinetic energy is $mu^2/2$ in both states. We reproduced this exact
trajectory numerically before adding more masses and a receiver.

The general identity
$\sum_j|p_j|=\sum_jp_j+2\sum_{p_j<0}|p_j|$ exposes the role of counterflow.
For a free chain the signed sum stays constant, while active contacts change.
Finite gaps, branching, restitution and fixture motion are the physical
extensions behind the open question. Here the calculated extension is a loaded
three-body line with gaps and a complete return trajectory.

## Calculated contact and reset histories

The position deviations $\mathbf x$ start at zero. Each column of $\mathbf B$
has $-1$ at the left body and $+1$ at the right body of a contact.
With gap offsets $\mathbf d$, the integrated equations were
\begin{equation}
\dot{\mathbf x}=\mathbf v,\qquad
\mathbf M\dot{\mathbf v}=\mathbf B\mathbf f+\mathbf u-\mathbf e_3bv_3,
\qquad f_e=k[-\mathbf B^T\mathbf x-\mathbf d]_{e,+}.
\label{eq:chain-model}
\end{equation}
The outside receiver absorbs $P_R=bv_3^2$; there is no internal damping in this
model. Contact stiffness was $400\,\mathrm{N/m}$. We computed mass sets
$(1,3,1/2)$, $(1/2,3,1)$ and $(1,1,1)$ kg, gap pairs $(0,0)$ and
$(0.05,0.10)$ m, and $b=0.5,2,8\,\mathrm{N\,s/m}$: 18 cases.

The first body received $8\sin^2(\pi t/0.2)$ newtons for $0<t<0.2$ s.
It then moved without launch drive until $2.5$ s. Finite quintic actuator
trajectories returned all bodies to their starting positions and zero velocity
by $3.5$ s. We integrated each actuator's work, including its returned work.
Kinetic and unilateral spring stores were evaluated independently.

![Computed chain results. Left: the best complete-history case, with equal masses and finite gaps. Right: unequal-mass and equal-mass controls under the same launcher and reset schedule.](figures/chain-results.pdf){#fig:chain-results width=98%}

\FloatBarrier

**What changed under load.** The table compares three cases at $b=8$.
Here $W_{\mathrm{pre}}$ is all receiver delivery before reset, including any
delivery during the launcher pulse. $D_{\mathrm{reset}}$ is gross reset input.

| Masses / gaps | $W_{\mathrm{pre}}$ (J) | $D_{\mathrm{reset}}$ (J) | Full COP |
| :-- | --: | --: | --: |
| $1:3:1/2$, zero | 0.162612 | 0.971015 | 0.309916 |
| $1:3:1/2$, finite | 0.239603 | 1.997999 | 0.212969 |
| $1:1:1$, finite | **0.315183** | **0.145422** | **0.982149** |

Table: Numerical comparison of loaded contact chains. A larger pre-reset output need not give a larger full-history COP.

For the unequal chain, the finite gaps raised pre-reset delivery by about
**47.3%**. The same force pulse supplied $0.196089$ J without gaps and
$0.319239$ J with gaps, and the latter state cost more to restore. In the equal-mass
control, launch input was $0.319246\,\mathrm{J}$ and total input
$0.464668\,\mathrm{J}$. Useful delivery was $0.456373\,\mathrm{J}$, including
$0.141190\,\mathrm{J}$ during reset; actuator return was $0.008295\,\mathrm{J}$.
All mechanical endpoint stores returned to numerical zero.

The useful result is the separation of three effects: momentum redistribution,
loaded delivery and restoration work. The exact counterflow example remains a
strong clue about transport, while the best computed cycle favored mass matching.
Gaps improved one output window by nearly half. The complete trajectories show
which part of that improvement contributes to the COP ambition and which part
requires a better return path. Branches and dissipative contact laws remain
outside this calculated line model.

\newpage

# The coupled-coil release

Two inductors exchanging through capacitance form an electrical counterpart
to the contact chain. Their flux linkages can acquire opposite signs while the
signed sum stays fixed. The idea is to change the circuit at a favorable phase
and route the prepared state into a useful receiver.

![Exact connected-model reference. Opposing linkage signs separate the growing magnitude sum from the fixed signed sum.](figures/coil-observation.pdf){#fig:coil-observation width=98%}

**The observation.** With zero mutual coupling, $L_1=1\,\mathrm{H}$,
$L_2=19\,\mathrm{H}$, initial currents $(10,0)$ A and zero capacitor voltage,
\begin{equation}
i_1=\frac{1+19\cos\theta}{2}\,\mathrm{A},\qquad
i_2=\frac{1-\cos\theta}{2}\,\mathrm{A},\qquad
\theta=t\sqrt{\frac{1/L_1+1/L_2}{C}}.
\label{eq:coil-reference}
\end{equation}
At $\theta=\pi$, flux linkages change from $(10,0)$ to $(-9,19)$ Wb.
Their magnitude sum rises from $10$ to $28$ Wb. The capacitor returns to zero
voltage and magnetic storage is $50$ J at both endpoints. Independent numerical
integrations reproduced the closed form.

Release opens a different question. Winding current must continue through
specified capacitance, clamp and receiver paths. The connected solution identifies
phases worth examining; the finite release circuit determines their useful yield.

## Calculated release, clamp and receiver work

Our finite model used $L_1=0.1$ H, $L_2=1.9$ H, winding resistances
$(0.02,0.04)\,\Omega$, and node capacitances $(0.0001,0.01)$ F.
Winding 1 runs from $a$ to ground; winding 2 runs from ground to $b$.
The currents obey
\begin{equation}
\begin{pmatrix}L_1&M\\M&L_2\end{pmatrix}\dot{\mathbf i}
=\begin{pmatrix}V_a-0.02i_1\\-V_b-0.04i_2\end{pmatrix},\qquad
U_M=\tfrac12L_1i_1^2+Mi_1i_2+\tfrac12L_2i_2^2.
\label{eq:coil-model}
\end{equation}
Kirchhoff's equations evolve both node voltages. A finite switch connects $a,b$;
a separate switch connects $b$ through receiver $R$ to ground.
The clamp at $a$ carries
$I_c=\operatorname{sgn}(V_a)[|V_a|-V_c]_+/(1\,\Omega)$.

Each gate obeys $\dot x=(\sigma-x)/(1\,\mathrm{ms})$, implemented by
$1\,\mu\mathrm{F}$ and $1\,\mathrm{k}\Omega$ at $5\sigma$ volts.
Exchange and receiver-switch conductances are $10^{-6}+100x$ siemens.
The preparation branch connects $10\sin^2(\pi t/0.4)$ volts to $a$ through
$10^{-6}+5x$ siemens for $0<t<0.4$ s. Preparation then switches off and
exchange switches on. At release, exchange switches off and the receiver on.

![Computed coil results. Left: $M=0$, 80 V clamp, $R=1\,\Omega$, release phase $\eta=1/2$; the early history is shown. Right: release/load comparisons. Every COP includes the full 14 s, gate supplies and reset.](figures/coil-results.pdf){#fig:coil-results width=98%}

\FloatBarrier

Release occurred at $t_s=0.4+\eta T_h$, where
$T_h=\pi\sqrt{0.01/(1/L_1+1/L_2)}\simeq0.0968304$ s.
We computed five phases $\eta=1/4,1/2,3/4,1,5/4$ and three loads
$R=1,10,50\,\Omega$. A $10^{-6}+0.1x$ S bleeder at each node was commanded
on from $1.4$ to $12$ s. The receiver command also ended at $12$ s;
integration continued to $14$ s.

The first 15 cases used a 20 V clamp, which conducted during exchange.
A declared second 15-case exploration raised it to 80 V. Two further cases
reversed signed coupling at the best zero-coupling phase and load.

| Clamp / $\eta$ / coupling $\kappa$ | Input (J) | Output (J) | COP |
| :-- | --: | --: | --: |
| 20 V / $1/4$ / $0$ | 16.8117 | 3.8995 | 0.2319 |
| 80 V / $1/2$ / $0$ | **16.8117** | **8.0954** | **0.4815** |
| 80 V / $1/2$ / $-1/2$ | 19.6876 | 8.5788 | 0.4357 |
| 80 V / $1/2$ / $+1/2$ | 19.6876 | 6.5646 | 0.3334 |

Table: Computed coil histories at $R=1\,\Omega$; $\kappa=M/\sqrt{L_1L_2}$. All numbers are numerical approximations.

Changing clamp and release phase more than doubled the zero-coupling receiver
work at essentially the same input. Waiting until $\eta=1$ raised the linkage
magnitude ratio to about $2.77$, but gave COP $0.0995$ at $R=1$ and 80 V.
The best energy delivery occurred earlier. Its other exported heat was
$8.716310$ J and its finite-reset storage remainder $5.0001\,\mu\mathrm{J}$.
These results make the release path the productive design variable: the largest
linkage-magnitude excursion and the best COP occur at different times.

\newpage

# What the calculations establish {-}

The target is four modelled events above COP 1.2, measurable on an ordinary
bench. The complete-history results below remain baseline comparisons;
selection under the event criterion requires reassessment.

| Best tested model | Input $D$ (J) | Useful $W_R$ (J) | COP |
| :-- | --: | --: | --: |
| Lever | 7.966219 | 7.927209 | 0.995103 |
| Transformer, fixed $a$ | 0.593317 | 0.257373 | 0.433787 |
| Chain, equal masses | 0.464668 | 0.456373 | 0.982149 |
| Coil release | 16.811682 | 8.095368 | 0.481532 |

Table: Best full-history COP in each explored family. These are selected model results, not universal optima.

**The baseline account.** At every supply or actuator port, inward power
$P_k$ was integrated separately into gross draw
$D_k=\int[P_k]_+dt$ and returned work $X_k=\int[-P_k]_+dt$.
We used $D=\sum D_k$, $X=\sum X_k$, outside receiver delivery $W_R$
and other exported heat $H$. Stored energy was evaluated from states, giving
\begin{equation}
r_E=\Delta U-D+X+W_R+H,\qquad
\mathrm{COP}=\frac{W_R}{D}
=1-\frac{X+H+\Delta U-r_E}{D}.
\label{eq:complete-account}
\end{equation}
These COPs include preparation and reset. Receivers had no backflow; shared
supplies were counted once. Reset work and remaining stores were calculated,
with exported heat crossing an ideal bath boundary.

**What was checked.** We integrated Newton/Kirchhoff equations rather than
imposing energy closure. Refined leading cases used relative tolerance
$2\times10^{-10}$ and a maximum step of $3$ ms. Independent explicit and implicit
methods changed their COP by less than $3\times10^{-10}$. Their maximum sampled
energy residuals were below $7\times10^{-10}$ J.
The coarser exploratory grid retained residuals up to $1.3\times10^{-4}$ J.

Uniform power sampling initially missed a fast coil-switch transient by
$0.178$ J. Independent 8- and 16-point Gaussian integration within resolved
solver steps reduced the leading cases' power-integral disagreements below
$3\times10^{-11}$ J. Exact contact/coil reference cases and symbolic component
power identities supplied further checks. These are numerical sensitivity
checks for the stated models, not certified error bounds or hardware uncertainty.

**The selection account.** For a declared event $[t_0,t_1]$, use
$$
D_{\rm event}=E_{\rm start}+\sum_k\int_{t_0}^{t_1}[P_{k,\rm external}]_+dt,
\qquad \mathrm{COP}_{\rm event}=\frac{W_{\rm useful}}{D_{\rm event}}>1.2.
$$
$E_{\rm start}$ is modelled prepared energy above a stated reference. Count
specified external inputs once and use net receiver delivery. Internal transfers
stay internal; final stores are reported separately. Unknown component accounts
and reset can remain open. Use the stated laws and label each result conditional
on its model; no missing supply is inferred from a residual.

**Making the surplus visible.** Mechanical work needs synchronized force and
motion, with a lifted weight as an independent check. Electrical work needs
synchronized voltage and current, with a characterized receiver. A qualifying
case must specify ranges, event bandwidth, timing and calibration uncertainty,
including starting energy, small enough to resolve
$W_{\rm useful}-1.2D_{\rm event}>0$. These requirements guide reassessment and
the search for new candidates.
