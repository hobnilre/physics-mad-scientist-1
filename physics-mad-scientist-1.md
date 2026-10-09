---
title: "Mad Scientist 1"
subtitle: "Four apparatus investigations for COP greater than one"
author: "Hob Nilre & Bo C. Herlin"
date: "2026-10-09"
abstract: |
  Four open problems pursue an ambitious goal: a repeatable machine that
  delivers more useful energy than all the energy supplied to it. A falling-weight
  lever, switched transformer, contact chain and coupled-coil release each receive
  one page explaining the background, motivating observation and physical idea
  behind the question. Brief experiments point toward the next discovery; a
  shared energy account connects that discovery to complete-cycle performance.
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

Each page traces that background and explains what made the question open,
ending with a short route to an experiment. Demonstrating repeatable full-cycle
excess output is the challenge. The final page supplies the common energy account.

\newpage

# The falling-weight lever

**Background.** A teeterboard turns the downward arrival of one or two people
into the upward flight of another. It is a vivid starting point for a mad
scientist: a short contact produces a dramatic launch, and changes in timing,
leg compression or board flexibility can change the outcome. The falling-weight
lever brings that idea to the tabletop, replacing the people with guided masses
and a receiver while retaining the contact-transfer question.

**The observation that starts the inquiry.** Consider an illustrative comparison:
two incoming masses, each $m=70\,\mathrm{kg}$, move downward at
$u=5\,\mathrm{m/s}$, while one receiver of the same mass leaves upward at
$w=8\,\mathrm{m/s}$. Their incoming and outgoing kinetic energies differ by
\begin{equation}
\Delta K_{\mathrm{comparison}}
=\frac{m}{2}(w^2-2u^2)
=\frac{70}{2}(64-50)\,\mathrm{J}
=490\,\mathrm{J}.
\label{eq:launch-comparison}
\end{equation}
That is an invitation to reconstruct the launch. The descending masses can
continue losing gravitational potential energy during contact; elastic
compression can store and return work; active leg forces can contribute along
the way. These chosen endpoint speeds leave those histories to be identified.

**Why this became an open problem.** The launch also exchanges momentum with
the support. An ideal fixed pivot can deliver an impulse while doing zero work,
because its point of application stays still. Momentum delivered to the flyer
and work delivered to the flyer therefore require different accounts. Board
bending, leg stroke, catch engagement and the instant of separation make the
route between the endpoints still richer.

Models with the same prescribed takeoff speed can have different force histories
and active-work requirements. Watching the final flight alone leaves those
possibilities together. The associated hardware question organizes the missing
force, motion and calibration records needed to distinguish them. Takeoff time,
board recoil, contact force and compression history are clues to the underlying
mechanism.

**The idea worth pursuing.** Replace active performers with falling masses and
let geometry, compliance and arrival timing do the organizing. A spring can
receive work during one part of the motion and return it while the receiver
moves differently. Two arrivals may interact through the board's ongoing
rotation and deformation. The attractive question is how deliberately shaping
that sequence changes useful delivery, including the work needed to prepare
and restore the machine. This passive version is a proposed adaptation with its
own model, separate from the human apparatus.

**A first experiment.** Compare a rigid and a compliant tabletop lever, then
vary the delay between two falling masses. Track their motion and the receiver's
force and displacement, including preparation and reset. One compact comparison
can reveal whether compliance changes the transfer history in the way the idea
requires.

\newpage

# The switched transformer

**Background.** A transformer winding with a tap offers several places to
connect a receiver. The motivating analogy is a planet gear: its rotation
relative to its carrier differs from its rotation relative to the ring. For
the transformer, the corresponding choice is the pair of terminals across
which voltage is observed. This makes the return connection an interesting
part of the apparatus.

**The observation that starts the inquiry.** Call the terminals $a,b,c$.
Winding 1 lies between $a$ and $c$; winding 2 between $b$ and $a$. On the same
electrical trajectory, their voltage differences satisfy
\begin{equation}
V_b-V_c=(V_b-V_a)+(V_a-V_c).
\label{eq:tap-identity}
\end{equation}
For an ideal opposed winding ratio of $-4$ and an input
$V_a-V_c=1\,\mathrm{V}$, winding 2 gives $V_b-V_a=-4\,\mathrm{V}$ and the
series connection gives $V_b-V_c=-3\,\mathrm{V}$. Both readings describe the
same instant. The tempting idea is to exploit the two connections during
different parts of a cycle.

A lightly loading meter reveals the two voltages. A receiver drawing current
also changes the source's return path and the subsequent electrical motion.
Each loaded connection consequently has its own current history. Shifting the
numerical zero of every potential leaves the differences unchanged; moving the
receiver's actual return wire creates the physical intervention.

**Why this became an open problem.** Comparing two fixed connections leaves a
third piece of physics to supply: the transition between them. A winding may
still carry current when its switch opens, and a capacitor may still hold
voltage when a new connection is made. Current then follows a clamp, winding
capacitance, an arc or another conducting path. Capacitors can redistribute
charge. The selector and its driver participate in the same event.

The original fixed-connection descriptions retained current paths through their
declared changes. They left actual opening and tap commutation to a fuller
switching description. Later finite models provide examples of how that
transition can be represented, while the real switch and gap laws remain to
be identified. A bounded complete-history comparison required more supply in
its switched case at matched receiver delivery, giving further designs a
concrete benchmark.

**The idea worth pursuing.** Treat connection and timing as physical design
variables. Can the receiver be connected where the evolving winding and
capacitor states favor delivery, then reconnected for a different part of the
cycle? How much of the subsequent transfer reaches the receiver, returns to
the source or stays in the machine? The open question lives in this changing
circuit and its real switching behavior.

