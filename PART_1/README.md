FinFET Scaling, Fabrication, and Future Device Integration
   FinFET Circuit Design & Technology Workshop

This repository documents my complete work and technical notes from the FinFET Circuit Design & Characterization Workshop, focusing on device physics, fabrication evolution, and next-generation transistor innovations. The goal was to understand how FinFET and nanosheet technologies enable scaling to the 7 nm node and beyond using ASAP7 PDK, Xschem, and Ngspice.

⚙️ Overview


<img width="940" height="512" alt="image" src="https://github.com/user-attachments/assets/8c3275fc-419d-41ee-8549-91debc04c10c" />
The next generation problems needs enormous computing
<img width="940" height="514" alt="image" src="https://github.com/user-attachments/assets/72a93fdd-e2bc-4e99-8dfc-b1192ed1430b" />
If you observe the graphs we can see that the moores law is still true.
But the performance of the chips are saturating(see the frequency graph)
why?
primarily because we are not ableto cool the systems down in a very efficient manner.
After the release of iphone, a lot of technology was directed the direction of mobile applications.   These devices does not have a very well designed cooling systems. So the power dissipation is less.Hence the frequency is also saturated in the curve. 
<img width="940" height="518" alt="image" src="https://github.com/user-attachments/assets/c0e09e6a-35bc-4be0-9466-a689084a91d8" />


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



  In semiconductor manufacturing, FEOL and BEOL are the two major stages of integrated circuit (IC) fabrication. Here’s a clear breakdown:
________________________________________
🧩 1. FEOL — Front-End of Line
Definition:
FEOL involves the creation of the transistor structures and all components inside the silicon wafer before any metal interconnects are added.
Key processes include:
	Wafer preparation (cleaning and oxidation)
	Active area formation (isolation using LOCOS or STI)
	Well formation (n-well, p-well implantations)
	Gate stack formation (gate oxide + gate material, often high-κ/metal gate)
	Source/drain implantation
	Spacer formation and annealing
	Silicidation (to reduce contact resistance)
Goal:
To build the active devices — MOSFETs, FinFETs, or GAA transistors — on the wafer surface.
Example:
When you read about “7 nm FinFET process” or “high-κ/metal gate integration,” that’s all FEOL work.
________________________________________
⚙️ 2. BEOL — Back-End of Line
Definition:
BEOL deals with the interconnect fabrication — building metal layers and vias above the transistor layer to connect different devices and circuits.
Key processes include:
	Dielectric deposition (usually low-κ materials)
	Contact and via formation
	Metal deposition (copper or aluminum layers)
	Chemical-mechanical polishing (CMP)
	Passivation layer (final protective coating)
Goal:
To connect millions or billions of transistors into functional logic circuits through multi-level metal routing.
Example:
When you hear “10 metal layers” or “dual-damascene Cu interconnects,” that refers to BEOL.

⚡ 3. MOL — Middle of Line
Definition:
The Middle of Line (MOL) is the intermediate stage that connects the transistors formed in the FEOL to the metal interconnect layers built in the BEOL.
Think of it as the “bridge” between the transistor world and the wiring world.
________________________________________
🧩 Where MOL Fits in the Process
	FEOL: Devices are built — source, drain, and gate are formed.
	MOL: Contacts and local connections are made to link each transistor terminal to the first-level metal.
	BEOL: Global wiring networks are built to connect logic blocks together.
________________________________________
⚙️ Key Steps in MOL
Step	Description	Purpose
Contact formation	Tungsten (W) or Cobalt (Co) plugs are formed over source, drain, and gate terminals	Provides a conductive path from the device terminals upward
Barrier/liner deposition	TiN, TaN, or Ru liners are used	Prevents diffusion and reduces contact resistance
Local interconnects	Short metal lines connecting nearby devices	Reduces BEOL routing congestion
Contact resistance optimization	Using silicides (NiSi, CoSi₂) at junctions	Lowers series resistance between transistor and metal
________________________________________
🧠 Why MOL is Important
	Bridges FEOL–BEOL gap: Enables clean electrical connection between tiny transistors and the larger interconnect network.
	Reduces resistance: Advanced MOL materials like cobalt, ruthenium, and TiN liners reduce parasitic resistance.
	Improves reliability: Prevents electromigration and diffusion of metals into silicon.
	Supports scaling: Essential for modern nodes (<10 nm) where FEOL and BEOL must be co-optimized for contact resistance and parasitic capacitance.
