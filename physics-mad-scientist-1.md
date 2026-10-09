---
title: "Mad Scientist 1"
subtitle: "Four apparatus investigations for COP greater than one"
author: "Hob Nilre & Bo C. Herlin"
date: "2026-10-09"
abstract: |
  Four open problems pursue an ambitious goal: a repeatable machine that
  delivers more useful energy than all the energy supplied to it. A falling-weight
  lever, switched transformer, contact chain and coupled-coil release supply four
  routes to investigate complete-cycle COP. Each experiment compares useful
  receiver work with all gross inward energy through preparation, operation and
  actual reset. Background, explanatory figures and exact illustrative mathematics
  connect each motivating observation to that test. The target is a reproducible
  COP lower bound above one with independently checked machine states.
keywords:
  - energy measurement
  - mechanical contact
  - transformer switching
  - coupled coils
  - coefficient of performance
---

\begingroup\scriptsize
\noindent PDF created: \pdfbuildtimestamp\par
\noindent Local draft; the GitHub destination below is planned, not published.\par
\noindent Latest on GitHub: \url{https://github.com/hobnilre/physics-mad-scientist-1}\par
\endgroup

# The top four {-}

I want an apparatus that raises a load or charges a receiver, does it again,
and leaves an energy record another experimenter can check. The ambition is a
coefficient of performance (COP) greater than one: useful receiver energy
divided by **all gross inward energy** over the complete history. Give the
exciting output a receiver, give every input a meter, and see what survives.

This list alternates the two leading mechanical and two leading electrical
investigations, preserving their order within each domain. The first pair
starts the work; the second reuses much of its instrumentation. Rank sets
experimental priority. The COP of each apparatus is a quantity to measure.

1. **The falling-weight lever.** Can timed compliant launch deliver more
   receiver work than the full lifting, release and reset input? [OP-CT-HW-01]
2. **The switched transformer.** Can physical tap commutation achieve COP
   above one with source, driver and reset inputs measured? [OP-TRF-02]
3. **The contact chain.** Can mass order, gaps and branching produce loaded
   COP above one over preparation, delivery and reset? [OP-LR54-03]
4. **The coupled-coil release.** Can timed release deliver more receiver work
   than complete energization, switching and reset require? [OP-LR48-03]

The starting points are striking: a fast launch, different voltages across
different terminal pairs, and growing sums of momentum or flux-linkage
magnitudes. Each suggests a physical idea worth following. Their open questions
concern the contact histories and changing connections that turn the idea into
an apparatus.

\newpage

# The falling-weight lever

A teeterboard turns the downward arrival of one or two people into the upward
flight of another. A brief contact produces a dramatic launch, and changes in
timing, leg compression or board flexibility can alter it. The falling-weight
lever brings this contact-transfer idea to a tabletop, replacing performers
with guided masses. Its COP question is whether timed contact can deliver more
useful receiver work than preparing and restoring the apparatus requires.

![Illustrative endpoint comparison for three equal masses. The central mechanism is schematic; descent and deformation continue during contact.](figures/lever-observation.pdf){#fig:lever-observation width=98%}

\FloatBarrier

**The observation.** In Figure \ref{fig:lever-observation}, each mass is
$m=70\,\mathrm{kg}$. Two arrive downward at $u=5\,\mathrm{m/s}$; one receiver
leaves upward at $w=8\,\mathrm{m/s}$. The selected kinetic terms give
\begin{equation}
K_{\mathrm{in}}=mu^2=1750\,\mathrm{J},\quad
K_{\mathrm{out}}=\frac12mw^2=2240\,\mathrm{J},\quad
K_{\mathrm{out}}-K_{\mathrm{in}}=490\,\mathrm{J}.
\label{eq:launch-comparison}
\end{equation}
The selected kinetic ratio is $2240/1750=32/25$. Turning that motivating
comparison into a COP test requires the whole contact and preparation history.
The descending masses continue losing gravitational potential energy; compliant
legs or a bending board can store and return work; active forces can contribute
during the same interval. Chosen endpoint speeds leave these histories to be
identified.

**What made the question open.** The support adds another intriguing feature.
An ideal fixed pivot can deliver an impulse while doing zero work, because its
point of application stays still. Momentum and work therefore follow different
accounts. The board's rotation, elastic recoil, catch engagement and separation
time connect the incoming motion to the outgoing flight.

Models with the same prescribed takeoff speed can require different active
work and contact-force histories. Takeoff time, board recoil and compression
history distinguish mechanisms that a final flight height leaves together.
The associated hardware question organizes the force, motion and calibration
records needed to make that distinction.

**The physical idea.** Let falling masses replace active performers, then use
geometry, compliance and arrival timing to organize delivery. A spring receives
work during one part of the motion and returns it while the receiver moves
differently. A second arrival meets a board already rotating or deforming.
Changing that timing gives a concrete route to explore.

The passive apparatus has its own model, separate from the human teeterboard.
Its attraction is a directly testable COP: useful lift compared with every
input needed to prepare, operate and restore a compact mechanical system.

\newpage

## Experiment: test COP over a full lever cycle

Figure \ref{fig:lever-experiment} turns the launch into a COP measurement.
Start before lifting the drivers; finish restored to the same ready state,
with useful output retained outside the machine.

![Lever COP experiment, schematic. Meter lifting/reset, release and support inputs; measure useful work at the outside receiver.](figures/lever-experiment.pdf){#fig:lever-experiment width=98%}

\FloatBarrier

**Compare complete cycles.** Test rigid and compliant contacts, one and two
drivers, and simultaneous and delayed arrivals $\Delta t$. Fix masses, heights
and load across each configuration's repetitions; vary delay relative to contact
duration. Include unloaded and loaded controls.

**Measure the useful output.** For a guided, rigid receiver of mass $m_R$,
upward interface force $F_R=m_R\dot v_R+m_Rg$ gives, without friction,
\begin{equation}
W_R=\int_{t_0}^{t_1}F_Rv_R\,dt
=m_Rg\,\Delta h_R+\frac{m_R}{2}\Delta(v_R^2).
\label{eq:lever-receiver}
\end{equation}
Synchronize force and motion at that interface. Receiver deformation and
friction need their own terms. Isolate the delivered load and record return flow.

**Meter the denominator.** Each $D_k$ is gross inward port work over the same
full interval, defined on the final page:
\begin{equation}
\mathrm{COP}_{L}=\frac{W_R}{E_{\mathrm{in},L}},\qquad
E_{\mathrm{in},L}=D_{\mathrm{lift}}+D_{\mathrm{release}}
+D_{\mathrm{support}}+D_{\mathrm{other}}.
\label{eq:lever-cop}
\end{equation}
$D_{\mathrm{lift}}$ includes lifting and restoration work; $D_{\mathrm{release}}$
supplies the release mechanism. Include moving-support work and every other
inward transfer. A fixed ideal pivot has zero work. Check driver gravitational
storage independently of input.

**Restore and check the state.** For a rigid lever centered at its fixed pivot,
translating drivers and linear springs,
\begin{equation}
U_{\mathrm{mech}}=\sum_i\left(\frac12m_iv_i^2+m_igh_i\right)
+\frac12I\dot\theta^2+\sum_j\frac12k_j\delta_j^2.
\label{eq:lever-store}
\end{equation}
Here $I$ is pivot inertia and $\delta_j$ spring deformation; the sums exclude
the receiver. Check driver heights and velocities, lever angle, springs and
latches, with flexural and thermal changes separately identified. Moving supports
require their corresponding kinematics and stores.

Report $W_R$, $E_{\mathrm{in},L}$ and the COP lower bound. Pursue a bound
above one with restored states and independent repetitions; contact histories
connect timing to COP.

\newpage

# The switched transformer

A transformer with a tap offers several places to connect a receiver. The
motivating analogy is a planet gear: rotation relative to its carrier differs
from rotation relative to the ring. In the electrical counterpart, the chosen
terminal pair determines the observed voltage. The return connection becomes
a design variable for the COP question: can a timed sequence deliver more
receiver work than all source, switching and reset inputs?

![Same instantaneous ideal state, shown as a topology schematic. Opposed winding voltages add algebraically, giving two different receiver-terminal voltages.](figures/transformer-observation.pdf){#fig:transformer-observation width=98%}

\FloatBarrier

**The observation.** Winding 1 joins terminals $a,c$; winding 2 joins $b,a$.
On one electrical trajectory,
\begin{equation}
V_b-V_c=(V_b-V_a)+(V_a-V_c).
\label{eq:tap-identity}
\end{equation}
An ideal opposed winding ratio $n=-4$ means
$V_b-V_a=n(V_a-V_c)$. With $V_a-V_c=1\,\mathrm{V}$, Figure
\ref{fig:transformer-observation} therefore gives $-4\,\mathrm{V}$ across
$b-a$ and $-3\,\mathrm{V}$ across $b-c$. The tempting idea is to use the two
connections at different stages of a cycle.

A lightly loading meter reveals those voltages on essentially the same state.
A receiver drawing current also changes the return path and subsequent motion.
Each loaded connection has its own current history. Shifting every potential
by the same numerical offset leaves the differences unchanged; moving the
actual return wire creates the physical intervention.

**What made the question open.** Two fixed-connection descriptions leave the
transition between them to be supplied. A winding can still carry current
when its switch opens, and a capacitor can still hold voltage when a new
connection is made. The current then follows a clamp, winding capacitance,
an arc or another conducting path. Charge redistributes, and the selector's
driver participates in the event.

The original descriptions retained current paths through their declared
changes. Actual opening and tap commutation therefore required a fuller
physical account. Later finite models represent particular transitions;
the real switch and gap laws remain to be identified. One bounded
complete-history comparison needed more supply in its switched case at matched
receiver delivery, providing further designs with a concrete benchmark.

**The physical idea.** Connect the receiver where the evolving winding and
capacitor states favor delivery, then reconnect for a different part of the
cycle. Pursue a sequence whose useful output exceeds its complete measured
input. The voltage comparison identifies a switching opportunity; integrating
receiver and supply powers through the actual cycle determines its COP.

\newpage

## Experiment: test COP with physical tap commutation

Figure \ref{fig:transformer-experiment} tests whether moving the receiver return
between $a$ and $c$ can produce COP above one. Use an isolated, current-limited
low-voltage source, finite selector and clamp, and independently metered drivers.

![Transformer COP experiment, functional schematic. Source and driver supplies are inputs; the outside receiver supplies the useful-output measurement. Meter the entire cycle.](figures/transformer-experiment.pdf){#fig:transformer-experiment width=98%}

\FloatBarrier

**Choose a useful service.** Compare fixed return at $a$, fixed return at $c$,
and commutation at declared phases. Adjust a declared drive setting to match
receiver work and delivery time at a fixed load, then compare complete input
and COP. Include zero-current and finite-current switching.

**Integrate output and every supply.** If $j_R$ enters the receiver at $b$,
\begin{equation}
W_R=\int_{t_0}^{t_1}(V_b-V_r)j_R\,dt,\qquad
\mathrm{COP}_{T}=\frac{W_R}{D_s+D_g+D_{\mathrm{other}}}.
\label{eq:transformer-cop}
\end{equation}
Here $D_s=\int_{t_0}^{t_1}[v_si_s]_+\,dt$ is the external source's gross
input, $D_g$ sums the independent driver supplies in the same way, and
$[x]_+=\max(x,0)$. $D_{\mathrm{other}}$ includes every remaining inward
transfer. Keep source return separate and include every supply's preparation
and reset work.

**Check the output independently.** A characterized constant-capacitance
receiver gives the ideal endpoint check
\begin{equation}
W_R=\frac{C_R}{2}\left(V_{R,f}^2-V_{R,i}^2\right).
\label{eq:transformer-receiver}
\end{equation}
Account separately for receiver leakage and dissipation where present. A resistor
with calibrated calorimetry offers another check. Use synchronized voltage/current
channels and a known dummy-load switching transient to check timing and bandwidth.

**Finish the cycle.** Start before energization from a declared ready state.
Record switching, clamp conduction, relaxation and actual reset, ending at that
same machine state. Check winding currents, capacitor voltages, controller state
and magnetic/thermal history independently. The receiver remains outside;
record any energy it sends back. Internal clamp transfer explains delivery and
heating without adding a second boundary output.

Report $W_R$, total gross input and the COP lower bound for every configuration.
A switched design can improve on a fixed tap while its absolute COP remains
below one. The target is a lower bound above one with repeatable restored states;
use the switching records to develop and independently retest that candidate.

\newpage

# The contact chain

A row of unequal masses and compliant contacts can pass a disturbance from
one end to the other. Some masses reverse while others advance, and a light
terminal mass can become fast. The COP ambition is to organize these local
exchanges into useful receiver work exceeding the complete preparation and
reset input.

![Exact two-mass elastic-contact illustration, with $p_0=mu>0$. Arrow lengths represent momenta; opposite motion doubles their magnitude sum while the signed total stays fixed.](figures/chain-observation.pdf){#fig:chain-observation width=98%}

\FloatBarrier

**The observation.** An exact building block makes the effect visible. A mass
$m$ arrives at speed $u>0$; a mass $3m$ is initially still. During a lossless
Hooke contact of stiffness $k$, let $\delta$ be compression. The force laws
$m\dot v_1=-k\delta$, $3m\dot v_2=k\delta$ and
$\dot\delta=v_1-v_2$ give, from $\delta(0)=0$,
\begin{equation}
v_1=\frac{u}{4}(1+3\cos\theta),\qquad
v_2=\frac{u}{4}(1-\cos\theta),\qquad
\theta=t\sqrt{\frac{4k}{3m}}.
\label{eq:chain-pair}
\end{equation}
At $\theta=\pi$, compression returns to zero and the masses separate.
Their momenta are $-p_0/2$ and $3p_0/2$, as in Figure
\ref{fig:chain-observation}. The signed sum remains $p_0$, while the sum of
magnitudes rises from $p_0$ to $2p_0$. Endpoint kinetic energy is
$\tfrac12mu^2$ in both cases.

For a longer free chain, the same distinction is captured by
$A_p=\sum_j|p_j|=P+2\sum_{p_j<0}|p_j|$, where $P=\sum_jp_j$.
Equal-and-opposite internal forces preserve $P$; opposing motion can increase
$A_p$. Kinetic energy, spring storage and receiver work provide complementary
views of that motion.

**What made the question open.** A permanent spring can push and pull;
a collision contact releases. The interacting pairs therefore change during
motion. The starting descriptions used free compliant chains with zero initial
gaps. Gaps introduce travel and change which events overlap. Branches divide
routes, while restitution, plasticity and fixture motion change the contact
physics. Increasing stiffness raises a further question about the limiting
impulse and work.

**The physical idea.** Choose mass order and spacing so a terminal mass meets
the next transfer at a useful moment. Loading that mass feeds a reaction back
through the contacts. The two-mass illustration identifies one mechanism;
the COP test extends it to a loaded chain and asks whether delivered work
exceeds all launch, actuator and restoration inputs. Track every mass while
pursuing that complete-cycle result.

\newpage

## Experiment: measure the loaded chain's COP

Use three unequal carts and spring bumpers, as in Figure
\ref{fig:chain-experiment}. Compare launch and restoration input with useful
receiver work. Mass order, gaps and branching are controls for pursuing COP
above one.

![Chain COP experiment, schematic. Meter launch/reset, release and fixture inputs. The terminal contact delivers useful work to the outside receiver.](figures/chain-experiment.pdf){#fig:chain-experiment width=98%}

\FloatBarrier

**Compare loaded cycles.** Test zero gaps against measured nonzero gaps
$d_{12},d_{23}$, reverse the mass order, and compare the line with a separately
declared branch. Hold the prepared incidence fixed within each comparison;
measure its preparation work. Compare unloaded, nominal and heavier receivers.
A direct launch-to-receiver control can show what adding the chain changes.

**Measure output and total input.** With force and velocity at the same receiver
interface, the primary result is
\begin{equation}
W_R=\int_{t_0}^{t_1}F_Rv_R\,dt,\qquad
\mathrm{COP}_{C}=\frac{W_R}{D_{\mathrm{launch}}+D_{\mathrm{release}}
+D_{\mathrm{fixture}}+D_{\mathrm{other}}}.
\label{eq:chain-cop}
\end{equation}
Each $D_k$ is gross inward port work over the complete cycle. Launch preparation
and repositioning belong in $D_{\mathrm{launch}}$; meter release-actuator and
moving-fixture work separately. Include all other inward transfers. Check receiver
work independently from its calibrated load and endpoint states.

**Follow every internal store.** In the unilateral Hooke model,
$f_e=k_e[\delta_e]_+$, where $[x]_+=\max(x,0)$ and negative compression is
an open gap. Integrating this contact force gives, for horizontal translation,
\begin{equation}
U_{\mathrm{mech}}=\sum_j\frac{p_j^2}{2m_j}
+\sum_e\frac12k_e[\delta_e]_+^2.
\label{eq:chain-store}
\end{equation}
Gravity, rotation and fixture elasticity add stores when present. Damped or
plastic contacts need identified force and release laws, including remaining
deformation. Motion and force records reveal which contacts feed the receiver;
exchanges inside the chain stay internal.

**Close and repeat the history.** Start before launch preparation with carts at
rest in a declared configuration. Record delivery, separation, relaxation and
actual repositioning to that state. Check every mass, spring, fixture, actuator
and relevant thermal state. The receiver retains the delivered work outside the
machine. Meter any return flow during restoration.

Report useful work, all gross input and the COP lower bound for each configuration.
Pursue a bound above one with independent preparations and restored-state checks.
Begin with resolvable soft contacts, then extend the COP test toward harder impacts.

\newpage

# The coupled-coil release

Two inductors exchanging through a capacitor provide an electrical counterpart
to the contact chain. Flux linkages can acquire opposite signs while their
signed sum stays fixed. Their magnitude sum then grows, suggesting a provocative
next step: change the connection at a chosen moment and direct the evolving
state into a receiver. The COP target is output exceeding all energization,
switching and restoration input.

![Exact connected-model curves for the stated zero-coupling illustration. Opposite linkage signs separate the growing magnitude sum from the fixed signed sum.](figures/coil-observation.pdf){#fig:coil-observation width=98%}

\FloatBarrier

**The observation.** Take the zero-mutual-coupling limit,
$L_1=1\,\mathrm{H}$, $L_2=19\,\mathrm{H}$ and $C>0$, initially at
$i_1=10\,\mathrm{A}$, $i_2=0$ and zero capacitor voltage. In the
equal-and-opposite winding-voltage connection, the exact LC solution is
\begin{equation}
i_1=\frac{1+19\cos\theta}{2}\,\mathrm{A},\qquad
i_2=\frac{1-\cos\theta}{2}\,\mathrm{A},\qquad
\theta=\omega t,\quad \omega^2=\frac{1/L_1+1/L_2}{C}.
\label{eq:coil-exchange}
\end{equation}
Figure \ref{fig:coil-observation} plots $\lambda_j=L_ji_j$. The first linkage
crosses zero at $\theta=\arccos(-1/19)$. By $\theta=\pi$, the pair has moved
from $(10,0)$ to $(-9,19)\,\mathrm{Wb}$: the signed sum stays
$10\,\mathrm{Wb}$ while the magnitude sum reaches $28\,\mathrm{Wb}$.

The capacitor voltage is again zero at this endpoint. Independently evaluated
magnetic storage is $50\,\mathrm{J}$ initially and
$(81+19)/2=50\,\mathrm{J}$ finally. A growing linkage magnitude and
redistributed stored energy occur together, giving a precise state from which
to ask what a changed connection would deliver.

**What made the question open.** Opening a branch changes the equations that
linked its winding voltages. The connected relation must be reconsidered on
the new circuit. Ideal zero-current opening is a clean special case;
finite-current opening introduces the switch gap, clamp, winding capacitance
and possible arc. The physical current path, clamp release and complete circuit
during transition become essential parts of the question.

**The physical idea.** Choose release time, coupling and winding orientation
to steer transfer into a receiver. The connected example makes the motivating
observation explicit. Actual release adds the COP experiment: choose a physical
switching path, measure the useful delivery, and compare it with every input
needed to create and repeat that release.

\newpage

## Experiment: test COP from energization to reset

Figure \ref{fig:coil-experiment} tests preparation, exchange, release through
$S_1,S_R$, relaxation and reset. A finite clamp carries the first coil's release
current. The target is useful receiver work exceeding all supplied energy.

![Coil-release COP experiment, functional schematic. Meter preparation/reset and driver supplies; integrate useful receiver work through delivery. Include all other inward ports.](figures/coil-experiment.pdf){#fig:coil-experiment width=98%}

\FloatBarrier

**Compare release strategies.** At each fixed coupling and winding orientation,
compare zero-current and declared finite-current release times $t_s$ from the
same prepared state. Test three coupling settings with geometry fixed within
each cycle. Compare clamp and stray capacitance separately; include a zero-coupling
release reference.

**Make COP the measured result.** For receiver voltage $v_R$ and current $i_R$
entering that receiver,
\begin{equation}
W_R=\int_{t_0}^{t_1}v_Ri_R\,dt,\qquad
\mathrm{COP}_{\mathrm{coil}}=\frac{W_R}{D_{\mathrm{source}}+D_{\mathrm{driver}}
+D_{\mathrm{other}}}.
\label{eq:coil-cop}
\end{equation}
Each $D_k$ is gross inward port work over the full history. Measure the actual
source work of preparing the currents and any capacitor voltage, all independent
driver supplies, and restoration work. Include other inward transfers in
$D_{\mathrm{other}}$ and report source return separately. The initial magnetic
store is an independent state check.

**Account for both coils together.** For fixed reciprocal linear inductances,
consistent current directions and signed mutual inductance $M$,
\begin{equation}
U_M=\frac12L_1i_1^2+Mi_1i_2+\frac12L_2i_2^2,
\qquad U_C=\frac12CV_C^2.
\label{eq:coupled-stores}
\end{equation}
Here $L_1,L_2>0$ and $M^2<L_1L_2$. With $\lambda_1=L_1i_1+Mi_2$ and
$\lambda_2=Mi_1+L_2i_2$, differentiation gives
$\dot U_M=i_1\dot\lambda_1+i_2\dot\lambda_2$. Identify nonlinear magnetic
and thermal states separately where the apparatus requires them.

**Check useful delivery and restoration.** A constant-capacitance receiver has
ideal gain $C_R(V_{R,f}^2-V_{R,i}^2)/2$; account for leakage or loss separately.
Calibrated resistor calorimetry is another independent check. Resolve the switch
and clamp transfers, then continue until the machine returns to its declared
preparation-start state. Check currents, voltages, controller and magnetic/thermal
states on both sides of release and after reset. Retain useful output outside.

Report $W_R$, all gross input and the COP lower bound for each strategy.
Pursue a bound above one on independently prepared, restored cycles. Release
and clamp traces explain the resulting COP.

\newpage

# The same test on every bench {-}

Draw the machine boundary before measuring. At every crossing port $k$, take
power $P_k$ positive inward: $vi$ electrically, $\mathbf F\cdot\mathbf v$
mechanically, or $\boldsymbol\tau\cdot\boldsymbol\omega$ rotationally.
Effort and motion refer to the same station and frame. Input groups in each
experiment are disjoint: count shared supplies once. Include signed heat and
environmental transfers when present. For the complete interval $[a,b]$, define
\begin{align}
W_k&=\int_a^b P_k\,dt=D_k-X_k, &
D_k&=\int_a^b\max(P_k,0)\,dt, &
X_k&=-\int_a^b\min(P_k,0)\,dt,
\label{eq:ports}\\
E_{\mathrm{in}}&=\sum_k D_k, &
E_{\mathrm{out}}&=\sum_k X_k, &
r_E&=\Delta U-E_{\mathrm{in}}+E_{\mathrm{out}}.
\label{eq:balance}
\end{align}
Here $\Delta U=U(b)-U(a)$ is evaluated independently from endpoint states;
$r_E$ is the signed balance residual. Positive $r_E$ denotes outward excess
relative to measured inputs and store change. Heat retained inside is a store
change; heat crossing the boundary is a transfer. Count each once.

Let $E_{\mathrm{useful}}=W_R$ be net useful work delivered to the declared
outside receiver, after any return flow. All inward receiver transfers also
enter $E_{\mathrm{in}}$. Report source return and unwanted heat separately. With a resolved,
positive input denominator, the ratio and its conservative measurement bound are
\begin{equation}
\mathrm{COP}=\frac{E_{\mathrm{useful}}}{E_{\mathrm{in}}},
\qquad
\mathrm{COP}_{\mathrm{lower}}=
\frac{E_{\mathrm{useful}}-B_{\mathrm{out}}}
{E_{\mathrm{in}}+B_{\mathrm{in}}}.
\label{eq:cop}
\end{equation}
The nonnegative bounds $B_{\mathrm{in}}$ and $B_{\mathrm{out}}$ must have
independently established simultaneous coverage. Use this lower bound when
$E_{\mathrm{useful}}-B_{\mathrm{out}}>0$. Declare coverage and an input floor
before evaluation; an unresolved or smaller input makes the ratio undefined. Identifying the ports and stores gives this bound its physical meaning.

**Measure the whole history.** Start before preparation in a reproducible ready
state; finish restored to that state with useful output retained outside.
Timestamp preparation, operation, switching/release, relaxation and actual reset
without gaps or double counting.
Split integration at events and retain both event-side states. Measure finite
transitions or separately justify any impulse work. Verify mechanical,
electrical, magnetic, controller and thermal endpoint states as applicable.
Measure reset work directly and bound any remaining depletion independently.
Use the same boundary for every comparison and every repetition.

**Calibrate and compare.** Establish gains, offsets, timing skew, bandwidth
and correlated errors with known loads or motions. Use simultaneous channels,
independent receiver checks and event-resolved integration checks. Finer
acquisition must resolve the actual events. Predeclare drive levels, receiver
loads, independent preparations and controls; retain failed starts and both
residual signs. Assess measurement, integration and model uncertainty separately.

**Follow the interesting result.** A lower COP bound above one, supported by
the boundary and endpoint checks, earns independent repetition. An unexplained
deficit also points to physics worth investigating. Keep exploratory adjustments
separate from fresh confirmation measurements. Start with the lever and
transformer, then carry the instruments into the contact chain and coil release.
Build the strongest experiment, follow the unexpected result, and make every
apparent win survive another meter and another independent preparation.
