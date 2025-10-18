FINFET CHARACTERISATION
<img width="940" height="484" alt="image" src="https://github.com/user-attachments/assets/ae9a82d8-f1c0-4c29-9777-665bd8ee1d24" />
🧩 1. What Is a FinFET?

Full Form: Fin Field-Effect Transistor
Structure:

The FinFET replaces the flat (planar) MOSFET channel with a thin, vertical silicon fin that rises above the substrate.

The gate wraps around the fin on three sides — top and both sidewalls — instead of lying only on top as in planar MOSFETs.

The fin acts as the channel.

The 3-D gate provides better electrostatic control of the channel charge.

⚙️ 2. Why FinFET Replaced Planar MOSFETs

As technology scaled below ~22 nm, planar MOSFETs suffered from:

Poor electrostatic control — the gate could not control the entire channel.

High leakage current — electrons flowed even when OFF.

Short-channel effects (SCEs): DIBL, threshold roll-off.

Unreliable switching — loss of gate authority at small nodes.

➡️ FinFETs were introduced (Intel 22 nm Tri-Gate, 2011) to overcome these issues by wrapping the gate around the fin and improving channel control.

🔹 3. Key Advantages of FinFETs
Feature	Description
Better electrostatic control	Gate surrounds fin → stronger field control over channel.
Faster ON/OFF transition	Improved subthreshold slope → sharp switching.
Reduced leakage power	Lower subthreshold and gate leakage.
Stable threshold voltage	Maintained V<sub>th</sub> even at 7 nm, 5 nm, 2 nm.
Temperature stability	Fin structure dissipates heat efficiently.
Scalability	Works well below 10 nm where planar FETs fail.
🔹 4. Why FinFETs Are Prominently Used

Planar MOSFETs cannot scale switching behavior properly; gate loses control.

FinFETs provide:

Strong gate control (3-side wrapping).

Reliable switching across shrinking geometries.

Low leakage & stable threshold → high-density, low-power logic.

FinFETs dominate 7 nm, 5 nm, 3 nm, and 2 nm nodes across foundries (TSMC, Intel, Samsung).

🔹 5. Temperature Stability & Energy Efficiency

Fin geometry provides better heat conduction to substrate.

Leakage increases slowly with temperature → predictable operation.

Stable thermal behavior maintains reference voltage and threshold, improving energy efficiency.

⚙️ Device-Physics Advantages
6️⃣ Better Subthreshold Slope (SS)

Definition:
SS = (dV<sub>G</sub>)/(d(log I<sub>D</sub>)) = (kT/q) ln(10)(1 + C<sub>dep</sub>/C<sub>ox</sub>)

Ideal SS = 60 mV/dec (at 300 K).

Smaller SS = faster ON/OFF transition.

Why FinFET Has Better SS:

In planar MOSFETs, gate controls only the top surface → weak coupling (η ≈ 0.7–0.8).

In FinFETs, the gate wraps around the channel → almost full control (η ≈ 1).

Thin fin → small C<sub>dep</sub>, large C<sub>ox</sub>.
➡️ Subthreshold slope approaches 60 mV/dec → sharper switching, lower leakage.

7️⃣ Less DIBL (Drain-Induced Barrier Lowering)

In short channels, high drain voltage lowers the source barrier → current leaks when OFF.

FinFET’s gate surrounds and shields the channel from the drain’s electric field.

The barrier near the source remains stable, keeping I<sub>off</sub> low.
➡️ Lower DIBL (10–30 mV/V vs 50–100 mV/V in planar).

8️⃣ Reduced Leakage Current (I<sub>off</sub>)

Leakage Sources:
Subthreshold leakage | Gate tunneling | Junction leakage
FinFET Mitigation:

Subthreshold: stronger gate coupling fully depletes channel → very low I<sub>off</sub>.

Gate tunneling: high-k/metal gate stack allows thicker oxide → less tunneling.

Junction: narrow fin → smaller junction area → lower leakage.

9️⃣ Gate–Channel Coupling Explained