________________________________________
⚙️ Example (FinFET Process)
	After FEOL transistor formation:
→ A contact etch stop layer (CESL) is deposited.
→ Contact holes are opened to reach source/drain regions.
→ Tungsten (W) plugs are filled to form vertical contacts.
→ These contacts connect to local interconnects (M0, M1) — the beginning of BEOL
	Summary:
Region	Description	Key Materials	Function
FEOL	Transistor fabrication	Si, SiO₂, high-κ/metal gate	Device formation
MOL	Contact & local interconnect	W, Co, Ru, TiN	Bridge between device and metal
BEOL	Global metal interconnect	Cu, Al, low-κ	Signal routing

Parasitics Resistance And Capacitance

In planar transistors the width of the CONTACT is equal to the width of the channel. Because of this we can keep the extrinsic resistance low.
 

As we go to the 3d devices like . The width of the channel is decreasing as we increase the stacking nature and PITCH.
 
As we go further into more 3D technologies , because of the nature and design of these devices the EXTRINSIC RESISTANCE is increasing
 

WE NEED TO REDUCE THIS!!! -----for that , a lot of material innovations and processes innovations should come up to reduce these EXTRINSIC RESISTANCE

RESISTANCE

 
Rc – contact resistance it’s a silicide – high resistance

this figure shows the resistive components and conduction paths in a FinFET stack, divided clearly into FEOL, MOL, and BEOL regions. Let’s go through it layer by layer so you can fully understand what each labeled resistance represents.
________________________________________
🧱 Overall Structure
From bottom to top, the image represents the current path from the silicon device region (FEOL) up to the metal interconnects (BEOL) through the MOL contacts.
Each region contributes some resistance (R) to the total path.
________________________________________
⚡ 1. FEOL Region (Device Level)
This is the transistor body and source/drain region.
Symbol	Meaning	Description
R_FEOL	FEOL resistance	The total resistance of the active device region (source/drain + channel). It includes both intrinsic and extrinsic transistor parts.
R_EPI	Epitaxial layer resistance	Resistance due to the epitaxially grown silicon on which the source/drain regions are formed. The epi layer helps with doping control and strain.
R_C	Contact resistance	The resistance between the metal contact and the semiconductor (source/drain). It depends on silicide quality (NiSi, CoSi₂, etc.) and doping level.
📘 In short:
FEOL → Transistor and its junction resistance.
________________________________________
🧩 2. MOL Region (Contact + Local Interconnect)
This section bridges the transistor terminals to the first metal layer.
Symbol	Meaning	Description
R_MOL	MOL total resistance	Combination of vertical and lateral resistances from the contact plugs and local interconnect.
R_TS	Trench silicide resistance	Resistance inside the silicided trench or source/drain extension region. It reflects the quality of the silicide and local doping.
R_CA-TS	Contact-to-trench-silicide resistance	Interface resistance between the contact plug (CA) and the underlying silicided region (TS).
R_CA	Contact area (plug) resistance	Resistance of the metal plug itself (tungsten, cobalt, or ruthenium). This is the vertical path in the MOL stack.
📘 Vertical vs Lateral in MOL:
	Vertical → from transistor contact upward through the plug.
	Lateral → short horizontal interconnects that tie neighboring transistors locally before BEOL.
________________________________________
🧠 3. BEOL Region (Interconnect Stack)
This is where global metal routing happens.
Symbol	Meaning	Description
R_CA-BEOL	Resistance between contact and BEOL layer	Transition resistance where the MOL contact connects to the first BEOL metal layer (M1).
R_BEOL	BEOL total resistance	Resistance of the wiring metals and vias that form the larger interconnect network. It depends on metal type (Cu, Al) and wire geometry.
📘 Note:
“xAA” in the diagram refers to the via/contact array density or area, which affects overall series resistance (smaller area → higher resistance).
________________________________________
🔌 Putting It All Together
Total series resistance (R_total):
R_total=R_FEOL+R_C+R_MOL+R_BEOL

