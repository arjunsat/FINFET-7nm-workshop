FinFET Scaling, Fabrication, and Future Device Integration
   FinFET Circuit Design & Technology Workshop

This repository documents my complete work and technical notes from the FinFET Circuit Design & Characterization Workshop, focusing on device physics, fabrication evolution, and next-generation transistor innovations. The goal was to understand how FinFET and nanosheet technologies enable scaling to the 7 nm node and beyond using ASAP7 PDK, Xschem, and Ngspice.

⚙️ Overview
<img width="940" height="506" alt="image" src="https://github.com/user-attachments/assets/52c67bf2-6496-461d-8ef6-156a84d7ca7b" />

<img width="940" height="512" alt="image" src="https://github.com/user-attachments/assets/8c3275fc-419d-41ee-8549-91debc04c10c" />
The next generation problems needs enormous computing
<img width="940" height="514" alt="image" src="https://github.com/user-attachments/assets/72a93fdd-e2bc-4e99-8dfc-b1192ed1430b" />
If you observe the graphs we can see that the moores law is still true.
But the performance of the chips are saturating(see the frequency graph)
why?
primarily because we are not ableto cool the systems down in a very efficient manner.
After the release of iphone, a lot of technology was directed the direction of mobile applications.   These devices does not have a very well designed cooling systems. So the power dissipation is less.Hence the frequency is also saturated in the curve. 
<img width="940" height="518" alt="image" src="https://github.com/user-attachments/assets/c0e09e6a-35bc-4be0-9466-a689084a91d8" />

<img width="940" height="518" alt="image" src="https://github.com/user-attachments/assets/7b489d85-c5bf-41e3-a01b-274da616c820" />

<img width="940" height="508" alt="image" src="https://github.com/user-attachments/assets/f728dea2-f658-457f-b00b-f826ba72aa8f" />

How to keep moores law going?
<img width="940" height="464" alt="image" src="https://github.com/user-attachments/assets/e111dc08-894d-4565-80d8-c83523777ed7" />

1)Patterning
EUV-13.5 nanometer wave
2) Channel Material
silicon will not help us scale dowm gatelenth less than 10 nm
3)Interconnect material
    damsence process
4)Gate stack material
5)Device structure
 we started from planara devices
But it could nt give us steep enough on to off switching
Finfet – gave us better short channel effects so better on to of switching
today – gate all around and nano sheet

<img width="940" height="723" alt="image" src="https://github.com/user-attachments/assets/97ec3891-a661-4d82-9d72-52b3bd84cdf2" />

FINFETS
<img width="940" height="549" alt="image" src="https://github.com/user-attachments/assets/73f257e9-328a-45e1-a30a-0d0ba49c4fa0" />

<img width="940" height="470" alt="image" src="https://github.com/user-attachments/assets/a0d504f6-50df-44be-8061-87d581f991b4" />

<img width="940" height="470" alt="image" src="https://github.com/user-attachments/assets/625f9491-2a89-4174-b32a-ebea8f207d31" />
Digfference between a planr transistor and a finfet
the active channel PROTRUDES up from the SUBSTRATE.	------it liiks like a fin

The gate will straddle around that fin.
Since  the PROTRUDED 
MORE DERIVE CURRENT THAN -----how because of the vertical nature of the non planar devices. You can decouple the electrical width which is the peripheri of the fin in finfet or the nanosheet in gate all around   from the device or substrate
<img width="940" height="521" alt="image" src="https://github.com/user-attachments/assets/7136fa3e-e911-4558-93b6-68017932b5b7" />
<img width="795" height="709" alt="image" src="https://github.com/user-attachments/assets/9ec25907-6a07-45d1-add3-5ebf49576624" />
The gate can control the channel formed on the  top , between S & D .

But in this form structure ther is chance of  sub channel leakage.
where
<img width="795" height="709" alt="image" src="https://github.com/user-attachments/assets/abfe8138-5cf7-4c8d-b916-974be50929e1" />
<img width="795" height="709" alt="image" src="https://github.com/user-attachments/assets/0dc6feda-0197-44f5-964d-ec308121225e" />

