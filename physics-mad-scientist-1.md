---
title: "Mad Scientist 1"
subtitle: "Four apparatus investigations for COP greater than one"
author: "Hob Nilre & Bo C. Herlin"
date: "2026-10-09"
abstract: |
  Four proposed bench investigations pursue an ambitious goal: a repeatable
  machine that delivers more useful energy than all the energy supplied to it.
  A falling-weight lever, switched transformer, contact chain and coupled-coil
  release each receive one page of apparatus, measurements, controls and open
  questions. A shared method follows energy through preparation, operation and
  reset, so an exciting observation can become a result others can check.
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

The lever starts with scales, rulers, video and calibrated force sensors; the
chain adds timing that separates contacts. Synchronized voltage and current
channels reveal the electrical benches' bidirectional switching power, including
the driver supplies. These are concrete routes from a promising effect to a
readable energy account.

Each following page proposes a first screen and identifies the physics it can
explore. Demonstrating repeatable full-cycle excess output is the experimental
challenge. The final page gives all four benches the same measurement standard.

\newpage

# The falling-weight lever

**Why it comes first.** A receiver rising through a measured height makes
mechanical delivery visible. A lever with compliant contact can turn a slow
descent into a rapid launch; the question is how much useful work survives a
load, with the work of preparing and restoring the apparatus included.

**The apparatus.** Use a tabletop lever, one or two guided falling masses,
a spring or compliant contact, and a guided receiver. Begin with soft, long
contacts that the instruments can resolve. Compare rigid and compliant contact,
one and two drivers, and simultaneous and delayed arrivals. Choose heights,
masses, spring settings and receiver conditions before evaluating the work.

**The boundary and measurements.** Enclose the lever, driver masses, springs
and release mechanism. Include the drivers' gravitational interaction energy
among the machine's stores; keep the useful receiver outside. Integrate force
times velocity at every preparation, release, receiver and moving-support
interface. Force and velocity must refer to the same contact point and frame.
Record every mass's height and velocity, lever rotation, spring deflection and
support motion through preparation, launch, relaxation and actual reset.

A scale and ruler establish masses and distances. Synchronized video and
calibrated load cells supply motion and force histories. For a rigid receiver
of mass $m$, moving vertically without friction, the force law
$F=m\dot v+mg$ gives the independent work check
\begin{equation}
W_{\mathrm{rec}}=\int_a^b Fv\,dt
=mg(h_b-h_a)+\frac{m}{2}(v_b^2-v_a^2).
\label{eq:receiver}
\end{equation}
Here $F$ is the upward force exerted by the machine, $v=\dot h$, and $g$ is
constant gravitational acceleration. Elastic changes, friction and other
receiver transfers add terms when present. Resolve them and the kinetic change
to turn a height reading into an independent energy check.

**The discriminating control.** Repeat the same rig with compliance removed,
while still measuring active release work. Observe how the receiver work and
the complete input history change together. Replenishing a driver's height or
a spring's compression is a measured preparation or reset input. Record that
work directly, giving the output an independent input measurement to beat.

**The opportunity.** The motivating launch comparison places launch energy
beside potentially available descent energy. The experimental next step is to
measure both alongside the complete preparation and reset. This mass-driven
tabletop adaptation opens a separate investigation from human teeterboard
motion, with its own mechanical model and protocol. Identifying flexure,
support motion and heat storage makes the result more decisive.

A higher launch is a useful observation. The stronger result would be receiver
work exceeding every measured input over a complete history, with independently
checked machine states and an uncertainty margin that survives repetition.

\newpage

# The switched transformer

**Why it comes second.** A tapped transformer offers accessible source and
receiver terminals, while a physical change of connection exposes a specific
unresolved step: the work transferred during commutation. The useful comparison
is how source draw, source return and receiver delivery change together when
the actual return connection moves.