where
R_MOL=R_TS+R_(CA-TS)+R_CA+R_(CA-BEOL)

________________________________________
🧠 Key Insight:
	FEOL dominates when the transistor channel is small or mobility is low.
	MOL becomes critical at sub-10 nm nodes, since contact resistance can be 30–40% of total device resistance.
	BEOL affects signal delay and IR drop in large circuits.
________________________________________
🔍 In summary:
Region	Layers/Paths	Major Resistances	Function
FEOL	Silicon device	R_FEOL, R_EPI, R_C	Device conduction
MOL	Contacts + local interconnect	R_TS, R_CA-TS, R_CA, R_MOL	Device-to-metal bridge
BEOL	Global wiring stack	R_CA-BEOL, R_BEOL	Circuit routing
 

We can observe that, In order to reduce this total resistance , it is evident that we need to reduce the CONTACT resistance.
CONTACT RESISTIVITY
 

We need to add more and more dopants in the source drain regions very close to the   silicide.

the choise of metal to reduce the barrier height ---- from nickel to titanium we were able to reduced the barrier aswell.
we are also looking at new types of metals wit low barriers.

If we can manage all this we can reduce RC upto 
 
SOLID STATE DOPING AND ANNELING TECHNIQUES HAVE IMPROVED 
so we can add more dopants now


1. Solid-State Doping: Overview
Definition:
Doping is the process of intentionally introducing impurities (dopant atoms) into a semiconductor (usually silicon) to modify its electrical properties — i.e., to make it n-type or p-type.
Goal:
Control carrier concentration → tune conductivity, threshold voltage, and junction characteristics.
________________________________________
🧩 2. Solid-State Doping Techniques
There are mainly two classes of doping methods in solid-state semiconductor processing:
________________________________________
A. Thermal Diffusion
This is the oldest and simplest technique — dopants move into silicon via diffusion at high temperature.
🔹 Process Steps:
	Oxidation: A thin oxide layer is grown on the wafer (can act as a mask or source).
	Dopant source introduction: Either solid, liquid, or gas dopant source is used.
	Examples:
	Boron (B₂O₃, BBr₃) for p-type
	Phosphorus (POCl₃) for n-type
	Diffusion in furnace: Wafers are heated in a quartz tube furnace at 900–1100°C.
	Drive-in stage: A second high-temp step drives dopants deeper and activates them.
🔹 Fick’s Laws of Diffusion govern dopant motion:
∂C/∂t=D (∂^2 C)/(∂x^2 )

where C = concentration, D = diffusion coefficient.
🔹 Types of Diffusion:
Type	Description
Constant-source diffusion	Surface concentration stays constant (limited by solubility)
Limited-source diffusion	Total dopant atoms fixed (from thin layer or spin-on source)
________________________________________
B. Ion Implantation
Modern precision doping technique used in advanced CMOS.
🔹 Principle:
Ions of dopant species (e.g., B⁺, As⁺, P⁺) are accelerated in an electric field and bombarded onto the silicon wafer.
🔹 Process Steps:
	Ion generation: Dopant gas (e.g., BF₃, PH₃) is ionized.
	Acceleration: Ions are accelerated to energies from keV to MeV.
	Beam focusing: Magnetic/electrostatic fields steer ions for uniform dose.
	Implantation: Ions penetrate the wafer surface, creating amorphized lattice.
	Annealing (next step) repairs the damage and activates dopants.
🔹 Control Parameters:
Parameter	Effect
Dose (ions/cm²)	Controls dopant quantity
Energy (keV–MeV)	Controls penetration depth
Angle	Reduces channeling effects (ions going deep along crystal planes)
🔹 Advantages:
	Precise control of dose and depth
	Can do selective doping using resist masks
	Low contamination risk