In this region the gate cannot have much control .

How to solve this problem?

By doping this region.
However as the S and D cones closer and closer we need to increase the counter doping correspondingly.

And this increase in doping will lead to another problem --- Band to Band tunneling

because you have highly doped substrate and highly doped drain. So Band to Band tunneling occurs
Band to Band tunneling- leakage between drain and substrate----because of hih doping in drain  and substrate

to prevent this
<img width="841" height="698" alt="image" src="https://github.com/user-attachments/assets/4ec51bb8-fc9b-4926-9e04-6391ae6d9fef" />


<img width="940" height="763" alt="image" src="https://github.com/user-attachments/assets/cc730524-7f9d-479c-beff-0b9cf39bf67e" />
Perfect — that image shows a Double-Gate MOSFET (DG-MOSFET) cross-section.
Let’s explain everything happening here clearly and physically 👇
________________________________________
⚙️ Structure Overview
	S → Source
	D → Drain
	G → Two gates (top and bottom) controlling the same undoped silicon channel
This is a symmetrical double-gate device, meaning both gates can control the channel potential simultaneously.
________________________________________
⚡ What “Two Gates Enhance Gate Capacitance” Means
The gate capacitance (Cox) determines how effectively the gate voltage controls the channel.
In a single-gate MOSFET, the channel is influenced from only one side.
In a double-gate, you have two gates coupling electrostatically with the channel — top and bottom — so:
C_(ox,eff)=C_(ox,top)+C_(ox,bottom)

✅ Result:
The total gate control over the channel charge doubles, improving electrostatic control, transconductance (gm), and drive current (ID).
________________________________________
🧪 “Drain Capacitance Is Reduced Due to Undoped Channel”
In short-channel MOSFETs, drain-to-channel capacitance (Cd) causes unwanted coupling — called Drain-Induced Barrier Lowering (DIBL).
By using an undoped channel, we reduce:
	Depletion regions,
	Junction capacitance (since no abrupt p–n junction),
	Therefore, the drain electric field has less penetration into the channel.
✅ Result:
Less DIBL → better short-channel control, less leakage.
________________________________________
🧩 “Improves Short-Channel Performance”
Short-channel effects (SCE) are major issues when transistors shrink:
	Drain field distorts channel potential,
	Threshold voltage roll-off,
	Subthreshold swing worsens.
But here:
	Two gates control the potential tightly from both sides,
	Drain field is screened by strong gate control,
	Hence SCE are suppressed.
✅ Improved metrics:
	Lower subthreshold swing (S),
	Smaller DIBL,
	Better Ion/Ioff ratio.
________________________________________
📐 Formula — Subthreshold Swing Relation
S∝(1+C_d/C_ox )

Where:
	C_d: depletion capacitance from body/channel
	C_ox: gate oxide capacitance
If C_oxincreases (due to two gates) and C_ddecreases (undoped channel),
→ The ratio C_d/C_oxbecomes very small
→ So S decreases, approaching the ideal 60 mV/dec at room temperature.
________________________________________
⚡ Summary of What’s Happening
Feature	Physical Meaning	Benefit
Two gates	Double electrostatic control	Higher drive current, better gm
Undoped channel	Less depletion, lower Cd	Reduced leakage, better SCE
Increased Cox	Stronger gate control	Steeper subthreshold slope
Reduced Cd	Less DIBL, better channel isolation	Stable Vth and lower S
 



<img width="940" height="508" alt="image" src="https://github.com/user-attachments/assets/669308a9-16c8-427d-95f6-4e362d37543a" />
The rate at which  drive current increases or decreases with respect to applied gate voltage
For 3d devices ie trigate device shows better subthreshold swing compared to planar device .
also FOR THE SAME Vt less LEAKAGE.