I<sub>D</sub> ∝ e<sup>(qψ<sub>s</sub>/kT)</sup>, where ψ<sub>s</sub> = ηV<sub>G</sub>.
FinFETs have η ≈ 1 → small ΔV<sub>G</sub> produces large Δψ<sub>s</sub> → exponential I<sub>D</sub> rise.
Result = rapid current increase, faster switching, near-ideal SS.

🔹 10. Comparison Summary
Property	Planar MOSFET	FinFET	Physical Reason
Gate control	Top only	3 sides (top + 2 sides)	Stronger electric-field coupling
Subthreshold slope	90–100 mV/dec	60–70 mV/dec	Gate fully controls channel (η≈1)
DIBL	High (>50 mV/V)	Low (<30 mV/V)	Drain field shielded by gate
Leakage	High	Very low	Full depletion & thicker oxide
Threshold stability	Poor	Excellent	Minimal short-channel effects
Temperature stability	Weak	Strong	Better heat path through fin
Scalability	< 20 nm limit	2 nm and below	Superior electrostatics
✅ Final Summary
Aspect	Key Point
What	Fin-shaped 3-D FET with gate wrapping around channel.
Why introduced	Planar MOSFETs lost gate control and leaked below 22 nm.
Core advantages	Better SS, less DIBL, lower leakage, stable V<sub>th</sub>, scalable below 10 nm.
Physical reason	Multi-gate structure enhances gate–channel coupling (η ≈ 1).
Outcome	Faster switching, low power, high performance, reliable operation at 7 nm / 5 nm / 2 nm.
Simulation Code (Ngspice)
**** begin user architecture code
.tran 0.1p 100p
.control
    run
    set xbrushwidth=3
    plot nfet_out nfet_in
.endc
**** end user architecture code
**.ends
.GLOBAL GND
...
(end of BSIMCMG model listing)

How Many Fins Does a FinFET Have?

A FinFET can have one or more fins depending on the desired drive current and device width.

Basic Concept
Each fin acts as a channel controlled by the gate.
Effective channel width:
W<sub>eff</sub> = N<sub>fin</sub> × (2 H<sub>fin</sub> + T<sub>fin</sub>)

Typical Numbers

1 fin → low-power/test devices

2–4 fins → standard cells (14 nm / 7 nm)

Up to 8+ fins → high-drive transistors

Why Multiple Fins?
More fins = higher I<sub>on</sub>, like increasing W in planar FETs.
Trade-off = higher capacitance and area.

✅ FinFETs typically use 1–8 fins depending on drive requirements.

Industry Standard Fin Count
Technology Node	Logic Devices	High-Drive Devices	Notes
22 / 16 nm	1–3 fins	4–6 fins	Early FinFET generations (Intel 22FF, TSMC 16FF).
10 / 7 nm	1–4 fins	6–8 fins	TSMC N7 / Intel 10 use 2–3 fins for standard cells.
5 / 3 nm	1–3 fins	4–6 fins	Fins grew taller → fewer needed.
2 nm and below	—	—	Fins replaced by stacked nanosheets (2–4 sheets).

Rule of thumb:

Low-power cells → 1 fin

Standard logic → 2–3 fins

High-drive I/O → 4–8 fins

Example ( TSMC N7 ):
INV_X1 → 1 fin; INV_X2 → 2 fins; INV_X4 → 4 fins.

✅ Industry standard = 2–3 fins for logic at 7–5 nm.

Does Varying Width Equal Varying Fin Count?
Concept	Planar MOSFET	FinFET
Width	Continuous	Quantized (1, 2, 3… fins)
Control	Mask layout	Number of fins under gate
Drive scaling	∝ W	∝ N<sub>fin</sub>
Layout impact	Longer gate	Wider footprint with same L

✅ In FinFETs, varying width = varying fin count.
Each fin adds a discrete unit of effective width and drive current.

Example:

INV_X1 → 1 fin

INV_X2 → 2 fins (≈ 2× drive)

INV_X4 → 4 fins (≈ 4× drive)