________________________________________
🔥 3. Annealing Techniques
After implantation, silicon’s crystal lattice is damaged, and dopants are electrically inactive.
Annealing repairs this and activates the dopants (puts them on substitutional lattice sites).
________________________________________
A. Furnace Annealing
	Temperature: 900–1100°C
	Time: 30–60 minutes
	Environment: N₂, O₂, or inert gas
	Purpose: Dopant activation and defect repair
	Limitation: Long time → dopant diffusion (loss of sharp junctions)
________________________________________
B. Rapid Thermal Annealing (RTA)
	Temperature: 950–1050°C
	Time: 1–10 seconds
	Method: Infrared lamps heat wafer rapidly, then cool it quickly
	Advantage:
	Activates dopants without allowing diffusion
	Maintains shallow junctions for advanced CMOS nodes
________________________________________
C. Flash Lamp Annealing (FLA) / Laser Annealing
	Temperature: 1200–1350°C (surface only, for a few milliseconds)
	Method: Pulsed laser or xenon flash melts surface layer briefly
	Purpose: Ultra-shallow junctions, minimal diffusion
	Used in: Sub-10 nm FinFET and GAA technologies
________________________________________
🧠 4. Relationship Between Doping and Annealing
Step	Purpose	Example
Doping	Introduce impurity atoms	Ion implant B⁺ at 30 keV
Annealing	Repair damage + activate dopants	RTA at 1000°C for 5 s
If annealing is too short → low activation.
If too long → diffusion broadens junction, increasing leakage.
________________________________________
⚙️ 5. Typical Dopants and Applications
Dopant	Type	Common Use
Boron (B)	p-type	Source/drain, channel doping
Phosphorus (P)	n-type	Source/drain, wells
Arsenic (As)	n-type	Shallow junctions, low diffusivity
Antimony (Sb)	n-type	Contact regions
________________________________________
🧩 6. Summary Diagram
 ┌───────────────────────────────────────────────┐
 │  Doping Introduces Impurities (Diffusion/Implant) │
 │     ↓                                           │
 │  Crystal Damage + Inactive Dopants              │
 │     ↓                                           │
 │  Annealing Restores Lattice + Activates Dopants │
 └───────────────────────────────────────────────┘
________________________________________
Would you like me to add a visual process flow diagram (with energy-depth profiles and before/after annealing effects) to help you visualize how ion implantation and annealing affect dopant profiles?
You said:
will aneling help us include more dopants
🔥 Short answer:
No — annealing doesn’t add more dopants,
but it activates and redistributes the dopants you already introduced, effectively increasing the number of active dopants in the crystal.

🧠 Detailed Explanation
🔹 1. What happens right after doping (especially ion implantation):
When you implant dopants (like B⁺ or P⁺ ions):
	Many dopant atoms don’t sit in proper crystal lattice sites — they occupy interstitial positions or form clusters.
	These atoms are electrically inactive (they can’t donate or accept carriers).
	The silicon lattice is also damaged — lots of broken bonds and disordered regions.
So, the total dopant concentration (C_total) is high,
but the electrically active dopant concentration (C_active) is much lower.
________________________________________
🔹 2. What annealing actually does:
Annealing provides thermal energy that allows:
	Lattice self-healing → Silicon atoms return to proper crystal positions.
	Dopant activation → Implanted atoms move onto substitutional lattice sites, where they can function as donors (n-type) or acceptors (p-type).
	Defect removal → Reduces recombination centers that would trap carriers.
So annealing does not increase dopant count,
but it increases the number of dopants that are active — which raises the effective carrier concentration.
________________________________________
🔹 3. What happens if temperature is too high or time too long:
	Dopants diffuse deeper, broadening junctions (bad for short-channel devices).
	Some atoms can cluster again or precipitate, reducing activation.
	In extreme cases, dopant deactivation or defect regrowth may occur.