<img width="940" height="269" alt="image" src="https://github.com/user-attachments/assets/17fc1e49-80f3-43f8-bb83-3648dd16ea16" />


<img width="940" height="526" alt="image" src="https://github.com/user-attachments/assets/bedda497-1d52-4700-9ecb-c11997233343" />



<img width="592" height="380" alt="image" src="https://github.com/user-attachments/assets/07fe882b-ead4-4d43-a69d-8c7aef05b3c5" />

<img width="940" height="350" alt="image" src="https://github.com/user-attachments/assets/79cf4d70-e304-44b5-9f62-3078a3b7f94b" />

🧩 1. What “High-k” Means
The term k refers to the dielectric constant (relative permittivity, εᵣ) of a material — how well it stores electric charge in an electric field.
	Silicon dioxide (SiO₂) → k ≈ 3.9
	High-k materials → k ≫ 3.9 (typically 10–25 or more)
Common examples:
Material	Dielectric Constant (k)
SiO₂	3.9
Si₃N₄	7
Al₂O₃	9
HfO₂	20–25
ZrO₂	22–25
TiO₂	40–80 (less stable for CMOS)
________________________________________
⚙️ 2. Why High-k Materials Are Used
As transistors scaled down, the gate oxide thickness (Tₒₓ) needed to decrease to maintain strong electrostatic control.
However:
	Thinner SiO₂ → huge leakage current due to quantum tunneling.
	This causes power waste and device heating.
So, instead of using thinner SiO₂, engineers replaced it with a thicker layer of high-k material that gives the same capacitance but less leakage.
________________________________________
⚡ 3. Gate Capacitance Relation
C_ox=(ε_0 ε_r)/t_ox 

To get the same Cox, we can use:
	High εᵣ (dielectric constant)
	Larger tₒₓ
That’s the key idea:
High-k dielectric = thick physical oxide with thin electrical equivalent (EOT).
________________________________________
Equivalent Oxide Thickness (EOT)
EOT=t_(high-k)×3.9/k_(high-k) 

So for HfO₂ (k≈20), a 2 nm layer gives:
EOT=2×3.9/20=0.39" nm (effective like ultra-thin SiO₂!)"

✅ Thus:
	Same gate control,
	Far less tunneling leakage.
________________________________________
🧠 4. Benefits
Parameter	With SiO₂	With High-k
Leakage current	Very high (thin oxide)	Much lower
Gate capacitance	Decreases as Tox ↓	Maintained high
Drive current	Limited	Increases (better control)
Reliability	Poor (tunneling)	Improved
Scaling	Limited below ~1.2 nm	Enabled < 1 nm EOT nodes
________________________________________
⚡ 5. Challenges
High-k materials are not perfect — they introduce new problems:
	Interface traps: poor bonding with Si → degraded mobility.
	Fixed charges: shift threshold voltage (Vth).
	Thermal stability: high-k materials can crystallize at high temps.
	Need for metal gates: polysilicon + high-k causes Fermi-level pinning → metal gate replaces poly-Si.
Hence the modern High-k / Metal Gate (HKMG) stack.
________________________________________
🧱 6. Final Structure (Modern CMOS Stack)
Metal Gate (TiN / TaN / W)
──────────────────────────
High-k Dielectric (HfO₂ / ZrO₂)
──────────────────────────
Silicon Channel
________________________________________
🧭 Summary
Aspect	Explanation
Definition	Material with dielectric constant > 3.9
Purpose	Reduce gate leakage while maintaining capacitance
Mechanism	Use thicker oxide but same Cₒₓ via high εᵣ
Benefit	Higher drive current, lower leakage, continued scaling
Example	HfO₂, ZrO₂, Al₂O₃
Common stack	High-k + Metal Gate (HKMG)

<img width="617" height="345" alt="image" src="https://github.com/user-attachments/assets/28d88416-918f-487e-9da0-e57ffdf3d3d6" />

<img width="940" height="518" alt="image" src="https://github.com/user-attachments/assets/9362badd-1e29-41b5-83bf-f15b10494f06" />
Why siGe instead of si in 5nm?