**The apparatus.** Use an isolated, current-limited low-voltage source, a
tapped transformer, a finite switch network, an observable clamp and a resistor
or capacitor receiver. Compare a fixed connection with physical tap commutation
at predeclared phases. Start with edges slow enough for the acquisition system
to resolve. Document the winding connections on each side of the transition
so the comparison follows the actual physical change.

**The boundary and measurements.** Enclose the windings, switches, clamp and
drivers. Simultaneously record voltage and current at the external source,
every independent driver supply and the receiver. Integrate each signed power
separately. Clamp and switch observations locate transfers inside this boundary;
count the useful delivery where it crosses into the receiver.

Follow winding currents, capacitor voltages, magnetic state, controller stores
and temperature through energization, commutation, relaxation and reset.
Check magnetic and thermal return independently alongside repeating voltages.
Shunts and an oscilloscope provide the main work measurements; meters provide
independent checks within their bandwidth. Resistor calorimetry requires a
calibrated thermal response and heat-leak correction.

For an ideal constant-capacitance receiver, $i=C\dot V$ gives a second check:
\begin{equation}
W_C=\int_a^b Vi\,dt
=\int_{V_a}^{V_b}CV\,dV
=\frac{C}{2}(V_b^2-V_a^2).
\label{eq:capacitor}
\end{equation}
Receiver resistance, leakage and dielectric history must be identified before
applying this expression to a real component. Compare endpoint storage with
terminal charging work as two independent views of the same delivery.

**The discriminating controls.** Use the fixed tap, zero-current switching
and a separately calibrated dummy load. Compare declared receiver service,
such as the same delivered work over the same interval, while retaining all
endpoint differences. Include every driver supply and preserve source-return
intervals with their measured sign. Any make-before-break or break-before-make
comparison requires its own stated conducting paths.

**The opportunity.** Finite switching models give the bench a starting account;
measuring the real switch law is the next step. A bounded complete-history
comparison required more total supply in its switched case at matched receiver
service. That supplies a concrete benchmark to improve upon. Actual commutation,
clamp conduction and charge sharing are the physical questions to investigate.

The first useful result is a reproducible map of where the switching work goes.
An improvement becomes compelling when receiver delivery and every driver,
clamp, preparation and reset measurement tell the same story.

\newpage

# The contact chain

**Why it comes third.** A light final mass can leave a chain at an impressive
speed. Unequal masses, separated arrivals and a branch make this an accessible
test of energy concentration and contact timing. The practical question is
whether the terminal motion delivers useful work under load and how that work
compares with preparation and restoration of the whole chain.

**The apparatus.** Arrange three unequal carts or suspended masses with spring
bumpers. Begin in a line. Compare zero gap with two independently measured
nonzero gaps, then compare the line with one branch. Couple the terminal mass
to an instrumented receiver. Fix mass ratios, gaps, arrival conditions and
receiver settings before reading the energy results.

**The boundary and measurements.** Enclose every chain mass and spring.
Preparation, receiver, fixture and release-actuator connections cross the
boundary. Measure every mass with synchronized video or photogates, each
compliant contact with force and displacement, and the receiver with its own
force and motion record. Include fixture motion and any associated support
work. Resolve successive contacts rather than assigning one average force
to the entire event.

Evaluate kinetic energy in every moving mass and elastic energy remaining in
every spring at both endpoints. For an identified linear spring of stiffness
$k$ and compression $x$, the elastic store follows from
$\int_0^x k\xi\,d\xi=kx^2/2$. Include gravitational changes for suspended
configurations, rotation when present, and independently assessed thermal
changes. Keep following the first and middle masses after the last reaches
the receiver: their remaining motion belongs in the result too.

**A useful diagnostic.** For a translating mass with kinetic energy $E$,
\begin{equation}
E=\frac12 mv^2
\quad\Longrightarrow\quad
|v|=\sqrt{\frac{2E}{m}}.
\label{eq:chain}
\end{equation}
At equal kinetic energy a smaller mass is faster. Equation
\eqref{eq:chain} gives a clean reference for interpreting a fast endpoint;
the loaded experiment determines how this chain actually transfers work.
Follow contact work inside the chain, and count useful output once where it
crosses the boundary into the receiver.

