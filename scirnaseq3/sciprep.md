---
title: sci-Preparation
subtitle: Modified sci-RNA-Seq3 protocol for single-cell/nucleus RNA-seq
date: May 15, 2023
Author: Chaichontat Sriworarat
---

<style>
.critical{
  font-weight: bold;
  color: #702963;
}

.caution{
  font-weight: bold;
  color: #bb2222;
}

.pause{
  font-weight: bold;
  color: #228B22;
}

.timing{
  font-weight: bold;
  color: #6495ED;
}

.sequence{
  font-family: monospace;
}

.buffer{
  font-size: 1.1em;
  font-weight: bold;
}
</style>

## Preparation

### Materials and Reagents

| Reagent                                                     | Vendor                                                                        | Notes                                                                                                                                                                   |
| ----------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| DSP                                                         | (Lomant's reagent; Thermo Fisher, cat. no. 22586 or PG82081)                  | <span class="critical">CRITICAL:</span>DSP is sensitive to water and should be used immediately after dissolving in  DMSO                                               |
| Methanol                                                    | (Millipore Sigma, cat. no. 494437-2L)                                         |                                                                                                                                                                         |
| DMSO                                                        | (Millipore Sigma, cat. no. D2438-5X10ML)                                      | <span class="critical">CRITICAL:</span>DMSO is hygroscopic. Always use a new DMSO vial for DSP.                                                                         |
| Sodium phosphate dibasic                                    | (Millipore Sigma, cat. no. S3264-250G)                                        |                                                                                                                                                                         |
| Sodium phosphate monobasic monohydrate                      | (Millipore Sigma, cat. no. 71507-250G)                                        |                                                                                                                                                                         |
| Potassium phosphate monobasic                               | (Millipore Sigma, cat. no. P9791-100G)                                        |                                                                                                                                                                         |
| Sodium chloride                                             | (Millipore Sigma, cat. no. S3014-500G)                                        |                                                                                                                                                                         |
| Potassium chloride                                          | (Millipore Sigma, cat. no. P9541-500G)                                        |                                                                                                                                                                         |
| Magnesium chloride solution, 2 M                            | (Millipore Sigma, cat. no. 68475-100ML-F)                                     |                                                                                                                                                                         |
| IGEPAL CA-630                                               | (Millipore Sigma, cat. no. I8896-50ML)                                        |                                                                                                                                                                         |
| BSA, 20 mg/ml                                               | (New England Biolabs, cat. no. B9000S)                                        |                                                                                                                                                                         |
| DEPC                                                        | (Millipore Sigma, cat. no. D5758-25ML)                                        | <span class="caution">CAUTION:</span> Handle DEPC, and samples containing it, in a fume hood.                                                                           |
| Sucrose                                                     | (VWR, cat. no. 97061-428)                                                     |                                                                                                                                                                         |
| Triton X-100                                                | (Millipore Sigma, cat. no. T8787-100ML)                                       |                                                                                                                                                                         |
| Tween 20                                                    | (Thermo Fisher, cat. no. BP-337-100)                                          |                                                                                                                                                                         |
| 10× Dulbecco’s PBS                                          | (10× DPBS; Thermo Fisher, cat. no. 14200075)                                  |                                                                                                                                                                         |
| Superscript IV reverse transcriptase                        | (Thermo Fisher, cat. no. 18090200)                                            |                                                                                                                                                                         |
| T4 DNA Ligase                                               | (New England Biolabs, cat. no. M0202L)                                        |                                                                                                                                                                         |
| Tagmentase (Tn5 transposase) , unloaded                     | (Diagenode, cat. no. C01070010-20)                                            | <span class="critical">CRITICAL:</span> The amount of tagmentase added to Step 57 has been determined for this brand only.                                              |
| Tn5-N7 oligo                                                | (<span class="sequence">5'-GTCTCGTGGGCTCGGAGATGTGTATAAGAGACAG-3'</span>, IDT) |                                                                                                                                                                         |
| Mosaic End (ME) oligo                                       | (<span class="sequence">5'-/5Phos/CTGTCTCTTATACACATCT-3'</span>, IDT)         |                                                                                                                                                                         |
| NEBNext mRNA second-strand synthesis module                 | (New England Biolabs, cat. no. E6111L)                                        |                                                                                                                                                                         |
| NEBNext high fidelity 2× PCR master mix                     | (New England Biolabs, cat. no. M0541L)                                        |                                                                                                                                                                         |
| dNTP mix                                                    | (New England Biolabs, cat. no. N0447L)                                        |                                                                                                                                                                         |
| Agencourt AMPure XP                                         | (Beckman Coulter, cat. no. A63882)                                            |                                                                                                                                                                         |
| Yoyo dye                                                    | (Thermo Fisher, cat. no. Y3601)                                               |                                                                                                                                                                         |
| RNaseAlert kit                                              | (IDT, cat. no. 11-02-01-02)                                                   |                                                                                                                                                                         |
| RNaseZap                                                    | (Thermo Fisher, cat. no. AM9780)                                              |                                                                                                                                                                         |
| Elution buffer                                              | (EB, 10 mM Tris pH 8.5; Qiagen, cat. no. 19086)                               |                                                                                                                                                                         |
| Protease                                                    | (Qiagen, cat. no. 19157)                                                      | <span class="critical">CRITICAL:</span>  Do not use any other protease/proteinase. This one can be heat-inactivated at the temperature and time listed in the protocol. |
| 6% TBE Novex PAGE gels                                      | (10 wells; Thermo Fisher, cat. no. EC6262BOX)                                 |                                                                                                                                                                         |
| UltraPure agarose                                           | (Thermo Fisher, cat. no. 16500-500)                                           |                                                                                                                                                                         |
| Qubit double-stranded DNA high-sensitivity quantitation kit | (Thermo, cat. no. Q32851)                                                     |                                                                                                                                                                         |
| sci-RNA-seq3 indexed primer plates                          | IDT                                                                           | standard desalting for purification; random bases do not need hand-mixing. **These are modified from sci-RNA-SeqV3**                                                    |

### Equipment

Equipment

- **Chilled** Hammer
- DNA/RNA LoBind tubes (Eppendorf, cat. no. 022431021)
- Refrigerated centrifuges that hold 1.5-ml microcentrifuge tubes, microwell plates and 15- and 50-ml conical tubes
- Chemical fume hood
- Multichannel pipettes and tips
- FloMi filter, 40 μm (VWR, cat. no. 10032-802)
- Falcon cell strainer, 40 μm (VWR, cat. no. 21008-949)
- Pestle for cell strainer (Midsci, cat. no. SG-PEST)
- 96-well plates (Eppendorf, cat. no. 951020401)
- 96-well LoBind plates (Eppendorf, cat. no. 30129512) or FrameStar 96-well skirted PCR plates (Thomas Scientific, cat. no. 1149V59) if LoBind plates are not available
- Thermomixer
- Sonicator (Diagenode Bioruptor Plus)
- Cell counter with GFP channel, or a hemocytometer and an inverted microscope that allows visualization with GFP
- Electrophoresis chambers for PAGE and agarose gels

### Buffers and Solutions

- <span class="buffer">10× PBS-hypotonic stock solution</span><br>
Mix 5.45 g of Na2HPO4 (dibasic), 3.1 g of NaH2PO4·H20, 1.2 g of KH2PO4, 1 g of KCl and 3 g of NaCl in nuclease-free water and bring to a final volume of 500 ml. This stock solution will have a pH of ~6.8, but when diluted to 1×, should end up at pH 7.0–7.4. The buffer can be stored at room temperature (20–23 °C) for 6 months.

- <span class="buffer">Hypotonic lysis buffer solution A</span><br>
This buffer is used for whole mouse embryos E16.5 and older. Mix 5 ml of the 10× PBS-hypotonic stock solution, 5.7 g of sucrose, 75 μl of 2 M MgCl2 and nuclease-free water to a final volume of 50 ml to make the lysis base solution. Right before lysis, for every 1 ml of lysis buffer needed, add 2.5 μl of 10% (vol/vol) IGEPAL (vol/vol) and 10 μl of DEPC and then vortex the solution to disperse the DEPC throughout. For example, if a sample needs 5 ml of lysis buffer, take a 5-ml aliquot of lysis buffer stock solution and add 12.5 μl of 10% (vol/vol) IGEPAL and 50 μl of DEPC. Keep the buffer on ice. Make fresh for each experiment.

<aside>
<span class="caution">CAUTION:</span> DEPC needs to be used in a fume hood. <br>

<span class="critical">CRITICAL:</span>  DEPC has a short half-life in aqueous solutions, so adding it to the buffer just before the cells are added is important.
</aside>

- <span class="buffer">Hypotonic lysis buffer solution B</span><br>
This buffer is used for Tiny-Sci, cell lines, mouse embryos under E16.5 and isolated tissues. Mix 5 ml of the 10× PBS-hypotonic stock solution, 75 μl of 2 M MgCl2 and nuclease-free water to a final volume of 50 ml to make the lysis base solution. Right before lysis, for every 1 ml of lysis buffer needed, add 40 μl of BSA (20 mg/ml), 2.5 μl of 10% (vol/vol) IGEPAL and 10 μl of DEPC and then vortex the solution to disperse the DEPC throughout. For example, if a sample needs 5 ml of lysis buffer, take a 5-ml aliquot of lysis buffer base solution and add 200 μl of BSA, 12.5 μl of 10% (vol/vol) IGEPAL and 50μl of DEPC. Keep the buffer on ice. Make fresh for each experiment.

<aside>
<span class="caution">CAUTION:</span> DEPC needs to be used in a fume hood. <br>

<span class="critical">CRITICAL:</span> DEPC has a short half-life in aqueous solutions, so adding it to the buffer just before the cells are added is important.
</aside>

- <span class="buffer">0.3 M SPBSTM (sucrose PBS TritonX MgCl2)</span><br>
This is the main buffer used throughout the protocol for washing and diluting nuclei. Dissolve 28.5 g of sucrose in 25 ml of 10× DPBS (regular DPBS, not the hypotonic version) and 125 ml of nuclease- free water (about half the volume of water that you will need). Once the sucrose has dissolved, add 2.5 ml of 10% (vol/vol) Triton X-100, 375 μl of 2 M MgCl2 and more water to the final volume of 250 ml. Store this buffer at 4 °C for &le;3 months.

- <span class="buffer">DSP 50 mg/ml stock</span><br>

Dissolve a 50-mg vial of DSP in 1 ml of anhydrous DMSO (use a new vial of DMSO), because DSP will precipitate in aqueous solutions. Dissolved DSP should be used immediately **for practical reasons, this is not necessary**.
Store the stock solution at -80 °C for \lt 3 months.

- <span class="buffer">Yoyo-1 dye for counting</span><br>
Dilute 1 μl of Yoyo-1 dye in 1 ml of 0.3 M SPBSTM in a dark or amber microcentrifuge tube and store the reagent at 4 °C for &le;3 months. This will be used to dilute nuclei for counting.

- <span class="buffer">Annealed N7 oligos</span><br>
The annealed N7 oligos are Tn5-N7 (<span class="sequence">5'-GTCTCGTGGGCTCGGAGATGTGTATAAGAGACAG-3'</span>) and ME (<span class="sequence">5'-[phos]CTGTCTCTTATACACATCT-3'</span>). Resuspend both oligos to 100 μM in annealing buffer (50 mM NaCl, 40 mM Tris-HCl pH 8.0). Mix one volume of Tn5-N7 with one volume of ME. This creates a working stock at 50 μM. Anneal them with the following PCR program: 95 °C for 5 min, cool to 65 °C (0.1 °C/s), 65 °C for 5 min, cool to 4 °C (0.1 °C/s). Store annealed oligos at 4 °C for 6 months or divide them into aliquots and freeze them at 20 °C for &le;1 year.

- <span class="buffer">N7-loaded Tn5</span><br>
To 20 μl of Tn5, add 20 μl of annealed N7 oligos. Place in a thermomixer and shake at 350 rpm and 23 °C for 30 min. Add 20 μl of glycerol. Store at -20 °C for &le;6 months.

- <span class="buffer">Tagment DNA buffer (2×)</span><br>
To 38.75 ml of nuclease-free water, add 1ml of 1M Tris pH7.6, 250μl of 2M MgCl<sub>2</sub> and 10 ml of dimethylformamide. The final volume is 50 ml. Make 550 μl aliquots and store them at -20 °C for &le;6 months.

- <span class="buffer">Indexed primer plates</span><br>
Primers for reverse transcription, ligation and PCR indexing steps are ordered at 100 μM. Working dilutions are made to 10 μM in EB (10 mM Tris-Cl pH 8.5) and kept at 4 °C for &le;6 months.

<aside>
<span class="critical">CRITICAL:</span>Spin the primer plates down before opening, but do not spin the plates with nuclei until the second-strand synthesis stage.
</aside>

- <span class="buffer">10% (vol/vol) IGEPAL</span><br>
Dilute 5 ml of IGEPAL in 45 ml of nuclease-free water. Store at room temperature for &le;6 months.

- <span class="buffer">10% (vol/vol) Triton X-100</span><br>
Dilute 5 ml of Triton X-100 in 45 ml of nuclease-free water. Store at room temperature for &le;6 months.

- <span class="buffer">10% (vol/vol) Tween 20</span><br>
Dilute 5 ml of Tween 20 in 45 ml of nuclease-free water. Store at room temperature for &le;6 months.

- <span class="buffer">Protease</span><br>
Add 7 ml of water to a bottle of lyophilized Qiagen protease (Qiagen, cat. no. 19157). Make 200-μl aliquots and store them at -20 °C for &le;6 months. Do not freeze–thaw.

<aside>
<span class="critical">CRITICAL:</span>  This must be the specified protease, not proteinase K.
</aside>