Standard Cell Area Scaling And Variability

<img width="940" height="488" alt="image" src="https://github.com/user-attachments/assets/5f5c6427-84ee-4945-bc49-51021e043a1c" />
Fin depopulation
reduces capacitive load on inputs
number of fins reducing and thereby cell height is reduced

<img width="940" height="525" alt="image" src="https://github.com/user-attachments/assets/dc4a5420-769e-4c4e-9751-8a26c54d4b1f" />
diffusion break--- REDUCES THE CROSS TALK BETWEEN TRANSISTORS


<img width="623" height="583" alt="image" src="https://github.com/user-attachments/assets/34a9ffc4-5a67-4920-9759-e378027c2aea" />

<img width="822" height="650" alt="image" src="https://github.com/user-attachments/assets/bc409102-a103-4e5f-a3d4-3950a8b08776" />

Putting power rails within the substrate

<img width="940" height="850" alt="image" src="https://github.com/user-attachments/assets/55731920-6a8d-450f-808f-69bef51397bb" />
the FIN DEPOPULATION
has again started t0 increase  Vt

<img width="899" height="516" alt="image" src="https://github.com/user-attachments/assets/352e32c3-d940-4dcf-ba18-beb7436730bd" />

<img width="940" height="495" alt="image" src="https://github.com/user-attachments/assets/bce86b5f-f5a9-4c4b-97c9-a650d3b18cc2" />
we used planar for a long time
first finfet -2011


<img width="940" height="510" alt="image" src="https://github.com/user-attachments/assets/e5b3af45-0a51-4c4c-8c6b-6d2d5894c6db" />

<img width="940" height="464" alt="image" src="https://github.com/user-attachments/assets/a05b340e-773d-4a91-9f8c-6d0f5dbe6a84" />

<img width="940" height="560" alt="image" src="https://github.com/user-attachments/assets/28d317a2-24fa-4ff1-92d8-1dc69dcd0997" />
how the drive current increases

Excellent question — let’s go step by step so you can physically understand how the drive current increases when we “decouple electrical width from device area.”
________________________________________
⚡ 1. Drive Current in a MOSFET (Basic Equation)
In the saturation region, the drain current of a MOSFET is roughly:
I_Dsat=1/2 μC_ox  W/L(V_GS-V_th )^2

Where:
	μ: carrier mobility
	C_ox: oxide capacitance per unit area
	W: channel width
	L: channel length
	V_GS-V_th: effective gate overdrive voltage
So → ID ∝ W, i.e., a wider channel = more current.
________________________________________
🧱 2. In Planar MOSFETs — Width = Physical Width
If you double the gate width (say from 1 µm to 2 µm), you physically make the device twice as wide.
→ This doubles the current, but also doubles the layout area and capacitance.
________________________________________
🏗️ 3. In FinFETs — Vertical Stacking Adds Width Without Area Growth
In a FinFET, current flows along the sides and top of a raised fin.
Each fin contributes an effective electrical width:
W_eff=2H_fin+W_fin

If you add more fins, total effective width becomes:
W_(eff,total)=N_fin (2H_fin+W_fin)

✅ But note:
Fins are spaced tightly in the vertical direction, so adding fins doesn’t increase lateral area linearly like planar MOSFETs.
→ You get more total channel per unit footprint.
Thus, ID increases (∝ W_eff) without large area penalty.
________________________________________
🧬 4. In Nanosheet / Forksheet FETs — Vertical Sheets Multiply Conduction Paths
In nanosheet or forksheet FETs, the current flows around multiple stacked horizontal channels, fully surrounded by the gate (GAA).
If you have N sheets, each with width W_sheet:
W_(eff,total)=N×W_sheet

