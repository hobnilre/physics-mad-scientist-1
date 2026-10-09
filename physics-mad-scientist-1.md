---
title: "Mad Scientist 1"
subtitle: "Four apparatus investigations for COP greater than one"
author: "Hob Nilre & Bo C. Herlin"
date: "2026-10-09"
abstract: |
  Four open problems pursue an ambitious goal: a repeatable machine that
  delivers more useful energy than all the energy supplied to it. A falling-weight
  lever, switched transformer, contact chain and coupled-coil release each receive
  two pages: the observation and its background, then an experiment that develops
  the idea. Eight explanatory figures and exact illustrative mathematics connect
  the physical questions to measurable transfers. A shared energy account follows
  preparation, operation and reset.
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

1. **The falling-weight lever.** Can compliant launch deliver a receiver gain
   that survives measured preparation and reset? [OP-CT-HW-01]
2. **The switched transformer.** Where does the work go when a winding
   connection is physically changed under load? [OP-TRF-02]
3. **The contact chain.** How do unequal masses, gaps and branching change
   loaded transfer when every mass is tracked? [OP-LR54-03]
4. **The coupled-coil release.** How is transfer divided among receiver,
   clamp and parasitic stores when a coupled circuit opens? [OP-LR48-03]

The starting points are striking: a fast launch, different voltages across
different terminal pairs, and growing sums of momentum or flux-linkage
magnitudes. Each suggests a physical idea worth following. Their open questions
concern the contact histories and changing connections that turn the idea into
an apparatus.

Each two-page treatment explains the observation with a figure and mathematics,
then develops an experiment with its own schematic and work account.
Demonstrating repeatable full-cycle excess output is the challenge. The final
page supplies the common measurement standard.

\newpage

# The falling-weight lever

A teeterboard turns the downward arrival of one or two people into the upward
flight of another. A brief contact produces a dramatic launch, and changes in
timing, leg compression or board flexibility can alter it. The falling-weight
lever brings this contact-transfer idea to a tabletop, replacing performers
with guided masses while keeping the question: how does the launch acquire
its outgoing motion?

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
This illustrative difference invites a reconstruction of the contact history.
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
Its attraction is that the launch, the continued descent and the restoration
of the machine can all be followed in a compact mechanical system.

\newpage

## Experiment: shape the contact history

Figure \ref{fig:lever-experiment} asks how compliance and arrival delay change
receiver work. Choose masses, initial heights and receiver conditions before
comparing the results, connecting the launch to its contact history.

