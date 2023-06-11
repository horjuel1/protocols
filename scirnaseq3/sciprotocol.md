---
title: sci-protocol
subtitle: Modified sci-RNA-Seq3 protocol for single-cell/nucleus RNA-seq
date: May 15, 2023
Author: Chaichontat Sriworarat
---

Main reference is [@martinOptimizedSinglenucleus2023].

## Materials & Reagents

- DSP (Lomant’s reagent; Thermo Fisher, cat. no. 22586 or PG82081) CRITICAL DSP is sensitive to water and should be used immediately after dissolving in dimethyl sulfoxide (DMSO).
- Methanol (Millipore Sigma, cat. no. 494437-2L)
- DMSO (Millipore Sigma, cat. no. D2438-5X10ML) CRITICAL DMSO used for dissolving DSP should be new and unopened so that water is not introduced. These smaller bottles are useful for this reason.
- Sodium phosphate dibasic (Millipore Sigma, cat. no. S3264-250G)
- Sodium phosphate monobasic monohydrate (Millipore Sigma, cat. no. 71507-250G)
- Potassium phosphate monobasic (Millipore Sigma, cat. no. P9791-100G)
- Sodium chloride (Millipore Sigma, cat. no. S3014-500G)
- Potassium chloride (Millipore Sigma, cat. no. P9541-500G)
- Magnesium chloride solution, 2 M (Millipore Sigma, cat. no. 68475-100ML-F)
- Igepal CA-630 (Millipore Sigma, cat. no. I8896-50ML)
- BSA, 20 mg/ml (New England Biolabs, cat. no. B9000S)
- DEPC (Millipore Sigma, cat. no. D5758-25ML) **CAUTION** Handle DEPC, and samples containing it, in a fume hood.
- Sucrose (VWR, cat. no. 97061-428)
- Triton X-100 (Millipore Sigma, cat. no. T8787-100ML)
- Tween 20 (Thermo Fisher, cat. no. BP-337-100)
- 10× Dulbecco’s PBS (10× DPBS; Thermo Fisher, cat. no. 14200075)
- Superscript IV reverse transcriptase (Thermo Fisher, cat. no. 18090200)
- T4 DNA Ligase (New England Biolabs, cat. no. M0202L)
Tagmentase (Tn5 transposase), unloaded (Diagenode, cat. no. C01070010-20) CRITICAL The amount of tagmentase added to Step 57 has been determined for this brand only.
- Tn5-N7 oligo (5'-GTCTCGTGGGCTCGGAGATGTGTATAAGAGACAG-3', high-purity salt-free; Eurofins)
- Mosaic End (ME) oligo (5'-/5Phos/CTGTCTCTTATACACATCT-3', high-purity salt-free; Eurofins)
- NEBNext mRNA second-strand synthesis module (New England Biolabs, cat. no. E6111L)
- NEBNext high !delity 2× PCR master mix (New England Biolabs, cat. no. M0541L)
- dNTP mix (New England Biolabs, cat. no. N0447L)
- Agencourt AMPure XP (Beckman Coulter, cat. no. A63882)
- Yoyo dye (Thermo Fisher, cat. no. Y3601)
- RNaseAlert kit (IDT, cat. no. 11-02-01-02)
- RNaseZap (Thermo Fisher, cat. no. AM9780)
- Elution buffer (EB, 10 mM Tris pH 8.5; Qiagen, cat. no. 19086)
- Protease (Qiagen, cat. no. 19157) CRITICAL Do not use any other protease/proteinase. This one can
be heat-inactivated at the temperature and time listed in the protocol.
- 6% TBE Novex PAGE gels (10 wells; Thermo Fisher, cat. no. EC6262BOX)
- UltraPure agarose (Thermo Fisher, cat. no. 16500-500)
- Qubit double-stranded DNA high-sensitivity quantitation kit (Thermo, cat. no. Q32851)

**These are modified from sci-RNA-SeqV3**
- sci-RNA-seq3 indexed primer plates at 10 !M dilution (standard desalting for puri!cation; random
bases do not need hand-mixing). The complete list of primers is found in Supplementary Table 1. The plates include the following: plate(s) of indexed oligo-dT RT primers (5'- /5Phos/ CAGAGCNNNNNNNN[10bpRTindex]TTTTTTTTTTTTTTTTTTTTTTTTTTTTTT-3', where ‘N’ is any base; IDT), plate(s) of indexed ligation primers (5'- GCTCTG[9- or 10-bp ligation index] TACGACGCTCTTCCGATCT[reverse complement of ligation index]-3'), plate of indexed PCR P7 primers (5'-CAAGCAGAAGACGGCATACGAGAT[PCR P7 index]GTCTCGTGGGCTCGG-3'; IDT); and PCR P5 primers (this primer does not need to be indexed if you do only one plate of PCR) (5'-AATGATACGGCGACCACCGAGATCTACAC[PCR P5 index]ACACTCTTTCCCTA- CACGACGCTCTTCCGATCT-3'; IDT).

