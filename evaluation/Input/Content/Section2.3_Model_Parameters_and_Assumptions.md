### 2.3.1 Absorption

Propofol is only administered intravenously.

### 2.3.2 Distribution

Takizawa et al. ([Takizawa 2005](#5-references)) published a fu in humans to be 0.024. Mazoit et al. [Mazoit 1999](#5-references) reported that propofol binds to almost exclusively to serum albumin as plasma protein, which is built-in as such in the PBPK model.

After testing the available organ-plasma partition coefficient and cell permeability calculation methods built in PK-Sim, observed clinical data was best described by choosing the partition coefficient calculation and cell permeability calculation by PK-Sim standard. Specific organ permeability normalized to surface area was automatically calculated by PK-Sim.

### 2.3.3 Metabolism and Elimination

Propofol undergoes fast biotransformation to different metabolites. *In vitro* studies show that particularly the UGT1A9 ([Court 2005](#5-references)) is involved, followed by CY2B6 ([Oda 2001](#5-references)).([Restrepo 2009](#5-references)) 

Al-Jahdari et al. ([Al-Jahdari 2006](#5-references)) investigated the contribution of the liver and kidneys to propofol metabolism in humans using an *in vitro–in vivo* scale up approach. Human kidney and liver microsomal incubations confirmed the dominant role of UGT metabolism for propofol. Propofol was in particular converted by UGT1A9 and CYP2B6. The apparent arithmetic mean Km values in the liver for the glucuronidation and hydroxylation of propofol by UGT1A9 and CYP2B6 were 0.52 (standard deviation (SD): 0.3) and 0.03 (SD: 0.0) mM, respectively. The corresponding Vmax values (nmol/min/mg protein) were 0.2.40 (SD: 0.2) for UGT1A9, and 1.08 (SD: 0.1) for CYP2B6. 

In the kidney the Km and Vmax values for glucuronidation by UGT1A9 were 1.20 (SD: 0.6) mM, and 7.97 (4.5) (nmol/min/mg protein), respectively. The Km and Vmax for hydroxylation were reported to be negligable.

Although UGT1A9 expression is highest in the kidney, as no measurement results were available for CYP2B6 mediated hydroxylation in the kidney, the reported liver *in vitro* Km and Vmax values for UGT1A9 and CYP2B6 were included in the model. Reported Vmax values were in units nmol/min/mg protein and thus not directly transferable into the PBPK model. Therefore, a joint scaling factor f<sub>activity </sub> on the *in vitro* V<sub>max</sub> values was estimated to match observed *in vivo* data, and keeping the relative relationship between those *in vitro* values (0.89 and 0.53 nmol/min/mg) for UGT1A1 and CYP2B6 fixed according to:

V<sub>max,UGT1A9</sub> = f<sub>activity </sub> *  V<sub>max,in-vitro,UGT1A9</sub>

V<sub>max,CYP2B6</sub> = f<sub>activity</sub> * V<sub>max,in-vitro,CYP2B6</sub>

It is especially important to fix the relative contribution of both enzymes as a ratio to ensure that, when translating to other populations (e.g. children where both enzymes may undergo a different ontogeny pattern, or patients who have differently reduced amounts of UGT1A1 vs CYP2B6) the relative contributions can be adequately scaled. 
Note that the estimated scaling factor f<sub>UGT</sub> will be directly implemented into the final *in vivo* V<sub>max</sub> values (only V<sub>max,UGT1A9</sub> and V<sub>max,CYP2B6</sub> will be reported in [section 3](#3-results-and-discussion))

Finally, as ~0.3% of the dose is excreted in human urine as unchanged parent compound, GFR is introduced in the propofol PBPK model.
