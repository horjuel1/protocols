---
title: sci-protocol
subtitle: Modified sci-RNA-Seq3 protocol for single-cell/nucleus RNA-seq
date: May 15, 2023
Author: Chaichontat Sriworarat
---

Main reference is [@martinOptimizedSinglenucleus2023]. All modifications/improvements are derivative of this base protocol.

# Table of Contents
- [Table of Contents](#table-of-contents)
- [Preparation](#preparation)
  - [Materials \& Reagents](#materials--reagents)
  - [Buffers \& Solutions](#buffers--solutions)
    - [Reagent setup](#reagent-setup)
      - [10× PBS-hypotonic stock solution](#10-pbs-hypotonic-stock-solution)
      - [Hypotonic lysis buffer solution A](#hypotonic-lysis-buffer-solution-a)
      - [Hypotonic lysis buffer solution B](#hypotonic-lysis-buffer-solution-b)
      - [0.3 M SPBSTM (sucrose PBS TritonX MgCl2)](#03-m-spbstm-sucrose-pbs-tritonx-mgcl2)
      - [DSP 50 mg/ml stock](#dsp-50-mgml-stock)
      - [Yoyo-1 dye for counting](#yoyo-1-dye-for-counting)
      - [Annealed N7 oligos](#annealed-n7-oligos)
      - [N7-loaded Tn5](#n7-loaded-tn5)
      - [Tagment DNA buffer (2×)](#tagment-dna-buffer-2)
      - [Indexed primer plates](#indexed-primer-plates)
      - [10% (vol/vol) igepal](#10-volvol-igepal)
      - [10% (vol/vol) Triton X-100](#10-volvol-triton-x-100)
      - [10% (vol/vol) Tween 20](#10-volvol-tween-20)
      - [Protease](#protease)
- [Protocol](#protocol)
  - [Nuclei isolation](#nuclei-isolation)
    - [Procedure](#procedure)
  - [Nuclei/Cell Fixation](#nucleicell-fixation)
  - [Reverse Transcription](#reverse-transcription)
  - [Ligation](#ligation)
  - [Final distribution](#final-distribution)
  - [Second-strand synthesis](#second-strand-synthesis)
  - [Protease Digestion](#protease-digestion)
  - [Tagmentation](#tagmentation)
- [References](#references)

# Preparation

## Materials & Reagents

|Reagent | Vendor | Notes|
|--------|--------|------|
| DSP | (Lomant’s reagent; Thermo Fisher, cat. no. 22586 or PG82081) | <span style="color: #702963;">**CRITICAL:**</span>  DSP is sensitive to water and should be used immediately after dissolving in dimethyl sulfoxide (DMSO) |
| Methanol | (Millipore Sigma, cat. no. 494437-2L) |     |
| DMSO | (Millipore Sigma, cat. no. D2438-5X10ML) | <span style="color: #702963;">**CRITICAL:**</span>  DMSO used for dissolving DSP should be new and unopened so that water is not introduced. These smaller bottles are useful for this reason.     |
| Sodium phosphate dibasic | (Millipore Sigma, cat. no. S3264-250G) |   |
| Sodium phosphate monobasic monohydrate | (Millipore Sigma, cat. no. 71507-250G) |    |
| Potassium phosphate monobasic | (Millipore Sigma, cat. no. P9791-100G) |    |
| Sodium chloride | (Millipore Sigma, cat. no. S3014-500G) |   |
| Potassium chloride | (Millipore Sigma, cat. no. P9541-500G) |   |
| Magnesium chloride solution, 2 M | (Millipore Sigma, cat. no. 68475-100ML-F) |    |
| Igepal CA-630 | (Millipore Sigma, cat. no. I8896-50ML) |     |
| BSA, 20 mg/ml | (New England Biolabs, cat. no. B9000S) |     |
| DEPC | (Millipore Sigma, cat. no. D5758-25ML) | **CAUTION** Handle DEPC, and samples containing it, in a fume hood.   |
| Sucrose | (VWR, cat. no. 97061-428) |   |
| Triton X-100 | (Millipore Sigma, cat. no. T8787-100ML) |     |
| Tween 20 | (Thermo Fisher, cat. no. BP-337-100) |   |
| 10× Dulbecco’s PBS | (10× DPBS; Thermo Fisher, cat. no. 14200075) |   |
| Superscript IV reverse transcriptase | (Thermo Fisher, cat. no. 18090200) |    |
| T4 DNA Ligase | (New England Biolabs, cat. no. M0202L) |     |
| Tagmentase (Tn5 transposase) , unloaded | (Diagenode, cat. no. C01070010-20) | <span style="color: #702963;">**CRITICAL:**</span> The amount of tagmentase added to Step 57 has been determined for this brand only.   |
| Tn5-N7 oligo | (5'-GTCTCGTGGGCTCGGAGATGTGTATAAGAGACAG-3', high-purity salt-free; Eurofins) |     |
| Mosaic End (ME) oligo | (5'-/5Phos/CTGTCTCTTATACACATCT-3', high-purity salt-free; Eurofins) |   |
| NEBNext mRNA second-strand synthesis module | (New England Biolabs, cat. no. E6111L) |     |
| NEBNext high !delity 2× PCR master mix | (New England Biolabs, cat. no. M0541L) |    |
| dNTP mix | (New England Biolabs, cat. no. N0447L) |    |
| Agencourt AMPure XP | (Beckman Coulter, cat. no. A63882) |   |
| Yoyo dye | (Thermo Fisher, cat. no. Y3601) |     |
| RNaseAlert kit | (IDT, cat. no. 11-02-01-02) |   |
| RNaseZap | (Thermo Fisher, cat. no. AM9780) |    |
| Elution buffer | (EB, 10 mM Tris pH 8.5; Qiagen, cat. no. 19086) |    |
| Protease | (Qiagen, cat. no. 19157) | <span style="color: #702963;">**CRITICAL:**</span>  Do not use any other protease/proteinase. This one can be heat-inactivated at the temperature and time listed in the protocol. |
| 6% TBE Novex PAGE gels | (10 wells; Thermo Fisher, cat. no. EC6262BOX) |    |
| UltraPure agarose | (Thermo Fisher, cat. no. 16500-500) |    |
| Qubit double-stranded DNA high-sensitivity quantitation kit | (Thermo, cat. no. Q32851) |     |
| sci-RNA-seq3 indexed primer plates at 10 &mu;M dilution (standard desalting for puri!cation; random bases do not need hand-mixing). |   The plates include the following: plate(s) of indexed oligo-dT RT primers (5'- /5Phos/ CAGAGCNNNNNNNN[10bpRTindex]TTTTTTTTTTTTTTTTTTTTTTTTTTTTTT-3', where ‘N’ is any base; IDT), plate(s) of indexed ligation primers (5'- GCTCTG[9- or 10-bp ligation index] TACGACGCTCTTCCGATCT[reverse complement of ligation index]-3'), plate of indexed PCR P7 primers (5'-CAAGCAGAAGACGGCATACGAGAT[PCR P7 index]GTCTCGTGGGCTCGG-3'; IDT); and PCR P5 primers (this primer does not need to be indexed if you do only one plate of PCR) (5'-AATGATACGGCGACCACCGAGATCTACAC[PCR P5 index]ACACTCTTTCCCTA- CACGACGCTCTTCCGATCT-3'; IDT). | \***These are modified from sci-RNA-SeqV3** |

## Buffers & Solutions

### Reagent setup
#### 10× PBS-hypotonic stock solution
Mix 5.45 g of Na2HPO4 (dibasic), 3.1 g of NaH2PO4·H20, 1.2 g of KH2PO4, 1 g of KCl and 3 g of NaCl in nuclease-free water and bring to a !nal volume of 500 ml. This stock solution will have a pH of ~6.8, but when diluted to 1×, should end up at pH 7.0–7.4. The buffer can be stored at room temperature (20–23 °C) for 6 months.

#### Hypotonic lysis buffer solution A
This buffer is used for whole mouse embryos E16.5 and older. Mix 5 ml of the 10× PBS-hypotonic stock solution, 5.7 g of sucrose, 75 &mu;l of 2 M MgCl2 and nuclease-free water to a !nal volume of 50 ml to make the lysis base solution. Right before lysis, for every 1 ml of lysis buffer needed, add 2.5 &mu;l of 10% (vol/vol) igepal (vol/vol) and 10 &mu;l of DEPC and then vortex the solution to disperse the DEPC throughout. For example, if a sample needs 5 ml of lysis buffer, take a 5-ml aliquot of lysis buffer stock solution and add 12.5 &mu;l of 10% (vol/vol) igepal and 50 &mu;l of DEPC. Keep the buffer on ice. Make fresh for each experiment. ! CAUTION DEPC needs to be used in a fume hood. <span style="color: #702963;">**CRITICAL:**</span>  DEPC has a short half-life in aqueous solutions, so adding it to the buffer just before the cells are added is important.

#### Hypotonic lysis buffer solution B
This buffer is used for Tiny-Sci, cell lines, mouse embryos under E16.5 and isolated tissues. Mix 5 ml of the 10× PBS-hypotonic stock solution, 75 &mu;l of 2 M MgCl2 and nuclease-free water to a !nal volume of 50 ml to make the lysis base solution. Right before lysis, for every 1 ml of lysis buffer needed, add 40 &mu;l of BSA (20 mg/ml), 2.5 &mu;l of 10% (vol/vol) igepal and 10 &mu;l of DEPC and then vortex the solution to disperse the DEPC throughout. For example, if a sample needs 5 ml of lysis buffer, take a 5-ml aliquot of lysis buffer base solution and add 200 &mu;l of BSA, 12.5 &mu;l of 10% (vol/vol) igepaland50&mu;lofDEPC.Keepthebufferonice.Makefreshforeachexperiment.!CAUTION DEPC needs to be used in a fume hood. CRITICAL DEPC has a short half-life in aqueous solutions, so adding it to the buffer just before the cells are added is important.

#### 0.3 M SPBSTM (sucrose PBS TritonX MgCl2)
This is the main buffer used throughout the protocol for washing and diluting nuclei. Dissolve 28.5 g of sucrose in 25 ml of 10× DPBS (regular DPBS, not the hypotonic version) and 125 ml of nuclease- free water (about half the volume of water that you will need). Once the sucrose has dissolved, add 2.5 ml of 10% (vol/vol) Triton X-100, 375 &mu;l of 2 M MgCl2 and more water to the !nal volume of 250 ml. Store this buffer at 4 °C for à3 months.

#### DSP 50 mg/ml stock
Dissolve a 50-mg vial of DSP in 1 ml of anhydrous DMSO (use a new vial of DMSO), because DSP will precipitate in aqueous solutions. Dissolved DSP should be used immediately.

#### Yoyo-1 dye for counting
Dilute 1 &mu;l of Yoyo-1 dye in 1 ml of 0.3 M SPBSTM in a dark or amber microcentrifuge tube and store the reagent at 4 °C for à3 months. This will be used to dilute nuclei for counting.

#### Annealed N7 oligos
The annealed N7 oligos are Tn5-N7 (5!-GTCTCGTGGGCTCGGAGATGTGTATAAGAGACAG-3!) and ME (5!-[phos]CTGTCTCTTATACACATCT-3!). Resuspend both oligos to 100 !M in annealing buffer (50 mM NaCl, 40 mM Tris-HCl pH 8.0). Mix one volume of Tn5-N7 with one volume of ME. This creates a working stock at 50 !M. Anneal them with the following PCR program: 95 °C for 5 min, cool to 65 °C (0.1 °C/s), 65 °C for 5 min, cool to 4 °C (0.1 °C/s). Store annealed oligos at 4 °C for 6 months or divide them into aliquots and freeze them at !20 °C for à1 year.

#### N7-loaded Tn5
To 20 &mu;l of Tn5, add 20 &mu;l of annealed N7 oligos. Place in a thermomixer and shake at 350 rpm and 23 °C for 30 min. Add 20 &mu;l of glycerol. Store at !20 °C for à6 months.

#### Tagment DNA buffer (2×)
To38.75mlofnuclease-freewater,add1mlof1MTrispH7.6,250&mu;lof2MMgCl2 and10mlof dimethylformamide. The !nal volume is 50 ml. Make 550-&mu;l aliquots and store them at !20 °C for à6 months.

#### Indexed primer plates
Primers for reverse transcription, ligation and PCR indexing steps are ordered at 100 !M. Working dilutions are made to 10 !M in EB (10 mM Tris-Cl pH 8.5) and kept at 4 °C for à6 months. <span style="color: #702963;">**CRITICAL:**</span>  Spin the primer plates down before opening, but do not spin the plates with nuclei until
the second-strand synthesis stage (Step 50).

#### 10% (vol/vol) igepal
Dilute 5 ml of igepal in 45 ml of nuclease-free water. Store at room temperature for à6 months.

#### 10% (vol/vol) Triton X-100
Dilute 5 ml of Triton X-100 in 45 ml of nuclease-free water. Store at room temperature for à6 months.

#### 10% (vol/vol) Tween 20
Dilute 5 ml of Tween 20 in 45 ml of nuclease-free water. Store at room temperature for à6 months.

#### Protease
Add 7 ml of water to a bottle of lyophilized Qiagen protease (Qiagen, cat. no. 19157). Make 200-&mu;l aliquots and store them at !20 °C for à6 months. Do not freeze–thaw. <span style="color: #702963;">**CRITICAL:**</span>  This must be the speci!ed protease, not proteinase K.

# Protocol

## Nuclei isolation

<span style="color: #6495ED;">**Timing: 2 h**</span>


<span style="color: #702963;">**CRITICAL:**</span> Keep everything cold and on ice at all times. Pre-cool tubes on ice before adding cells/nuclei.


<span style="color: #702963;">**CRITICAL:**</span> LoBind (DNA/RNA) microcentrifuge tubes are preferred for all steps in which they are used for collecting nuclei.


1. Prepare two ice buckets with wet ice, a bucket with crushed dry ice to hold your frozen tissues, and a thick, flat slab of dry ice for smashing tissues. Pre-cool both a centrifuge that will hold 50-ml tubes and a microcentrifuge to 4 °C.

2. Determine how much lysis buffer you will need for the tissue you will be processing. (For extremely small samples, skip to Box 1: Tiny-Sci.) An E13.5 mouse embryo (~200 mg) requires 5 ml of lysis buffer. An E16.5 embryo (~500 mg) will need 20 ml. An adult mouse heart needs 5 ml. Adult mouse kidneys need 5 ml per kidney. Adult mouse liver needs 20 ml. Adult mouse pancreas needs 15 ml. Adult tissues and tissues high in RNases will necessitate a bigger lysis volume. The buffer is inexpensive to make, so do not worry about using too much.
**CAUTION:** DEPC is flammable and toxic. Avoid breathing vapors. The following steps should be performed in the chemical hood from this point until the DEPC is washed from the sample (Step 17).

3. For every 1 ml of lysis buffer needed, add 2.5 μl of 10% (vol/vol) IGEPAL and 10 μl of DEPC to the hypotonic lysis buffer solution (and 40 μl of BSA if using lysis buffer B) and then vortex the solution to disperse the DEPC throughout. Have complete lysis buffer in a 50-ml tube for each sample on ice ready to go.

4. Fold a piece of aluminum foil four times so that you have a small pouch with eight layers of foil on each side. Place this on a slab of dry ice to chill.

5. Place your frozen tissue inside this foil and hold it firmly closed on the dry ice and smash it with a hammer (Fig. 4 and Supplementary Video 1). You want to be gentle enough not to tear the foil, but thorough enough to make a powder of the tissue. Do not let the tissue thaw.

6. Use the foil to guide your powdered tissue into the tube of the lysis buffer. It will stick a bit; pipette some of the lysis buffer from the tube to rinse the sample from the foil into the tube. Try to make sure that the sample is thawing only if it is in the lysis buffer.

7. Cap the 50-ml tube and shake it to disperse the chunks in the buffer. Let it sit on ice for 10 min. Triturate the chunks with a 1-ml pipette tip to help tease them apart a bit.

8. Set up another 50-ml tube on ice with a 40-μm cell strainer on top. Pour your lysate through that; there will still be a lot of chunks. Use a disposable pestle to coax the tissue through the filter. Do not worry about getting all of it through.

9. Take a 45-μl sample of the filtered lysate and check for RNase activity with the IDT RNaseAlert kit. The RNaseAlert test will guide you on whether to proceed or not. There should not be any RNase detected, and if there is, you will have to restart with a new sample and adjust either the sample size or the volume of lysis buffer

10. While the RNaseAlert sample is incubating, spin down the remainder of the lysate (500g, 3 min, 4 °C).  Keep the nuclei in the 50-ml tube.  Resuspend the nuclei in 1 ml of 0.3 M SPBSTM with 10 μl of DEPC added (or more buffer if there are a lot of nuclei—roughly 1 ml of buffer per 200-500 mg of starting material at minimum).

**Tiny-Sci (optional approach)**

<span style="color: #6495ED;">**Timing 1 h**</span>

### Procedure

1. Samples should be no more than 2-3 mm in size, should be frozen individually in a microcentrifuge tube and kept on dry ice until lysis. The key to these small samples is to limit pipetting  and tube transfers that will leave behind precious nuclei.

2. You will need 100 μl of lysis buffer B per embryo, but make up enough for several samples.

3. Right before lysis, for every 1 ml of lysis buffer needed, add 2.5 μl of 10% (vol/vol) igepal, 40 μl of BSA (20 mg/ml) and 10 μl of DEPC and then vortex the solution to disperse the DEPC throughout. **CAUTION: You must work in the hood because the DEPC is toxic.**

4. Add 100 μl of complete lysis buffer (with BSA/DEPC/igepal) to the tube with the frozen embryo and make sure that the embryo is actually in the buffer. Let it sit a couple of minutes on ice and then triturate the embryo slowly and gently with a pipette set to 50 μl with a yellow (200 μl) tip. You should not see any chunks left. Lysis time is only ~5 min.

5. (Optional) You can take 1 μl of this and mix it with 9 μl of diluted Yoyo dye to quickly check under a microscope with a GFP filter to make sure that you are seeing intact, separate nuclei.

6. Mix fixative: 400 μl of ice-cold methanol + 10 μl of DSP stock solution. Add 400 μl to the embryo on ice dropwise over 1–2 min. Do not pipette up and down; instead, flick gently to mix and repeat occasionally over 5–10 min. You may see some clumping now.

7. Add 1 ml of 0.3 M SPBSTM dropwise, slowly and mixing gently by flicking. Do not pipette up and down.

8. Spin at 500g for 3 min at 4 °C. You should see a very tiny pellet. Remove all but ~50 μl of the supernatant and discard, without disturbing the pellet.

9. Add 500 μl of 0.3 M SPBSTM. Set a 1-ml pipette to 100 μl and resuspend by pipetting gently.

10. If you got clumps from fixing, sonicate the tube for 12 s on low at 4 °C.

11. Spin again at 500g for 3 min at 4 °C. Carefully remove the supernatant and resuspend the nuclei pellet gently in SPBSTM so that the volume is 42.5 μl. Add 2.5 μl of 10 mM dNTPs and put 5 μl into each well of one column on a plate, noting into which wells the nuclei went.

12. Fill up the plate with more embryos or some other nuclei of which you have a lot and continue with the sci procedure at Step 24 of the reverse
transcription.

## Nuclei/Cell Fixation

<span style="color: #6495ED;">**Timing:** 1 h</span>

1. For each sample, prepare fixative. In a 5-ml tube, add 100 μl of 50 mg/ml DSP stock solution to 4 ml of ice-cold methanol for every 1 ml of nuclei with which you are starting.

2. Add the prepared fixative gradually to the 50-ml tube containing the nuclei, swirling as you are adding it.

3. Fix on ice for 15 min, swirling occasionally.

<span style="color: #228B22;">**PAUSE POINT**</span> Fixed samples may be held here prior to rehydration. To pause, add 0.1 volume of 1M glycine pH 8.5 to quench DSP. Store at −80°C

4. Add 2 volumes of 0.3 M SPBSTM **(or PBS-T if using cells)** gradually, 2–3 ml at a time, swirling between additions to rehydrate the nuclei. For instance, with 1 ml of nuclei and 4 ml of fixative, you would need 10 ml of buffer to rehydrate.

5. Spin down the nuclei at 1000g for 2 min at 4 °C.

6. Carefully remove the supernatant and dispose properly. The nuclei pellet is at the bottom and should look a little white-ish from the DSP.

7. Resuspend the nuclei in ≥1 ml of 0.3 M SPBSTM **(or PBS-T if using cells)**. Triturate gently with a pipette tip to separate nuclei.

8. Divide fixed nuclei into aliquots of ~2 million nuclei (Fig. 5) in microcentrifuge tubes. Spin at 500g for 3 min at 4 °C and remove and discard the supernatant. Continue with the protocol or snap-freeze tubes in liquid nitrogen and store at −80 °C.

<span style="color: #228B22;">**PAUSE POINT**</span> Fixed samples may be stored at −80 °C for ≤6 months.

9. (**Optional**) If continuing with the protocol the same day and there are obvious clumps at this point that will not tease apart, you will need to sonicate them to break them up. Sonicate (Diagenode Bioruptor Plus) on low intensity for 12 s only at 4 °C. Spin and resuspend the nuclei in 500 μl of 0.3M SPBSTM (or PBS-T) as in Step 21.

## Reverse Transcription

<span style="color: #6495ED;">**Timing:** 2-3 h</span>

Follow the chart below to determine how many starting nuclei you need and their volume. 

|No. of cells | 2,000,000 | 1,000,000 | 800,000 | 500,000 | 400,000 | 200,000 |
|-------------|-----------|-----------|---------|---------|---------|---------|
|**No. of columns** |12 |6 |4 |3 |2 |1|
|**Nuclei volume (&mu;l)** |500 |250 |170 |125 |85 |42.5|
|**10 mM dNTP (&mu;l)** |56 |28 |19 |14 |9.5 |4.75|

If you are dividing the plate among multiple samples, then the chart will outline the cell number you need depending on how many columns in the plate each sample will occupy. For example, if you will have two samples on one plate, each one will take six columns, you will need 1 million cells of each sample in a tube to start with in a volume of 250 &mu;l each, and you will add 28 &mu;l of dNTPs to each before distributing to their RT plate wells.

1. Resuspend an aliquot of frozen nuclei in 500 &mu;l of 0.3 M SPBSTM to start. Count. Dilute nuclei if necessary to get an accurate count. If nuclei are clumpy, sonicate (Diagenode Bioruptor Plus) on low intensity for 12 s only at 4 °C. If there is still an excess of clumps, put the nuclei over a 40-!m Flow-mi pipette tip &mu;lter before counting. Use of a Flow-mi &mu;lter is a last resort because it results in nuclei loss but is helpful if you have an excess of nuclei.

2. Pull out the desired amount of nuclei into a new tube and spin. Remove the supernatant and resuspend nuclei in the necessary volume of 0.3 M SPBSTM determined by the chart above and add the appropriate amount of dNTPs.

3. Distribute 5-&mu;l aliquots of nuclei+dNTP mix to each well of the plate on ice.

4. Quickly spin the plate of three-level RT primers (10 !M) (5!-/5Phos/CAGAGCNNNNNNNN[10-bp RT index]TTTTTTTTTTTTTTTTTTTTTTTTTTTTTT-3!, where ‘N’ is any base)

5. Add 2 &mu;l of primer to each well. Do not pipette up and down to mix; just stir gently with the pipette tips.

6. Incubate the plate at 55 °C for 5 min in a PCR machine (heated lid set to 65 °C) and then immediately place on ice.

7. While this is incubating, make the reaction mix. Note: we do not include dithiothreitol in this mix,
because it will undo the DSP cross-links (it is not necessary for the RT to work).

|RT mix per plate |1 well| x110 |
|-----------------|------|------|
|5× Superscript IV buffer (&mu;l)| 2 | 220 |
|Maxima RT H Minus (&mu;l) | 0.25 | 27.5 |
| Nuclease Free H<sub>2</sub>O (&mu;l)| 0.75 | 82.5 |
\*_Do NOT use 5x Maxima buffer, contains DTT_

8. Put 3 &mu;l of reaction mix into each well (45 &mu;l of mix × 8 in a strip tube for multichannel pipetting), stirring gently with tips. The total volume per well is now 10 &mu;l.

9. Incubate at 50°C for 30 min (heated lid at 65 °C) and then immediately place on ice.

10. Ice plates until they are cold (>2 min). Add 5 &mu;l of cold 0.3 M SPBSTM per well. To maximize recovery, pool wells by using a 12-multichannel pipette with 200 &mu;l tips to pipette gently up and down (the pipetting up and down is important to dislodge the nuclei, but try to avoid creating excessive bubbles) and combine each row of the plate into the bottom row. You can use the same tips for the whole plate. Then, collect these wells into two cold microcentrifuge tubes. (The solution will be bubbly, so it is dif!cult to squeeze into one tube.)

11. Spin at 500g for 3 min at 4 °C. The pellet will be small, but you should be able to see it. Remove and discard the supernatant. 1,000g 1 min

12. Combine tubes and wash once more in 1 ml of cold 0.3 M SPBSTM. Spin at 500g for 3 min at 4 °C.
Remove and discard the supernatant.

## Ligation

<span style="color: #6495ED;">**Timing:** 1.5 h</span>

|4x Ligation master mix w/ 12% 1,2-propanediol |200 μl|
|----------------------------------------------|------|
|10x T4 buffer |80 &mu;l|
|1,2-propanediol |96 μl |
|T4 ligase |20 μl |
| Nuclease Free H<sub>2</sub>O |4 μl|
\*_Make and store at -20°C. Should not freeze._

1. Resuspend nuclei in 1,200 &mu;l of 0.3 M SPBSTM.
2. Distribute 5 &mu;l to each well of a new plate on ice.
3. Quick-spin the plate of three-level ligation primers (10 !M) (5!-GCTCTG[9- or 10-bp ligation index]TACGACGCTCTTCCGATCT[reverse complement of ligation index]-3!).
4. Add 2 &mu;l of primer to each well. Do not pipette up and down.
5. Make a 3:1 mix of 10× T4 ligation buffer and T4 DNA ligase (195 &mu;l of 10× buffer + 65 &mu;l of T4 DNA ligase).
6. Add 2.5 &mu;l of ligase mix to each well (40 &mu;l × 8 in a strip tube for multichannel pipetting). The total volume per well is now 9.5 &mu;l.
7. Incubate for 20 min at room temperature.
8. Ice plates until cold.
9. Add 10 &mu;l of cold SPBSTM to each well. This helps keep the nuclei from clumping and allows for more nuclei to be recovered.
10. Pool wells by using a 12-multichannel to pipette gently up and down (the pipetting up and down is important to dislodge the nuclei) and combine each row of the plate into the bottom row. Then, collect these wells into two cold microcentrifuge tubes.
11. Spin at 1,000g for 1 min at 4 °C. Remove and discard the supernatant.
12. Combine the two tubes and wash twice more with 1 ml of 0.3 M SPBSTM per wash.
13. Resuspend in 1 ml of 0.3 M SPBSTM to count. If nuclei are clumpy and cannot be teased apart with gentle pipetting, sonicate on low intensity for 6 s only at 4 °C and recount. Note that this is a shorter sonication step than before.

## Final distribution

<span style="color: #6495ED;">**Timing:** 1 h</span>

Sort if possible.

<span style="color: #702963;">**CRITICAL:**</span>  In the final plate, you will want ~1,000 nuclei/well (or 4,000/well if you have scaled up the experiment to 384 × 384 × 384). You should have enough nuclei to freeze multiple plates if you like.

1. Make 400 &mu;l of 1× second-strand synthesis buffer for each plate in the !nal distribution. Dilute 40 &mu;l of 10× second-strand buffer in 360 &mu;l of water to get 1× concentration.
2. Spin down 100,000 nuclei for each plate desired for the !nal distribution (400,000 per plate if this is a 384 × 384 × 384 experiment). For each plate/100,000, resuspend in 400 &mu;l of 1× second-strand synthesis buffer
3. Put 4 &mu;l of nuclei into each well of a regular, not LoBind, plate on ice.
4. Cover with foil seals and freeze plates at !80 °C or proceed with second-strand synthesis.

<span style="color: #228B22;">**PAUSE POINT**</span> Plates may be kept frozen at !80 °C for à6 months.

## Second-strand synthesis 

<span style="color: #6495ED;">**Timing:** 3 h (or overnight)</span>

1. Thaw plate on ice.
2. Make second-strand synthesis mix on ice as follows:

|Reaction mix per plate| 1 well |×140|
|----------------------|--------|----|
| Nuclease Free H<sub>2</sub>O (&mu;l) | 0.675| 94.5|
|Second-strand buffer (10×) (&mu;l) | 0.075 | 10.5|
|Second-strand enzyme (20×) (&mu;l) | 0.25 | 35|

3. Put 1 &mu;l of second-strand synthesis mix into each well (17 &mu;l of mix ×8 in a strip tube for multichannel pipetting). The total volume per well is now 5 &mu;l.
4. Incubate for 2.5 h at 16 °C in a PCR machine (no heated lid). 

<span style="color: #228B22;">**PAUSE POINT**</span> Keep the plate at 4 °C for &le;24 h.

## Protease Digestion

<span style="color: #6495ED;">**Timing:** 2 h</span>

1. Add 1 &mu;l of protease to each well.
<span style="color: #702963;">**CRITICAL:**</span> This is not proteinase K. Using Qiagen protease (cat. no 19157) is important because it can be heat-inactivated. See Reagent setup.

2. Incubate at 37 °C for 40 min in a PCR machine (47 °C heated lid). Check 1 &mu;l on a microscope: mix a 1-&mu;l sample with 2 &mu;l of diluted Yoyo-1 dye, put this on a slide and check on the GFP channel. You should see whisps of DNA instead of intact nuclei. If not, incubate for another 10 min before proceeding to heat inactivation.
3. Heat-inactivate the protease at 75 °C for 20 min (85 °C heated lid).
<span style="color: #702963;">**CRITICAL:**</span> Do not lower this temperature and do not shorten this time. Qiagen lists different conditions for heat-inactivating their protease, but it is not suf!cient. Put the plate on ice after inactivating.

<span style="color: #228B22;">**PAUSE POINT**</span> Store the plate at 4 °C for à1 week.

## Tagmentation

# References

[^ref]