## Nuclei isolation

<span style="color: #6495ED;">**Timing: 2 h**</span>


<span style="color: #702963;">**CRITICAL:**</span> Keep everything cold and on ice at all times. Pre-cool tubes on ice before adding cells/nuclei.


<span style="color: #702963;">**CRITICAL:**</span> LoBind (DNA/RNA) microcentrifuge tubes are preferred for all steps in which they are used for collecting nuclei.


1. Prepare two ice buckets with wet ice, a bucket with crushed dry ice to hold your frozen tissues, and a thick, flat slab of dry ice for smashing tissues.
   Pre-cool both a centrifuge that will hold 50-ml tubes and a microcentrifuge to 4 °C.

2. Determine how much lysis buffer you will need for the tissue you will be processing.
   (For extremely small samples, skip to Box 1: Tiny-Sci.)
   An E13.5 mouse embryo (~200 mg) requires 5 ml of lysis buffer. An E16.5 embryo (~500 mg) will need 20 ml. An adult mouse heart needs 5 ml.
   Adult mouse kidneys need 5 ml per kidney.
   Adult mouse liver needs 20 ml.
   Adult mouse pancreas needs 15 ml.
   Adult tissues and tissues high in RNases will necessitate a bigger lysis volume.
   The buffer is inexpensive to make, so do not worry about using too much.

   **CAUTION:** DEPC is flammable and toxic. Avoid breathing vapors. The following steps should be performed in the chemical hood from this point until the DEPC is washed from the sample (Step 17).

3. For every 1 ml of lysis buffer needed, add 2.5 μl of 10% (vol/vol) IGEPAL and 10 μl of DEPC to the hypotonic lysis buffer solution (and 40 μl of BSA if using lysis buffer B) and then vortex the solution to disperse the DEPC throughout.
   Have complete lysis buffer in a 50-ml tube for each sample on ice ready to go.

4. Fold a piece of aluminum foil four times so that you have a small pouch with eight layers of foil on each side.
   Place this on a slab of dry ice to chill.

5. Place your frozen tissue inside this foil and hold it firmly closed on the dry ice and smash it with a hammer (Fig. 4 and Supplementary Video 1).
   You want to be gentle enough not to tear the foil, but thorough enough to make a powder of the tissue. Do not let the tissue thaw.

6. Use the foil to guide your powdered tissue into the tube of the lysis buffer.
   It will stick a bit; pipette some of the lysis buffer from the tube to rinse the sample from the foil into the tube.
   Try to make sure that the sample is thawing only if it is in the lysis buffer.

7. Cap the 50-ml tube and shake it to disperse the chunks in the buffer.
   Let it sit on ice for 10 min. Triturate the chunks with a 1-ml pipette tip to help tease them apart a bit.

8. Set up another 50-ml tube on ice with a 40-μm cell strainer on top.
   Pour your lysate through that; there will still be a lot of chunks.
   Use a disposable pestle to coax the tissue through the filter.
   Do not worry about getting all of it through.

9. Take a 45-μl sample of the filtered lysate and check for RNase activity with the IDT RNaseAlert kit.
   The RNaseAlert test will guide you on whether to proceed or not.
   There should not be any RNase detected, and if there is, you will have to restart with a new sample and adjust either the sample size or the volume of lysis buffer

10. While the RNaseAlert sample is incubating, spin down the remainder of the lysate (500g, 3 min, 4 °C).
    Keep the nuclei in the 50-ml tube.
    Resuspend the nuclei in 1 ml of 0.3 M SPBSTM with 10 μl of DEPC added (or more buffer if there are a lot of nuclei—roughly 1 ml of buffer per 200-500 mg of starting material at minimum).

**Tiny-Sci (optional approach)**

<span style="color: #6495ED;">**Timing 1 h**</span>

### Procedure

1. Samples should be no more than 2-3 mm in size, should be frozen individually in a microcentrifuge tube and kept on dry ice until lysis. The key to these small samples is to limit pipetting    and tube transfers that will leave behind precious nuclei.

2. You will need 100 μl of lysis buffer B per embryo, but make up enough for several samples.

3. Right before lysis, for every 1 ml of lysis buffer needed, add 2.5 μl of 10% (vol/vol) igepal, 40 μl of BSA (20 mg/ml) and 10 μl of DEPC and then vortex the solution to disperse the DEPC throughout.

   **CAUTION: You must work in the hood because the DEPC is toxic.**

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

## References

[^ref]