**The discriminating controls.** Reverse the mass order and remove the branch.
Compare unloaded motion with nominal and heavier receiver conditions. Preserve
the complete preparation, contact, relaxation and reset history in every case.
A promising terminal-speed result earns a stronger test through all-mass
tracking and measurement of the individual contact events.

**The opportunity.** Nonzero gaps, physical restitution or plasticity,
branching, fixture impulses and hardware behavior extend beyond the bounded
compliant models. Softer contacts make the first measurements accessible.
Progressively harder contacts and different materials then ask new questions,
each with its own identified contact law; the rigid-impact limit remains a
separate target.

The visible effect is concentration of motion. The decisive observation is
loaded receiver work alongside all remaining motion, deformation and measured
inputs, with any unexplained balance retained at its actual sign and size.

\newpage

# The coupled-coil release

**Why it comes fourth.** This experiment focuses on the instant a coupled
circuit acquires a different physical connection. It asks how prepared magnetic
energy, continuing supply work and switching transfers divide among a receiver,
a clamp, winding capacitance and other stores. It reuses the transformer bench's
synchronized electrical measurements while isolating a different event.

**The apparatus.** Prepare two coupled coils through a metered source. Change
one branch's connection and route the resulting transfer into a measured
receiver capacitor or resistor, retaining an observable finite clamp path.
Compare three independently characterized coupling settings, both winding
orientations, and zero-current versus finite-current switching. Vary the clamp
and measured stray capacitance in separately declared configurations.

**The boundary and measurements.** Enclose both coils, the switches, clamp,
drivers and internal capacitors. Record source, independent driver and receiver
powers throughout preparation, release, relaxation and actual reset. Track both
coil currents, winding voltages, receiver charge, temperature and the states
on each side of switching. Resolve the fastest transfer being investigated,
and follow the prepared magnetic store as carefully as the source terminal.

**The joint magnetic store.** For reciprocal, fixed, linear inductances
$L_1,L_2>0$ and signed mutual inductance $M$, with $M^2\leq L_1L_2$, let
$\lambda_1=L_1i_1+Mi_2$ and $\lambda_2=Mi_1+L_2i_2$ be flux linkages.
The inductive power $i_1\dot\lambda_1+i_2\dot\lambda_2$ is the derivative of
\begin{equation}
U_{\mathrm{mag}}=
\frac12 L_1i_1^2+Mi_1i_2+\frac12 L_2i_2^2.
\label{eq:mutual}
\end{equation}
The zero-current state fixes the store's reference. Identify the inductances
independently, and define current directions and winding orientation consistently
with the sign of $M$. Retain the mutual term alongside both individual-coil terms.
Winding resistance, capacitance, core hysteresis and temperature require their
own transfers or stores. Equation \eqref{eq:mutual} describes a reversible linear
magnetic law; a nonlinear core opens a separate material-history investigation.

**The discriminating controls.** Compare zero-current switching with the
prepared finite-current release, then change coupling, winding orientation,
clamp and capacitance under the declared conditions. Cross-check receiver work
with equation \eqref{eq:capacitor} in its applicable regime or calibrated
resistor calorimetry. Report changes in transfer partition alongside the
complete balance. A change in receiver delivery can accompany a change in
clamp loss or remaining magnetic storage.

**The opportunity.** The connected model tracks its total store alongside a
growing absolute sum; receiver-work measurements give the physical comparison.
Switch and gap laws, arc ignition or restrike, clamp release, winding capacitance
and the full circuit during release remain open hardware questions. A finite
clamped screen can establish the transfer partition over its observed paths
and operating range, creating a firm starting point for the next configuration.

The opportunity is to measure the release itself. Any residual that survives
the joint-store calculation and complete event record deserves an independently
prepared repetition, with its uncertainty and remaining unknowns preserved.

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