That’s why advanced nodes use Rapid Thermal Annealing (RTA) or Flash Annealing — short, intense heat pulses that activate dopants without significant diffusion.
________________________________________
🔹 4. Conceptual Summary:
Stage	Dopant behavior	Comment
Before annealing	High total dose, low activation	Many dopants in interstitial positions
After annealing	Same total dose, high activation	Dopants move to substitutional sites, lattice repaired
Excessive annealing	Possible dopant diffusion or deactivation	Overheating causes junction broadening
________________________________________
✅ Key takeaway:
Annealing doesn’t add more dopants — it “turns them on.”
It converts implanted dopants from inactive atoms to active charge carriers by restoring the silicon crystal structure.



Now lets look at the

 Parasitic capacitance.

As we scale down the transistor features we are also scaling down the gap between the gate and source drain contacts. Because of that the contribution of the intrinsic capacitance which is the Cox of the transistor is going down .   ------DATA MARKED IN BLACK. 
<img width="323" height="509" alt="image" src="https://github.com/user-attachments/assets/0423d216-b473-4a60-97b3-db10ac1e4e47" />


However the contribution of parasitic capacitance is going HIGH -----DATA MARKED IN RED.
<img width="336" height="573" alt="image" src="https://github.com/user-attachments/assets/824f0b2c-73a8-443e-9fc4-d5f0ae5d6c8e" />

 


 <img width="940" height="419" alt="image" src="https://github.com/user-attachments/assets/80a8de66-5da3-4d49-911e-2d83e122c498" />

 How to reduce this parasitic capacitance?
1) To introduce a lower K material in the gap between the gate and the source drain contact.
 <img width="477" height="610" alt="image" src="https://github.com/user-attachments/assets/ffa37344-da38-47fa-b5db-a80965939a0e" />


NOTE   - delay reduces as we do this  because the parasitic capacitance reduces.
 
Which low k material we use?
 
 

The ultimate thing is air spacer instead of anyother low  k material as spacer.  15 percent improvement.

 

Device Scaling And Electrical Characteristics
 
we are looking at layered materials to be able to scale the transistors closer to 5nm gate length ------state of the art transistor today is having 15 nm

What is a main challenge ? to prevents direct source to drain tunnelling. 


This fundamentally prevents the scalingof short transistors.


These 2 d materials are very interesting , that can be implemented with atomic scale precision.

MoS2 --- slightly higher heavier than silicon.

ONE of the EFFECTIVE WAYS to DECREASE SOURCE TO DRAIN TUNNELING IS to INCREASE THE EFFECTIVE MASS of CARRIERS.

In terms of BANDGAP they are higher

 
What is Direct source to drain tunnelling?

Direct Source-to-Drain Tunneling (DSDT) is a quantum mechanical effect that occurs in ultra-scaled MOSFETs, particularly when the channel length becomes extremely short (typically below ~10 nm).
________________________________________
🧠 Concept Overview
In an ideal MOSFET, current flows from source → drain only when a strong inversion channel is formed by applying a gate voltage (V<sub>GS</sub> > V<sub>th</sub>).
However, when the channel becomes very short, the potential barrier between source and drain becomes thin enough that electrons can tunnel directly through it, even without sufficient gate bias.
This is Direct Source-to-Drain Tunneling — a leakage current that bypasses normal channel conduction.
________________________________________
⚙️ Mechanism
	Normally, the gate controls the energy barrier between source and drain.
	In ultra-short channels:
	The barrier width (L<sub>ch</sub>) is comparable to the electron de Broglie wavelength (~5–10 nm).
	Electrons can quantum tunnel through this barrier directly.
	The result is a non-zero drain current (I<sub>D</sub>) even when V<sub>GS</sub> < V<sub>th</sub> (i.e., in subthreshold region).
