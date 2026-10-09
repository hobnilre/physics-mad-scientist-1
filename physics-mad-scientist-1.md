---
title: "Mad Scientist 1"
subtitle: "Four simulation studies for COP greater than one"
author: "Hob Nilre & Bo C. Herlin"
date: "2026-10-09"
abstract: |
  Four open problems invite a computational search for complete-cycle COP
  greater than one. A falling-weight lever, switched transformer, contact chain
  and coupled-coil release connect striking observations to explicit dynamical
  models. Each proposed study follows preparation, useful delivery and reset,
  integrating receiver work and every inward power flow. Exact examples supply
  reference cases; contact and switching laws define the territory to explore.
  The aim is to locate reproducible model behavior, resolve its energy transfers
  and identify the assumptions that make an above-one result possible.
keywords:
  - coefficient of performance
  - dynamical simulation
  - mechanical contact
  - transformer switching
  - coupled coils
---

\begingroup\scriptsize
\noindent PDF created: \pdfbuildtimestamp\par
\noindent Local draft; the GitHub destination below is planned, not published.\par
\noindent Latest on GitHub: \url{https://github.com/hobnilre/physics-mad-scientist-1}\par
\endgroup

# The top four {-}

I want a model that raises a load or charges a receiver, restores its machine
state, and makes every transfer inspectable. The ambition is a coefficient of
performance (COP) greater than one: useful receiver work divided by **all gross
inward energy** over the complete history. Give the output a load, give each
input an integral, and let the trajectories reveal what happened.

This list alternates the two leading mechanical and two leading electrical
questions, preserving their source order within each domain. Begin with the
lever and transformer; their modeling and accounting tools carry into the chain
and coil studies.

1. **The falling-weight lever.** Can contact timing and compliance produce
   receiver work exceeding the model's lifting, release and reset input?
   [OP-CT-HW-01]
2. **The switched transformer.** Can a finite tap-commutation model reach COP
   above one when source, driver and restoration work are included? [OP-TRF-02]
3. **The contact chain.** Can mass order, gaps and branching produce loaded
   COP above one through a complete launch-and-reset cycle? [OP-LR54-03]
4. **The coupled-coil release.** Can a resolved release path deliver more useful
   work than energization, switching and reset supply? [OP-LR48-03]

The clues are a fast launch, different voltages across different terminal pairs,
and growing sums of momentum or flux-linkage magnitudes. Each gives a physical
idea to explore. A simulation can expose the full state history, change one law
at a time, and show exactly which transfer changes the COP.

These are proposed simulation studies, with exact analytic reference cases.
Derive dynamics from forces, circuit constraints and component laws; evaluate
energy independently. Follow promising regions by resolving events and identifying
the responsible law. The final page gives the shared method.

\newpage

# The falling-weight lever

A teeterboard turns the downward arrival of one or two people into the upward
flight of another. Timing, leg compression and board flexibility change the
launch. Replacing performers with guided masses gives a compact model in which
contact timing can be explored against a complete-cycle COP target.

![Illustrative endpoint comparison for three equal masses. The mechanism is schematic; descent and deformation continue during contact.](figures/lever-observation.pdf){#fig:lever-observation width=98%}

\FloatBarrier

**The observation.** Let each mass be $m=70\,\mathrm{kg}$. Two arrive downward
at $u=5\,\mathrm{m/s}$ and one receiver leaves upward at $w=8\,\mathrm{m/s}$.
The selected kinetic terms are
\begin{equation}
K_{\mathrm{in}}=mu^2=1750\,\mathrm{J},\quad
K_{\mathrm{out}}=\tfrac12mw^2=2240\,\mathrm{J},\quad
K_{\mathrm{out}}-K_{\mathrm{in}}=490\,\mathrm{J}.
\label{eq:launch-comparison}
\end{equation}
Their ratio is $32/25$. The contact history connects that comparison to the COP
question: descending masses continue losing gravitational potential energy,
compliance stores and returns work, and active forces can act during contact.

**What made the question open.** An ideal fixed pivot supplies impulse at zero
work because its point of application stays still. The board's rotation, recoil,
catch engagement and separation time therefore matter independently of the
outgoing speed. Models imposing the same takeoff speed can require different
force and actuator-work histories. Those histories are the information to recover.

The passive model has its own scope, separate from the original human hardware
question. Let the launch emerge from its equations. Change the arrival delay and
contact compliance, then ask whether the useful delivery grows faster than all
work needed to prepare and repeat it.

## Simulation: let the launch emerge

Use driver heights $y_i$, lever angle $\phi$, receiver height $y_R$ and their
velocities as states. A rigid lever has inertia $I$ and its center of mass at a
fixed pivot. At signed arm coordinate $a_\alpha$, its contact height is
$h_\alpha=a_\alpha\sin\phi$. Define compression
$\delta_\alpha=h_\alpha-y_\alpha-d_\alpha$, with offset $d_\alpha$.
These definitions determine the contact motion rather than prescribing a launch.

![Lever simulation model, schematic. Evolve masses, rotation and contact states; integrate actuator inputs and work at the outside receiver.](figures/lever-simulation.pdf){#fig:lever-simulation width=98%}

\FloatBarrier

**Specify the contact law.** Start with
$f_\alpha=k_\alpha[\delta_\alpha]_+$, where $[x]_+=\max(x,0)$ and
$f_\alpha$ acts upward on the contacting mass. Newton's equations give
\begin{equation}
m_i\ddot y_i=-m_ig+f_i+u_i,\quad
m_R\ddot y_R=-m_Rg+f_R,\quad
I\ddot\phi=\tau_a-\sum_\alpha f_\alpha h'_\alpha(\phi).
\label{eq:lever-dynamics}
\end{equation}
Here $u_i$ and $\tau_a$ are preparation/reset actuator efforts; the sum includes
driver and receiver contacts. Prescribe finite actuator laws and integrate their
work. A latch or release actuator needs its own law and port. First use elastic
contacts, then declare a dissipative alternative and account for its heat.

**Calculate the COP.** Integrate the complete cycle from a ready state through
lifting, release, relaxation and driven restoration:
\begin{equation}
W_R=\int_{t_0}^{t_1}f_R\dot y_R\,dt,\qquad
\mathrm{COP}_L=\frac{W_R}{D_{\mathrm{act}}+D_{\mathrm{release}}
+D_{\mathrm{other}}}.
\label{eq:lever-cop}
\end{equation}
Each $D$ is gross inward port work. Form $D_{\mathrm{act}}$ from the separate
powers $u_i\dot y_i$ and $\tau_a\dot\phi$, using the common rule on the final
page. Include any added support or control supply in the appropriate input.
Check receiver work against
$m_Rg\Delta y_R+\tfrac12m_R\Delta(\dot y_R^2)$ in this ideal receiver model.

Evaluate the machine's driver kinetic/gravitational, lever rotational and
contact-spring stores from its states. Include the receiver-contact spring
inside the machine but the receiver mass outside. Reposition through actuator
dynamics; retain every transfer through reset.

**Explore and resolve.** Compare one and two drivers, equal and unequal arrival
times, contact stiffness and loaded receiver mass. Hold the prepared state fixed
within each timing comparison while retaining its preparation cost. Locate every
engagement and release event. Refine the timestep at fixed stiffness before
investigating harder contacts as a separate physical limit. Report input, output,
COP and state-return error together. Follow any persistent above-one region
through an independent contact formulation and its explicit work account.

\newpage

# The switched transformer

A transformer tap offers several places to connect a receiver. The motivating
analogy is a planet gear: rotation relative to the carrier differs from rotation
relative to the ring. Electrically, the terminal pair determines the voltage.
A timed return connection is therefore a concrete variable in the COP search.

![Same instantaneous ideal state, shown schematically. Opposed winding voltages add algebraically and give different receiver-terminal voltages.](figures/transformer-observation.pdf){#fig:transformer-observation width=98%}

\FloatBarrier

**The observation.** Winding 1 joins $a,c$ and winding 2 joins $b,a$. Along
one electrical trajectory,
\begin{equation}
V_b-V_c=(V_b-V_a)+(V_a-V_c).
\label{eq:tap-identity}
\end{equation}
An opposed ideal ratio $n=-4$ gives
$V_b-V_a=n(V_a-V_c)$. At $V_a-V_c=1\,\mathrm{V}$, the two receiver
voltages are $-4\,\mathrm{V}$ across $b-a$ and $-3\,\mathrm{V}$ across $b-c$.
The idea is to use different connections during different parts of a cycle.

A lightly loading meter can observe both on essentially the same state.
A loaded return connection changes the current history. A common potential-zero
shift leaves voltage differences unchanged; commutation changes the circuit
itself. A simulation must represent that change in its equations.

**What made the question open.** Fixed-connection descriptions leave the
transition to be specified. Winding current, capacitor charge, clamp conduction
and selector drive all participate. Existing finite models cover particular
transitions; physical switch and gap laws remain questions for the model.
One bounded complete-history comparison required more supply after switching
at matched receiver service. That result supplies a specific comparison to extend.

The opportunity is to vary the actual transition law and timing, follow every
supply and receiver transfer, and determine which choices raise complete-cycle
COP. A voltage comparison starts the question; a resolved loaded history answers
it for the chosen model.

## Simulation: evolve the finite switching network

Build the tapped circuit with winding resistance, a reciprocal inductance
matrix, winding/node capacitances and finite selector and clamp paths.
Use winding currents, capacitor voltages and driver states as dynamic variables.
The return moves between $a$ and $c$ through a declared gate waveform, with an
explicit RC driver and its power supply included.

![Transformer simulation topology. The finite selector and driver are modeled elements; source and receiver powers come from the resulting trajectories.](figures/transformer-simulation.pdf){#fig:transformer-simulation width=98%}

\FloatBarrier

**Assemble the equations.** With one node grounded, a useful network form is
\begin{equation}
\mathbf L\dot{\mathbf i}+\mathbf R\mathbf i=\mathbf A^{T}\mathbf v,\qquad
\mathbf C_n\dot{\mathbf v}+\mathbf A\mathbf i+
\mathbf G_\sigma(\mathbf v)\mathbf v=\mathbf j_{\mathrm{ext}}.
\label{eq:transformer-model}
\end{equation}
$\mathbf A$ has $+1$ at each winding's current-entry node and $-1$ at its exit.
$\mathbf C_n$ is the nodal capacitance matrix; $\mathbf G_\sigma$ represents
resistive, switch and clamp paths in state $\sigma$. External sources and the
receiver supply the signed injections $\mathbf j_{\mathrm{ext}}$. Keep finite
on/off conductances and transition duration explicit. Choose winding signs
consistently, with $L_1,L_2>0$ and $M^2<L_1L_2$ for the two-winding model.

**Compare useful service.** Simulate fixed return at $a$, fixed return at $c$,
and finite commutation. Vary switching phase and transition duration independently
of numerical step size. Use a declared source-amplitude adjustment to match
receiver work and delivery time at a fixed load; retain cases that cannot match.
Compare make-before-break and break-before-make paths as separate topologies.

**Integrate the result.** With $j_R$ entering the outside receiver at $b$,
\begin{equation}
W_R=\int_{t_0}^{t_1}(V_b-V_r)j_R\,dt,\qquad
\mathrm{COP}_T=\frac{W_R}{D_s+D_g+D_{\mathrm{other}}}.
\label{eq:transformer-cop}
\end{equation}
$D_s$ is gross source input and $D_g$ sums independent driver inputs.
Integrate from before energization through relaxation and simulated restoration.
Check winding, capacitor and driver states; carry dissipated energy as heat
or an explicit outward transfer. A constant-capacitance receiver gives the
independent ideal check $W_R=C_R(V_{R,f}^2-V_{R,i}^2)/2$.

Resolve gate edges and clamp onset with a stiff-system solver, then compare an
independent method and finer power quadrature. Track the energy residual without
forcing it to vanish. Report absolute COP beside improvement over the fixed-tap
controls. A persistent above-one result identifies a particular netlist,
transition law and parameter region for deeper examination.

\newpage

# The contact chain

Unequal masses and compliant contacts can pass a disturbance along a chain.
Some masses reverse while others advance; a light terminal mass can become fast.
The COP ambition is to turn those exchanges into useful receiver work exceeding
the complete launch and restoration input.

![Exact two-mass elastic-contact illustration, with $p_0=mu>0$. Momentum arrows show how opposite motion doubles the magnitude sum while the signed total stays fixed.](figures/chain-observation.pdf){#fig:chain-observation width=98%}

\FloatBarrier

**The observation.** A mass $m$ arrives at $u>0$; a mass $3m$ is initially
still. For a lossless Hooke contact of stiffness $k$, compression $\delta$
obeys $m\dot v_1=-k\delta$, $3m\dot v_2=k\delta$ and
$\dot\delta=v_1-v_2$. Starting at $\delta=0$ gives
\begin{equation}
v_1=\frac{u}{4}(1+3\cos\theta),\quad
v_2=\frac{u}{4}(1-\cos\theta),\quad
\theta=t\sqrt{\frac{4k}{3m}}.
\label{eq:chain-pair}
\end{equation}
At $\theta=\pi$, compression returns to zero. The separating momenta are
$-p_0/2$ and $3p_0/2$: their signed sum is $p_0$, their magnitude sum
$2p_0$. Endpoint kinetic energy is $\tfrac12mu^2$ in both cases.

For a free chain, $A_p=\sum_j|p_j|=P+2\sum_{p_j<0}|p_j|$, with
$P=\sum_jp_j$. Internal forces preserve $P$ while opposing motion can increase
$A_p$. Receiver work and the independently evaluated stores connect that
motion to the COP question.

**What made the question open.** A permanent spring can pull as well as push;
a contact releases. Gaps change arrival times, branches change the contact
network, and restitution, plasticity and fixture motion change the laws.
The original free, zero-gap compliant descriptions leave those extensions open.
Increasing stiffness also raises a separate rigid-impact-limit question.

Choose mass order and spacing to make the terminal contact deliver at a useful
moment. Its receiver reacts back on the chain. A simulation can follow every
mass and contact through that feedback while calculating full-cycle COP.

## Simulation: follow the changing contact network

Begin with three translating masses and unilateral spring contacts. Declare
mass ratios, gaps and the receiver load before exploring timing; a ratio such as
$1:3:1/2$ is an illustrative starting configuration. Prepare incidence through
a finite launcher force, then evolve the contacts and receiver together.

![Contact-network simulation, schematic. Integrate all mass states, contact events, launcher/reset work and useful receiver delivery. The branch is a separate model configuration.](figures/chain-simulation.pdf){#fig:chain-simulation width=98%}

\FloatBarrier

**Evolve the states.** For the line, let $\mathbf B$ have $-1$ at an edge's
left mass and $+1$ at its right mass, and let
$\mathbf M=\operatorname{diag}(m_j)$. Then
\begin{equation}
\dot{\mathbf x}=\mathbf v,\qquad
\mathbf M\dot{\mathbf v}=\mathbf B\mathbf f+\mathbf u-\mathbf e_N f_R,
\qquad \dot{\boldsymbol\delta}=-\mathbf B^T\mathbf v.
\label{eq:chain-model}
\end{equation}
$\mathbf u$ contains external actuator forces; $\mathbf e_N$ selects the
terminal mass. Offset each compression by its initial gap. Set
$f_e=k_e[\delta_e]_+$, with $[x]_+=\max(x,0)$, as the first contact law.
For a dissipative variant, add $c_e[\dot\delta_e]_+$ only while $\delta_e>0$,
where $c_e\geq0$. Its dissipated power is $c_e[\dot\delta_e]_+^2$ during contact.

Couple the terminal mass to an outside mass-spring receiver through an explicit
receiver-contact law. Include that contact's spring inside the machine.
For a branch, replace the line incidence relation by the Jacobian of the
declared contact geometry and track the extra mass. Compare laws and geometries
as distinct models.

**Calculate useful delivery.** At the receiver interface,
\begin{equation}
W_R=\int_{t_0}^{t_1}f_Rv_R\,dt,\qquad
\mathrm{COP}_C=\frac{W_R}{D_{\mathrm{launch}}+D_{\mathrm{release}}
+D_{\mathrm{fixture}}+D_{\mathrm{other}}}.
\label{eq:chain-cop}
\end{equation}
Integrate preparation and repositioning forces through the whole history.
Evaluate $\sum_j m_jv_j^2/2+\sum_e k_e[\delta_e]_+^2/2$ independently,
adding receiver-contact and any fixture stores. Track heat for dissipative
contacts. Check an ideal receiver against its kinetic and spring-energy change.

**Search with controls.** Compare zero and nonzero gaps, reverse the mass order,
add one declared branch, and change receiver loading. First reproduce the exact
two-mass contact above. Locate engagement and force-release events, retain
event-side states and refine integration at fixed contact parameters. Increase
stiffness only in a separate sequence. Drive the simulated reset and verify all
masses, springs and thermal states return within declared tolerances. Report COP,
input, output and reset mismatch for every case; investigate an above-one region
by isolating the contact law and event sequence that produced it.

\newpage

# The coupled-coil release

Two inductors exchanging through a capacitor provide an electrical counterpart
to the chain. Their flux linkages can acquire opposite signs while their signed
sum stays fixed. A growing magnitude sum suggests a next step: change the
connection at a chosen moment and route the state into a receiver.

![Exact connected-model curves for the stated zero-coupling illustration. Opposite linkage signs separate the growing magnitude sum from the fixed signed sum.](figures/coil-observation.pdf){#fig:coil-observation width=98%}

\FloatBarrier

**The observation.** In the zero-mutual-coupling limit, take
$L_1=1\,\mathrm{H}$, $L_2=19\,\mathrm{H}$, $C>0$, initial currents
$i_1=10\,\mathrm{A}$ and $i_2=0$, and zero capacitor voltage.
For equal-and-opposite winding voltages,
\begin{equation}
i_1=\frac{1+19\cos\theta}{2}\,\mathrm{A},\quad
i_2=\frac{1-\cos\theta}{2}\,\mathrm{A},\quad
\theta=\omega t,\quad \omega^2=\frac{1/L_1+1/L_2}{C}.
\label{eq:coil-exchange}
\end{equation}
The plotted linkages are $\lambda_j=L_ji_j$. At
$\theta=\arccos(-1/19)$, the first crosses zero. By $\theta=\pi$, the pair
has moved from $(10,0)$ to $(-9,19)\,\mathrm{Wb}$. Their signed sum stays
$10\,\mathrm{Wb}$ while the magnitude sum reaches $28\,\mathrm{Wb}$.
The capacitor is again at zero voltage; magnetic storage is $50\,\mathrm{J}$
initially and $(81+19)/2=50\,\mathrm{J}$ finally.

**What made the question open.** Release changes the circuit that linked the
winding voltages. At finite current, the switch gap, clamp and winding capacitance
provide the next paths; arc behavior may add further state. The connected
solution supplies a precise starting point for asking what those paths deliver.

Choose release time, coupling and winding orientation as design variables.
The COP question compares useful delivery with all work needed to prepare,
switch and restore the modeled circuit. The exact connected solution becomes
a reference test for that larger computation.

## Simulation: resolve the release and its return cycle

Use currents, capacitor voltages, gate states and any declared clamp/core states.
Fix winding geometry within each cycle and represent both switches with finite
conductances and finite transitions. Figure \ref{fig:coil-simulation} supplies
the model topology and the receiver boundary.

![Coil-release simulation topology. Preserve state through finite switching; integrate preparation/reset, driver and receiver power from the same history.](figures/coil-simulation.pdf){#fig:coil-simulation width=98%}

\FloatBarrier

**Build the connected phase first.** With winding resistances $R_1,R_2$,
consistent opposed current references and signed mutual inductance $M$,
\begin{equation}
\begin{pmatrix}L_1&M\\M&L_2\end{pmatrix}
\begin{pmatrix}\dot i_1\\\dot i_2\end{pmatrix}
=
\begin{pmatrix}V_C-R_1i_1\\-V_C-R_2i_2\end{pmatrix},
\qquad C\dot V_C=i_2-i_1.
\label{eq:coil-model}
\end{equation}
Take $L_1,L_2>0$ and $M^2<L_1L_2$. Reproduce the analytic
$M=R_1=R_2=0$ reference before adding release. During release, solve the
new node equations with the same winding constitutive laws; the two winding
voltages need no longer be opposite. Retain currents and capacitor voltages
through finite transitions.

**Give every path a law.** Start with winding resistance, capacitance and a
specified clamp current-voltage law. Drive the gates through explicit source,
resistance and capacitance models. Add a gap/arc state or nonlinear core only
as a separately declared extension. Its state evolution and power exchange
must be supplied. Sweep release phase and both orientations. An illustrative
coupling set is $|M|/\sqrt{L_1L_2}\in\{0,1/2,3/4\}$. Compare zero-current
and finite-current release with equal prepared states.

**Compute the COP and stores.** Integrate receiver power and each gross input
through energization, exchange, release, relaxation and modeled reset:
\begin{equation}
W_R=\int_{t_0}^{t_1}v_Ri_R\,dt,\qquad
\mathrm{COP}_{\mathrm{coil}}=
\frac{W_R}{D_{\mathrm{source}}+D_{\mathrm{driver}}+D_{\mathrm{other}}}.
\label{eq:coil-cop}
\end{equation}
Compute the joint store
$U_M=L_1i_1^2/2+Mi_1i_2+L_2i_2^2/2$ and capacitor stores from the states.
For fixed inductances, $\dot U_M=i_1\dot\lambda_1+i_2\dot\lambda_2$.
A constant-capacitance receiver gives the independent ideal check
$W_R=C_R(V_{R,f}^2-V_{R,i}^2)/2$. Carry winding/clamp losses into thermal
states or outward heat, and integrate the actual reset trajectory.

Refine event location, timestep and quadrature while holding component laws
fixed. Then vary clamp and stray capacitance as physical model choices.
Report COP and numerical sensitivity beside the restored-state error. A
persistent above-one region invites a direct comparison of the models: which
release path changed useful output, which input paid for it, and which law
accounts for the remaining difference?

\newpage

# The same calculation in every model {-}

Declare the machine boundary and all state variables before integrating.
At each crossing port $k$, use inward-positive power $P_k$: $vi$ electrically,
$\mathbf F\cdot\mathbf v$ mechanically, or
$\boldsymbol\tau\cdot\boldsymbol\omega$ rotationally. Effort and motion belong
to the same station and frame. Count shared supplies once. Include any thermal
or environmental input; keep the useful receiver outside.

For the complete interval $[t_0,t_1]$, calculate each port separately:
\begin{align}
D_k&=\int_{t_0}^{t_1}[P_k]_+\,dt,&
X_k&=\int_{t_0}^{t_1}[-P_k]_+\,dt,&
W_k&=D_k-X_k,\label{eq:ports}\\
E_{\mathrm{in}}&=\sum_kD_k,& E_{\mathrm{out}}&=\sum_kX_k,&
r_E&=\Delta U-E_{\mathrm{in}}+E_{\mathrm{out}}.
\label{eq:balance}
\end{align}
Here $[x]_+=\max(x,0)$ and $\Delta U$ is evaluated independently from endpoint
states. Internal contact and clamp transfers explain the history; they are
counted as boundary transfers only when they cross the chosen boundary.
Retained heat is a store, exported heat a transfer.

Let $W_R$ be net useful work into the declared receiver after return flow.
All receiver-to-machine work also contributes to gross input. Report source
return separately. With a resolved positive denominator,
\begin{equation}
\mathrm{COP}=\frac{W_R}{E_{\mathrm{in}}},\qquad
\mathrm{COP}_{\min}=\frac{W_R-\varepsilon_R}
{E_{\mathrm{in}}+\varepsilon_{\mathrm{in}}}.
\label{eq:cop}
\end{equation}
The second expression is a lower bound only when nonnegative error bounds
$\varepsilon_R,\varepsilon_{\mathrm{in}}$ are justified simultaneously for
the fixed model and $W_R-\varepsilon_R>0$. Differences between refined runs
are numerical error estimates, not automatically certified bounds. Declare an
input floor before comparing ratios. Keep component-law uncertainty separate.

**Simulate the complete history.** Begin before preparation from a declared ready
state. Evolve preparation, operation, contact/switching, relaxation and reset.
Return through modeled forces and circuits, recording their work; compare all
relevant endpoint states with stated tolerances. Bound any remaining depletion
independently. Keep delivered work outside while accounting for any backflow.

**Make the numerics answerable.** Check exact reference cases first. Locate
contact and switch events, split power integration there, and retain both event-side
states. Refine timestep, solver tolerances and quadrature independently; compare
another numerical method or formulation. Keep physical stiffness and switch
duration fixed during refinement. Study their limiting values separately.
Evaluate the energy residual afterward, without projecting states onto a desired
balance. Explain any persistent residual within the declared laws and boundary.

**Follow the promising region.** Freeze parameter ranges, loads and comparison
rules before the first sweep. Preserve failures, both residual signs and reset
mismatches. Follow a stable above-one region with independent runs, broader
component-law checks and a reconstructed transfer history. A verified bound
above one establishes a result for that specified model; its physical realization
becomes the next question. Save the model, parameters, event history and work
integrals so another researcher can reproduce the finding and pursue it.