**A first experiment.** Compare a fixed tap with a physically commutated tap
on an isolated, current-limited low-voltage bench. Keep the receiver and clamp
observable, and record synchronized source, driver and receiver power through
switching and reset. This gives the proposed timing idea a direct comparison.

\newpage

# The contact chain

**Background.** A row of unequal masses joined by springs or compliant
contacts can pass a disturbance from one end to the other. Some masses reverse
while others keep advancing; a light terminal mass can acquire a large speed.
The interesting possibility is to organize many local exchanges into a strong
final delivery. Mass order, contact duration and the arrival sequence become
design choices.

**The observation that starts the inquiry.** The underlying models track both
the signed total momentum $P$ and the sum of momentum magnitudes $A_p$. If
$p_j$ is the momentum of mass $j$ along the line, then
\begin{equation}
A_p=\sum_j |p_j|
=P+2\sum_{p_j<0}|p_j|,
\qquad P=\sum_j p_j.
\label{eq:momentum-magnitudes}
\end{equation}
In a free chain, equal-and-opposite internal forces leave $P$ unchanged.
Equation \eqref{eq:momentum-magnitudes} shows how $A_p$ can nevertheless grow
as backward and forward motion develop together. More motion in opposing
directions can coexist with the same signed total.

That distinction is central to the original curiosity. Kinetic energy follows
the separate expression $\sum_j p_j^2/(2m_j)$, with $m_j$ the individual masses;
compressed contacts carry elastic stores as well. The growing magnitude sum,
the terminal speed and the energy available to a receiver are three different
views of the evolving chain. Their relationship makes the system worth exploring.

**Why this became an open problem.** A spring joining two masses can push and
pull continuously. A collision contact pushes during compression and releases
when the bodies separate. Thus the set of interacting pairs changes during
the motion. In the initial compliant descriptions the bodies start with zero
gaps, the chain is free of fixtures, and the contact law sets a finite duration.

Actual gaps introduce travel between contacts and alter which events overlap.
A branch offers more than one route for the impulse. Plastic deformation,
restitution and fixture motion introduce further physical behavior. Making a
contact increasingly stiff also raises a distinct question: what limiting
impulse and work describe the event? These are the extensions that produced
the selected OP. They connect a bounded compliant-chain description to richer
physical contact networks.

**The idea worth pursuing.** Use the spacing and mass order to arrange when
the terminal mass encounters the next transfer. A branch could change the
timing or division of that transfer; a receiver feeds its reaction back into
the chain. This turns the striking internal motion into a concrete design
question: which combinations concentrate useful delivery, and what preparation
and remaining stores accompany them?

**A first experiment.** Start with three unequal masses and spring bumpers.
Compare touching and separated starts, then reverse the mass order. Track every
mass and spring while a receiver takes work from the end. The full preparation
and reset account connects the visible motion to the COP question.

\newpage

# The coupled-coil release

**Background.** Two inductors exchanging through a capacitor provide an
electrical counterpart to the contact chain. Flux linkages can develop opposite
signs while their signed sum stays fixed. The sum of their magnitudes can then
grow. The provocative next idea is to change the connection at a chosen moment
and direct part of that evolving state into a receiver.

**The observation that starts the inquiry.** A transparent ideal example uses
the zero-mutual-coupling limit, $L_1=1\,\mathrm{H}$ and
$L_2=19\,\mathrm{H}$, connected through a capacitor $C>0$. Initially,
$i_1=10\,\mathrm{A}$, $i_2=0$ and the capacitor voltage is zero. For the
equal-and-opposite winding-voltage connection, the exact LC solution is
\begin{equation}
i_1=\frac{1+19\cos\theta}{2}\,\mathrm{A},
\qquad
i_2=\frac{1-\cos\theta}{2}\,\mathrm{A},
\label{eq:coil-exchange}
\end{equation}
where $\theta=\omega t$ and $\omega^2=(1/L_1+1/L_2)/C$.
At half an exchange cycle, $\theta=\pi$, the currents are $-9$ and
$1\,\mathrm{A}$ and the capacitor voltage returns to zero. The flux linkages
$\lambda_j=L_ji_j$ have moved from $(10,0)$ to $(-9,19)\,\mathrm{Wb}$.
Their signed sum stays $10\,\mathrm{Wb}$ while their magnitude sum rises from
$10$ to $28\,\mathrm{Wb}$.

The independently evaluated magnetic store is $50\,\mathrm{J}$ initially and
$(81+19)/2=50\,\mathrm{J}$ at this endpoint. The example makes the motivating
distinction visible: a growing flux-linkage magnitude and redistributed stored
energy occur together. It supplies a precise starting state from which to ask
what a different connection would deliver.

**Why this became an open problem.** Opening a branch changes the equations
that linked the two winding voltages. The relation supporting the connected
exchange must be reconsidered on the new circuit. Ideal zero-current opening
offers a clean special case; finite-current opening brings the switch gap,
clamp, winding capacitance and possible arc into the motion.

The real release therefore needs its own physical description. Which path
carries the current? How does the clamp release? Can an arc reignite? What
remains in the winding and capacitor states? These missing device laws and
the complete circuit during release are the selected OP.

**The idea worth pursuing.** Choose the release time, coupling and winding
orientation to steer the transfer into a receiver. With fixed reciprocal linear
coupling, the magnetic store includes $Mi_1i_2$ in addition to
$L_1i_1^2/2+L_2i_2^2/2$, where $M$ is the signed mutual inductance.
The connected example is a starting comparison; the physical release asks a
new question about the paths created by switching.

**A first experiment.** Prepare both coils through a metered source and release
into a capacitor or resistor through an observable clamp. Compare zero-current
and finite-current release, tracking both coil currents and receiver work.
Include driver supplies, preparation and reset in the same account.

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