Mathematically, the tunneling probability T ≈ exp(-α·L<sub>ch</sub>·√Φ<sub>B</sub>),
where Φ<sub>B</sub> is barrier height and α is a material constant.
→ As L<sub>ch</sub> decreases, T increases exponentially, increasing leakage.
________________________________________
⚡ Effects on Device Performance
Parameter	Impact
Off-state current (I<sub>off</sub>)	Increases drastically due to tunneling leakage
Subthreshold slope (SS)	Degrades (cannot reach the ideal 60 mV/dec)
ON/OFF current ratio	Reduces, worsening digital logic behavior
Static power consumption	Increases sharply
Device reliability	Decreases; gate control weakens
________________________________________
🧩 Mitigation Techniques
To reduce DSDT in nanoscale MOSFETs:
	Use high-barrier materials (high effective mass or larger bandgap channels — e.g., SiGe, III-V, 2D materials).
	Increase channel length slightly to restore barrier width.
	Adopt multi-gate structures (FinFET, GAA, Nanosheet FETs) for better electrostatic control.
	Use tunneling FETs (TFETs) intentionally exploiting band-to-band tunneling for low-power operation.
	Employ strain or heterostructures to reshape the potential barrier.
	<img width="940" height="739" alt="image" src="https://github.com/user-attachments/assets/c9828670-9d06-4ced-b880-8f1bbbafff61" />

________________________________________
🧠 In Simple Terms
Direct source-to-drain tunneling means electrons "leak" straight through the transistor’s channel barrier instead of waiting for the gate to open the path — a quantum shortcut that becomes unavoidable when the transistor is extremely small.
Why it’s called Source-to-Drain Tunneling and not Drain to Source?
	In a MOSFET, electrons flow from the source to the drain, so tunneling current is defined in that direction.
	When the channel becomes very short, some electrons in the source tunnel through the thin barrier directly to the drain, even when the gate is off.
	Though tunneling is physically bidirectional, the net flow is from source → drain because the drain is at a higher potential (V<sub>DS</sub> > 0).
	Energy-band diagrams show filled states in the source and empty states in the drain, so electrons move forward.
	Hence, it’s called Direct Source-to-Drain Tunneling, not “Drain-to-Source,” since current direction and operation are defined by electron transport from source to drain.

CHALLENGES OF SCALING to SUB 5nm GATE Lengths

 

 


 
THERMIONIC EMISSION
Thermionic Emission is the process by which electrons escape from a material’s surface (usually a metal or semiconductor) when it is heated to a high temperature.
________________________________________
⚙️ How It Works
	Inside a metal or semiconductor, electrons are bound by a potential barrier known as the work function (Φ) — the minimum energy needed for an electron to escape into vacuum (or across an interface).
	When the material is heated, electrons gain thermal energy (kT).
	If this thermal energy becomes comparable to or greater than Φ, some electrons can “hop over” the barrier and escape from the surface.
→ This flow of electrons due to heat is called thermionic emission.
________________________________________
🧮 Mathematical Expression
The Richardson–Dushman equation describes the emitted current density:
J=AT^2 e^(-Φ/kT)

where:
	J= current density (A/m²)
	A= Richardson constant (~120 A/cm²·K² for metals)
	T= absolute temperature (K)
	Φ= work function (eV)
	k= Boltzmann constant
→ As temperature increases, the exponential term increases rapidly, giving a much higher emission current.
________________________________________
⚡ In MOSFETs and Semiconductors
In semiconductor devices, thermionic emission often occurs:
	Over the source–channel barrier in MOSFETs (especially at high temperatures).
	Across Schottky barriers in metal–semiconductor contacts.
	In vacuum tubes and thermionic converters, where hot cathodes emit electrons toward an anode.
In these cases, electrons gain enough energy to surmount (not tunnel through) the potential barrier.
________________________________________
🔍 Thermionic vs. Tunneling
Feature	Thermionic Emission	Quantum Tunneling
Mechanism	Electrons gain energy to jump over barrier	Electrons penetrate through barrier
Requires heat?	Yes (thermal energy)	No (quantum effect)
Dominant in	High-temperature, long-channel devices	Low-temperature, short-channel devices
Current equation	Richardson–Dushman law	Tunneling probability T∝e^(-αL√Φ)
________________________________________
🧠 In Simple Words
Thermionic emission is like heating a pan until water molecules (electrons) get enough energy to evaporate off the surface — jumping over the barrier and escaping.
The following graph implies that it is interesting to use the 2d materials for short gate length devices.

 
 


 
 