![Proposed lever experiment, schematic. The receiver is outside the machine boundary; its interface carries the measured force and velocity.](figures/lever-experiment.pdf){#fig:lever-experiment width=98%}

\FloatBarrier

**Make the comparison informative.** Begin with one falling mass and compare a
rigid contact with an identified spring contact. Add the second mass, first
with simultaneous arrival and then with a declared delay $\Delta t$. Record
the contact duration $\tau_c$; the ratio $\Delta t/\tau_c$ describes whether
the arrivals overlap. Repeat with unloaded, nominal and heavier receiver
conditions so timing effects can be followed under useful delivery.

**Measure work and motion together.** A guided receiver of mass $m_R$, acted
on by an upward force $F_R$, obeys $F_R=m_R\dot v_R+m_Rg$ in the frictionless,
rigid, vertical idealization. Multiplication by $v_R=\dot h_R$ and integration
give the independent check
\begin{equation}
W_R=\int_a^b F_Rv_R\,dt
=m_Rg\,\Delta h_R+\frac{m_R}{2}\Delta(v_R^2).
\label{eq:lever-receiver}
\end{equation}
Here $W_R$ is positive into the outside receiver. Receiver friction, deformation
or other transfers add terms when present. Synchronized force and motion at the
same interface connect the measured work to its height and velocity changes.

For a rigid lever whose center of mass lies at the fixed pivot, translating
drivers and linear springs, the mechanical store is
\begin{equation}
U_{\mathrm{mech}}=
\sum_i\left(\frac12m_iv_i^2+m_igh_i\right)
+\frac12I\dot\theta^2+\sum_j\frac12k_j\delta_j^2.
\label{eq:lever-store}
\end{equation}
The sums cover driver masses and springs; $I$ is the pivot inertia and
$\delta_j$ a spring deformation. Additional flexural and thermal stores are
assessed separately. The gravitational reference is fixed.

**Follow what changes.** Video and calibrated force sensors reveal whether a
timing adjustment changes recoil, contact duration or release. Track preparation,
release-actuator and moving-support work, then measure actual restoration.
A fixed ideal pivot has zero work. If the support moves, include its work and
the changed lever kinematics. Compare delivery, retained stores and inputs
using the shared account on the final page.

A reproducible contact-history change links the stronger launch to useful work
and the complete-cycle COP question.

\newpage

# The switched transformer

A transformer with a tap offers several places to connect a receiver. The
motivating analogy is a planet gear: rotation relative to its carrier differs
from rotation relative to the ring. In the electrical counterpart, the chosen
terminal pair determines the observed voltage. The return connection becomes
an interesting physical design variable.

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
cycle. The question is how that sequence divides transfer among receiver,
source return and remaining stores. The attractive territory lies in the
changing circuit, including the work of making the change.

\newpage

## Experiment: move the return connection

Figure \ref{fig:transformer-experiment} keeps the receiver at $b$ and changes
its return $r$ between $a$ and $c$. Use an isolated, current-limited low-voltage
source and specified finite switch, clamp and driver paths.

![Functional schematic of tap commutation. The selector changes the receiver return; the clamp and driver belong inside the measured machine boundary.](figures/transformer-experiment.pdf){#fig:transformer-experiment width=98%}

\FloatBarrier

**Separate the choices.** Compare fixed return at $a$, fixed return at $c$,
and physical commutation at predeclared phases. A zero-current transition is a
useful reference for finite-current switching. Keep the receiver service
explicit, for example delivery of the same work over the same interval, and
retain actual endpoint differences. Changing the return can change the source
current and the winding states as well as the receiver voltage.

If $j_R$ enters the receiver at $b$, its delivered work and the independently
supplied driver's input are
\begin{equation}
W_R=\int_{t_0}^{t_1}(V_b-V_r)j_R\,dt,\qquad
W_g=\int_{t_0}^{t_1}v_gi_g\,dt.
\label{eq:transformer-work}
\end{equation}
Use synchronized channels over the same interval $[t_0,t_1]$ to record the
source power as well. Preserve positive draw and negative return separately.
Internal clamp work helps locate the transfer within the machine boundary.

**Check a reconnection event.** Connect ideal capacitors $C_A,C_B$, initially at
$V_A,V_B$, only through a resistance $R$. With
$C_* = C_AC_B/(C_A+C_B)$, the voltage difference decays as
$\Delta V(t)=(V_A-V_B)e^{-t/(RC_*)}$. Integrating its resistor power gives
\begin{equation}
W_{\mathrm{eq}}(T)=\int_0^T\frac{\Delta V(t)^2}{R}\,dt
=\frac{C_*}{2}(V_A-V_B)^2\left(1-e^{-2T/(RC_*)}\right).
\label{eq:equalization}
\end{equation}
Equal initial voltages give zero work; finite $T$ retains a voltage difference.
Compare the power integral with independently evaluated capacitor stores.
This separate control gives the switching measurement a known event to resolve.

**Follow the real transition.** Resolve the switching edge, clamp conduction
and capacitor states, then follow relaxation and actual reset. Identify
magnetic, controller and thermal endpoint stores independently. Comparing
make-before-break and break-before-make sequences can reveal where a proposed
timing advantage is spent or delivered.

The result connects receiver-work changes to the physical connection and its
complete transition history.

\newpage

# The contact chain

A row of unequal masses and compliant contacts can pass a disturbance from
one end to the other. Some masses reverse while others advance, and a light
terminal mass can become fast. The motivating question is how to organize
these local exchanges into a strong final delivery.

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
the open question concerns its extension to loaded chains, changing contact
networks and real release laws.

\newpage

## Experiment: turn internal motion into delivery

Start with three unequal carts and spring bumpers, as in Figure
\ref{fig:chain-experiment}. First establish the line, then add a branch as a
separately declared configuration. The receiver turns an impressive endpoint
motion into a directly measurable transfer.

![Proposed chain experiment, schematic. Gaps change arrival timing; an optional branch is a separate configuration. Track every mass and the outside receiver.](figures/chain-experiment.pdf){#fig:chain-experiment width=98%}

\FloatBarrier

**Vary the ingredients that raised the question.** Compare zero gaps with two
measured nonzero gaps $d_{12},d_{23}$. Reverse the mass order, and compare
unloaded, nominal and heavier receiver conditions. Hold the prepared incidence
fixed within each comparison and record every contact's engagement and release.
The branch adds a new contact network and its own motion measurements.

**Keep the contact model visible.** For the simple unilateral Hooke model,
a contact with compression $\delta_e$ has force
$f_e=k_e[\delta_e]_+$, where $[x]_+=\max(x,0)$. Integrating this force with
respect to compression gives the corresponding store. For translating masses
on a horizontal rail,
\begin{equation}
U_{\mathrm{mech}}=
\sum_j\frac{p_j^2}{2m_j}
+\sum_e\frac12 k_e[\delta_e]_+^2.
\label{eq:chain-store}
\end{equation}
Negative compression denotes an open gap. Gravity, rotation and fixture
elasticity add stores when the chosen apparatus requires them. A measured
damped or plastic contact needs its own force and release law; follow any
remaining deformation after separation.

**Observe the full motion.** Synchronized video or photogates give every
mass's position and velocity. Force sensors and contact displacement identify
the transfers. For each mass and the receiver,
\begin{equation}
J_j=\int_{t_0}^{t_1}F_j^{\mathrm{net}}\,dt
=p_j(t_1)-p_j(t_0),\qquad
W_R=\int_{t_0}^{t_1}F_Rv_R\,dt.
\label{eq:chain-work}
\end{equation}
The impulse check locates changes in momentum; the receiver integral measures
useful work. Force and velocity refer to the same receiver interface. Contact
transfers remain internal when all chain masses and springs are enclosed.

**Follow the consequence of loading.** Does the receiver shift a release time,
reverse a middle mass, or leave a spring compressed? Record preparation,
fixture and release-actuator inputs, followed by relaxation and actual reset.
Keep thermal stores or exported heat in the appropriate part of the account.

Softer contacts make the first histories easier to resolve. Progressively
harder contacts then explore the rigid-contact question with identified
bandwidth and event-side states. Each configuration can reveal how a growing
internal-motion measure becomes useful delivery under a real load.

\newpage

# The coupled-coil release

Two inductors exchanging through a capacitor provide an electrical counterpart
to the contact chain. Flux linkages can acquire opposite signs while their
signed sum stays fixed. Their magnitude sum then grows, suggesting a provocative
next step: change the connection at a chosen moment and direct the evolving
state into a receiver.

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
observation explicit. Actual release adds a new design opportunity: discover
how the paths created by switching partition the prepared state and subsequent
input work.

\newpage

## Experiment: choose and observe the release

Figure \ref{fig:coil-experiment} separates preparation, connected exchange and
loaded release. In the proposed switching configuration, $S_1$ opens the first
branch and $S_R$ connects the receiver; a clamp retains a finite path for the
first coil's current. Meter preparation and driver supplies independently.

![Functional release schematic. Coil-current reference arrows are opposed; the finite clamp and both switches belong inside the machine boundary.](figures/coil-experiment.pdf){#fig:coil-experiment width=98%}

\FloatBarrier

**Make the alternatives concrete.** Compare release when $i_1=0$ with
predeclared finite-current release times $t_s$. Then compare three identified
coupling settings and both winding orientations. Change clamp and stray
capacitance only in separately documented configurations. Use the exact
zero-coupling example as a connected-state check before interpreting a different
physical assembly.

**Account for the joint state.** With fixed reciprocal linear inductances,
signed mutual inductance $M$ and consistent current directions,
\begin{equation}
U_M=\frac12L_1i_1^2+Mi_1i_2+\frac12L_2i_2^2,
\qquad U_C=\frac12CV_C^2.
\label{eq:coupled-stores}
\end{equation}
Here $L_1,L_2>0$ and $M^2<L_1L_2$ describe a nonsingular linear model.
Differentiating $U_M$ gives
$i_1\dot\lambda_1+i_2\dot\lambda_2$ for
$\lambda_1=L_1i_1+Mi_2$ and $\lambda_2=Mi_1+L_2i_2$.
Changing a switch connection leaves the actual coils' joint store to be
evaluated on both sides. Nonlinear core history and temperature require
independent identification.

**Resolve where release work goes.** Record both coil currents, winding
voltages, the clamp path and receiver power through a finite transition
$[t_-,t_+]$. For the complete boundary,
\begin{equation}
r_{\mathrm{event}}=
U(t_+)-U(t_-)-\sum_k\int_{t_-}^{t_+}P_k\,dt.
\label{eq:release-event}
\end{equation}
All $P_k$ are inward-positive; $U$ includes the applicable electrical,
controller and thermal stores. Internal clamp transfer is tracked for
attribution, while its heat is retained or exported according to the boundary.

A constant-capacitance receiver provides the independent ideal check
$W_R=C_R(V_{R,f}^2-V_{R,i}^2)/2$; a resistor offers a calibrated thermal check.
Include identified leakage or receiver losses where present. Continue through
relaxation and actual reset, even when the release pulse has ended.

The interesting result is a repeatable change in transfer partition with
release time, orientation or clamp behavior. The complete energy account
establishes how that change affects useful output, retained state and COP.

\newpage

# The same test on every bench {-}

Draw the machine boundary before measuring. At every crossing port $k$, take
power $P_k$ positive inward: $vi$ electrically, $\mathbf F\cdot\mathbf v$
mechanically, or $\boldsymbol\tau\cdot\boldsymbol\omega$ rotationally.
Effort and motion refer to the same station and frame. Include signed heat and
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

Let $E_{\mathrm{useful}}$ be outward work delivered to the declared useful
receivers. Report source return and unwanted heat separately. With a resolved,
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
independently established simultaneous coverage. Declare their coverage and an
input floor before evaluation; an unresolved or smaller input makes the ratio
undefined. Identifying the ports and stores gives this bound its physical meaning.

**Measure the whole history.** Timestamp preparation, operation,
switching/release, relaxation and actual reset, without gaps or double counting.
Split integration at events and retain both event-side states. Measure finite
transitions or separately justify any impulse work. Verify mechanical,
electrical, magnetic, controller and thermal endpoint states as applicable.
Independent store checks establish what a visible return means. Measure reset
work directly and resolve possible depletion before assigning a full-cycle COP.

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