→ Drive current increases proportionally to the number of sheets, even though the footprint area barely changes.
That’s how the electrical width (and hence drive current) increases — you’ve added more conduction surfaces (more channels) per unit footprint.
________________________________________
🔍 5. Physical Intuition
Think of it like adding more lanes to a highway stacked vertically — each lane carries current, but you’re not widening the road; you’re stacking them up.
→ More carriers flow in parallel → higher drive current.
→ But same footprint area → higher current density.
________________________________________
⚡ Summary Table
Device Type	Current Path	How ID Increases	Area Impact
Planar MOSFET	1 channel on surface	Increase W (lateral)	Large
FinFET	Current on fin sidewalls + top	Add more fins (vertical width)	Small
Nanosheet / Forksheet	Fully-gated stacked sheets	Add more sheets (stacked vertically)	Very small
________________________________________
So, when you decouple electrical width from device area, you’re increasing the number of active conduction channels per footprint — that’s why drive current increases while maintaining compact chip area.
Would you like me to show this concept visually (with a comparison diagram of current paths in planar vs FinFET vs nanosheet)?



CONSTANT ELECTRIC FIELD SCALING—voltage scalingAs semiconductor technology advances, traditional planar transistors face severe limits in electrostatics, leakage, and scaling efficiency. FinFETs and Gate-All-Around (GAA) structures solve these by improving gate control, suppressing short-channel effects, and enabling continued Moore’s Law progression.

This workshop explored:

The evolution from planar to 3D FinFETs and nanosheets.

Device-level characterization (Id–Vd, Id–Vg, gm, ro).

Advanced materials and fabrication innovations (High-k, Metal Gate, SiGe channels, BEOL).

Emerging 3D integration and Backside Power Delivery Networks (BS-PDN) for sub-3 nm nodes.

🧩 Key Topics Covered
1. Evolution of Scaling & Need for FinFETs

Performance saturation due to thermal and frequency limits.

Shift from planar to 3D structures for improved electrostatic control.

Transition path: Planar → FinFET → GAA → Nanosheet/Forksheet FETs.

2. FinFET Structure & Operation

Channel protrudes above substrate forming a “fin”, wrapped by the gate on three sides.

Enables stronger gate control and reduced leakage compared to planar MOSFETs.

Multiple fins provide higher effective width → higher drive current without increasing footprint.

3. Electrostatic Improvements

Double-gate and tri-gate geometries enhance gate capacitance and suppress DIBL.

Undoped channels lower drain capacitance and improve subthreshold swing (approaching 60 mV/dec).

4. High-k / Metal Gate Stack (HKMG)

Replaces thin SiO₂ to reduce gate leakage while maintaining high capacitance.

Common materials: HfO₂ (k≈20), ZrO₂, Al₂O₃ with TiN or W metal gates.

Benefits: lower tunneling current, improved drive current, and continued EOT scaling.

5. Channel & Material Innovations

SiGe and other high-mobility materials used for < 5 nm nodes.

Fin depopulation and diffusion breaks reduce parasitic capacitance and crosstalk.

Incorporation of buried power rails and backside power delivery to optimize cell height and routing.

⚡ Device Concepts and Phenomena
Constant-Field Scaling

Voltage scaling accompanies geometry reduction to maintain electric field consistency.

Drive Current Enhancement

FinFETs decouple electrical width from area — stacking fins/sheets increases conduction paths.

Planar: current ∝ lateral width

FinFET: current ∝ fin height × number of fins

Nanosheet: current ∝ total sheet perimeter (fully gated channels)

Short-Channel Effects Mitigation

Multi-gate control → reduced DIBL and subthreshold leakage.

High-k dielectrics enhance Cox without excessive leakage.

🧠 Body Biasing and Threshold Modulation

Planar CMOS allows body biasing to tune threshold voltage dynamically.

In FinFETs and GAA structures, body bias coupling is weak due to fin isolation.

Solution: Introduce an auxiliary “bias gate” (dual-gate structure).

Thin oxide + metal bias electrode modulates channel potential.

Enables Vth control of ~100 mV/V without doping changes.

🧱 Monolithic 3D Integration (M3D)