What is an ideal Sub threshold swing?-----nearly 60mV/decade
 
What happens if we build transistors with only 2d materials?
2 D materials are atomically thin and precise.
2D materials have no dangling bonds.
 


VG- VT ----measure of vertical electric field
As the vertical electric field increases mobility goes down.

In 3D devices because of dangling bonds
and Si behaviour the vertical electrical field will be higher, it will be less in 2D materials.

How would all 2 D material made mosfet behave?
 

The impact of mobility not degraded at higher electric field means drive current will be higher.
This will enable further voltage scaling   ---Vdd scaling


SOME PHYSICS

1-------Dangling bonds refer to unsatisfied or incomplete chemical bonds that occur when an atom at the surface or interface of a material does not have enough neighboring atoms to bond with — unlike atoms in the bulk, which are fully coordinated.
________________________________________
🔬 Example (Semiconductors)
In a crystal lattice like silicon (Si):
	Each Si atom ideally bonds with four neighboring Si atoms (tetrahedral structure).
	At the surface or at a defect site, some Si atoms might have only three or fewer bonds.
	The remaining unpaired electron(s) form dangling bonds.
________________________________________
⚡ Effects of Dangling Bonds
	Trap States: They introduce localized energy levels in the bandgap, which can trap charge carriers (electrons/holes).
	Increased Recombination: They act as recombination centers, reducing carrier lifetime.
	Instability: Cause threshold voltage shifts and noise in transistors and sensors.
	Surface Reactivity: Make the surface chemically active — useful in functionalization but harmful in pure electronic devices.
________________________________________
🧪 Common Fix — Passivation
To neutralize dangling bonds, atoms like hydrogen (H) or oxygen (O) are added to "saturate" the unpaired electrons.
Example:
In SiO₂/Si interface, hydrogen passivation removes Si dangling bonds by forming Si–H bonds, improving MOSFET performance.

2------why 2D materials does not have dangling bond?

this gets at one of the core advantages of 2D materials like graphene, MoS₂, WS₂, or h-BN.
________________________________________
⚛️ 1. Structural Reason
2D materials are atomically thin, fully bonded sheets where every atom’s bonding requirements are already satisfied within the plane:
	In graphene, each carbon atom forms three strong sp² bonds with its neighbors, and the fourth valence electron forms a delocalized π bond extending across the entire sheet.
→ No “dangling” valence electrons remain.
	In MoS₂, each Mo atom is sandwiched between two layers of S atoms (S–Mo–S).
→ The top and bottom sulfur atoms complete the bonding — again, no unsatisfied bonds at the surface.
So, even though they are surfaces, the surface itself is the material, and all bonds are internally satisfied.
________________________________________
⚙️ 2. Absence of Surface Dangling Bonds
Unlike 3D materials (like Si), where cutting a crystal leaves “broken” bonds at the surface, 2D materials are naturally terminated layers.
	You don’t “break” bonds when you exfoliate or isolate a monolayer — you just separate weak van der Waals interfaces between adjacent layers.
	These interlayer forces are non-bonding interactions, so no new dangling bonds appear.
________________________________________
⚡ 3. Implications
Because of this:
	Fewer surface traps → higher carrier mobility.
	Better interface quality when stacked or gated.
	No need for passivation like in SiO₂/Si systems.
	Ideal for heterostructures (graphene/h-BN, MoS₂/WSe₂, etc.) since layers can be combined without chemical mismatch.
________________________________________
🧠 In short
2D materials don’t have dangling bonds because their atomic structure is self-terminated and fully covalently satisfied within the plane. The layers are bound by van der Waals forces, not chemical bonds, so isolating them doesn’t “cut” any bonds.

3--------how are they 2D , what about the third dimension even a paper is 3D?

everything we can touch, including a sheet of paper, exists in three dimensions. But when we say a material is “2D”, we’re talking about its atomic-scale structure — not its macroscopic shape.
Let’s break this down clearly 👇
________________________________________
⚛️ 1. What “2D” really means in materials science
A 2D material is only one or a few atoms thick in the third dimension (the z-direction), while it can extend over large distances in the x and y directions.
So:
	It has length (x) and width (y) — two dimensions of freedom.
	But its thickness (z) is so small (≈ 0.3–1 nm) that electrons cannot move freely along it — their motion is quantum confined to essentially two dimensions.