Tuning Fin Count

For larger switching threshold → increase number of fins / width.

For smaller threshold → decrease number of fins / width.

Keep length constant; vary fin count to observe parametric changes.

As V<sub>G</sub> increases, the channel becomes more conductive → more current flows.

What Is Transient Analysis?

Transient analysis studies how voltages/currents change with time when a circuit is excited by time-varying inputs.

⚡ 1. Definition

Time-domain simulation showing dynamic behavior before steady-state.

🧮 2. Purpose

Used to observe charging/discharging of capacitors, switching behavior, delays, and oscillations.

📘 3. SPICE Example
.tran 0.1n 100n


(0.1 ns time step, 100 ns total duration)

🧠 4. What It Shows

Inverters: input pulse vs output delay, rise/fall.

RC/RLC circuits: charging, discharging, oscillations.

🧩 5. Comparison with Other Analyses
Type	Domain	Purpose
DC	Static	Steady-state voltages and currents
AC	Frequency	Small-signal response vs frequency
Transient	Time	Large-signal response vs time

✅ In short: Transient analysis reveals how a circuit responds to time-varying inputs — essential for measuring delays, dynamic behavior, and switching speed.

Comparison: DC, AC, and Transient Analyses
Feature	DC Analysis	AC Analysis	Transient Analysis
Domain	Steady-state	Frequency	Time
Input	Constant	Small sinusoid	Time-varying
Output	DC values	Gain/Phase vs freq	Waveforms vs time
Use Case	Biasing	Amplifier response	Switching & delay
Equations	Nonlinear static	Linearized	Time-dependent nonlinear

✅ Summary:

DC → Static

AC → Frequency

Transient → Dynamic

NGSPICE vs LTspice
Category	NGSPICE	LTspice
Developer	Open-source (Berkeley SPICE 3f5)	Analog Devices (formerly Linear Technology)
License	GPL (open-source)	Freeware (proprietary)
Platform	Linux / Windows / macOS	Windows (native), macOS, Linux (via Wine)
Interface	Text / CLI (+ KiCad GUI)	Full graphical schematic + viewer
Ease of Use	Manual netlist editing	Drag-and-drop components
Plotting	External tools (Gnuplot)	Built-in waveform viewer
Simulation Speed	Moderate	Fast (optimized engine)
Behavioral Modeling	Supports Verilog-A (partially)	Limited Verilog-A
BSIM-CMG / FinFET Models	Fully supported (open)	Limited support
Best For	Education, research, FinFET modeling	Analog/power IC design, quick prototyping

✅ Summary:

NGSPICE → Open-source, research-focused, flexible for FinFET and device modeling.

LTspice → Closed-source, fast and user-friendly for analog design and prototyping.



LAB SIMULATIONS -----INVERTER CHARACTERIZATION

<img width="533" height="532" alt="image" src="https://github.com/user-attachments/assets/86fa15ac-537e-45a5-9a70-dac79d8367bf" />
Transfer Charateristics
<img width="538" height="289" alt="image" src="https://github.com/user-attachments/assets/d5a97efd-109b-409e-b9fb-ffe929fcb145" /> 
Drain Current
<img width="503" height="332" alt="image" src="https://github.com/user-attachments/assets/9461651a-2f4d-4c50-b0ed-5d80a97c14ee" />
Drain Current Investigation
<img width="714" height="696" alt="image" src="https://github.com/user-attachments/assets/40684aee-d7dd-4fd0-9061-bf7f966d6b5f" />
Output Resistance
<img width="311" height="284" alt="image" src="https://github.com/user-attachments/assets/26991a53-61d4-4156-ba39-b662f1ceba82" />
Switching Voltage 
<img width="415" height="211" alt="image" src="https://github.com/user-attachments/assets/735f5223-e7b3-41e5-8910-70974f7f9100" />
Switching Voltage investigation
<img width="542" height="208" alt="image" src="https://github.com/user-attachments/assets/bf76e696-0b66-4a7c-954f-fa47f04bc9a7" />