Builds multiple active transistor layers sequentially on one wafer with nanometer-scale inter-layer vias (MIVs).

Increases density and reduces interconnect delay and energy.

Enables heterogeneous integration (e.g., Si logic + MoS₂ logic).

Uses low-temperature processes (≤ 400 °C) to preserve bottom-tier transistors.

🔩 BEOL and Interconnect Innovations
Interconnect Evolution
Era	Metal	Process	Feature Pitch	Key Focus
7–5 nm	Cu	Dual/Single Damascene	36–28 nm	Extend Cu reliability
3 nm	Cu	Optimized Damascene	20–24 nm	Reduce barrier thickness
2 nm	Ru/Co	Subtractive Etch	< 20 nm	Eliminate diffusion barriers
1 nm – 0.7 nm	Ru/Mo	Post-Damascene	~10 nm	Barrier-less metals
Key Challenges

RC delay from high resistivity and capacitance.

Electromigration (EM) reliability at small pitch.

Barrier and liner thickness reduce conductive area — pushing shift to Ru/Mo.

Backside Power Delivery (BS-PDN)

Moves VDD/VSS rails to wafer backside → frees front-side routing tracks.

Reduces standard-cell height (6 T → 5 T) → ~15–20 % area reduction.

Improves power integrity and IR drop performance.

⚙️ FEOL–MOL–BEOL Integration
Stage	Description	Key Materials	Purpose
FEOL	Transistor fabrication	Si, SiO₂, HfO₂, metal gate	Device formation
MOL	Contacts + local interconnect	W, Co, Ru	Bridge device to BEOL
BEOL	Global metal wiring	Cu, Ru, low-k dielectric	Signal routing
Resistance Components

R_FEOL: Source/drain and channel resistance

R_MOL: Contact and local interconnect resistance

R_BEOL: Metal/via network resistance

Reducing contact resistivity (via better silicides and dopants) is critical for performance at sub-10 nm nodes.

⚗️ Doping & Annealing

Ion implantation and thermal diffusion introduce dopants.

Rapid Thermal Annealing (RTA) and Flash/Laser Annealing activate dopants without excessive diffusion.

Annealing “turns on” dopants — restores crystal order and activates carriers.

Excessive annealing → junction broadening and leakage.

🧮 Parasitics and Scaling Limits
Resistance

Contact and interconnect resistance dominate at nanoscale — material engineering (Co/Ru/Ti-based contacts) helps reduce Rc.

Capacitance

Intrinsic Cox decreases with scaling; parasitic capacitance rises.

Low-k or air-gap dielectrics improve delay by lowering total capacitance.

🌌 2D Materials and Future Devices

MoS₂, WS₂, graphene — atomically thin, no dangling bonds, ideal for ultra-scaled channels.

High effective mass → reduces direct source-to-drain tunneling.

Excellent electrostatic control and high mobility even at short gate lengths.

Enable sub-5 nm scaling and low-VDD operation.

Quantum & Thermal Effects

Direct Source-to-Drain Tunneling: dominant leakage below 10 nm.

Thermionic Emission: carriers gain energy to overcome potential barriers.

2D materials mitigate both through larger bandgaps and stronger confinement.

📊 Summary
Topic	Insight
Scaling	Moving from planar → FinFET → GAA → 2D FETs to sustain Moore’s Law
Materials	Transition to high-k dielectrics, metal gates, SiGe, Ru, Co
Architecture	Adoption of 3D stacking and backside power networks
Challenges	Parasitics, contact resistivity, thermal budgets
Future	Monolithic 3D & 2D layered materials for atomic-scale devices
🙌 Credits

Workshop Mentors:

Kunal Ghosh — Co-Founder, VSD Corp Pvt Ltd | Ex-Qualcomm, Cadence | M.Tech, IIT Bombay

Soundarya Madhuri Royyuru — VSD Analog Design Team

Organized by:
VLSI System Design (VSD) Corp Pvt Ltd