Hence, the physics becomes two-dimensional, even though the object still exists in 3D space.
________________________________________
📘 2. Analogy — Paper vs. Graphene
Property	Sheet of Paper	Graphene Monolayer
Thickness	~0.1 mm (millions of atoms thick)	~0.34 nm (1 atom thick)
Atoms across thickness	Billions of layers	1 layer of carbon atoms
Electronic motion	3D — electrons move in all directions	2D — electrons confined in-plane
Bonding	3D (fibers, molecules)	2D (sp² bonded carbon lattice)
Even though both are “flat,” graphene’s thickness is on the atomic scale, where the third dimension practically vanishes for electrons.
________________________________________
🧪 3. Why the “third dimension” is negligible
	In a 3D solid like Si, electrons have allowed energy bands in all directions (x, y, z).
	In a 2D material, the energy quantization in the z-direction is so strong that only one discrete subband exists — electrons behave as if they live in a flat plane.
→ This gives rise to 2D electron gas (2DEG) physics and unique phenomena (quantum Hall effect, high mobility, etc.)
________________________________________
🧱 4. Real-world definition
“2D” doesn’t mean the material literally lacks the third dimension — it means the material’s electronic, structural, and optical behavior is confined to a plane, making it effectively two-dimensional.

Surface Roughness Scattering
Surface roughness scattering is a type of carrier scattering that occurs when the surface or interface of a semiconductor (or thin film) is not perfectly smooth, causing electrons (or holes) to scatter as they move near that surface.
________________________________________
⚛️ 1. Basic Concept
In nanoscale or 2D materials (like MOSFET channels, quantum wells, or thin films), charge carriers often move very close to an interface — e.g., between silicon and silicon dioxide (Si/SiO₂).
If that interface is rough or uneven on the atomic scale:
	The electric field at the interface fluctuates.
	The potential energy landscape becomes irregular.
	As electrons move, they scatter due to these potential variations.
This process is called surface roughness scattering (SRS).
________________________________________
⚙️ 2. Physical Origin
	Even high-quality interfaces have atomic-scale steps or bumps (~0.1–1 nm height variations).
	In a MOSFET, these variations cause the confinement potential (which confines electrons near the surface) to change locally.
	This alters the electron wavefunction, leading to momentum scattering and mobility degradation.
________________________________________
⚡ 3. Impact on Device Performance
	Reduces carrier mobility (μ):
Especially significant at high vertical electric fields when carriers are pushed closer to the surface.
	Limits current drive (Iₒₙ):
Scattering reduces channel conductivity.
	Affects low-dimensional devices:
In ultrathin films, nanowires, and 2D materials, surface roughness plays a dominant role because almost all carriers are near an interface.
________________________________________
🧮 4. Dependence Factors
Surface roughness scattering increases with:
	Higher surface electric field (strong inversion).
	Larger roughness amplitude (Δ) — height of irregularities.
	Shorter correlation length (Λ) — how rapidly the roughness varies spatially.
Mathematically, the scattering rate τ_SRS^(-1)∝Δ^2 Λ^(-2) E_"eff" ^2,
where E_"eff" is the effective vertical field.
________________________________________
🧠 5. Why It’s Important
	In modern sub-10 nm MOSFETs, SRS is often the dominant mobility-limiting factor.
	It competes with other scattering mechanisms:
	Phonon scattering (lattice vibrations)
	Coulomb scattering (charged impurities)
	Interface trap scattering
________________________________________
🔍 6. In 2D Materials
2D materials (like MoS₂, graphene) are less affected by surface roughness scattering because they are atomically flat and self-passivated — there’s no dangling bond interface like Si/SiO₂. However, substrate roughness (like SiO₂ under graphene) can still introduce potential fluctuations and degrade mobility.





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
