---
title: sci Sample Preparation
subtitle: Modified sci-RNA-Seq3 protocol for single-cell/nucleus RNA-seq
date: Jan 4, 2024
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

Main reference is [@martinOptimizedSinglenucleus2023].
All modifications/improvements are derivative of this base protocol.

Note that their volume estimate is way overkill, 10% extra for pipetting is enough.

Changes are in bold.

To print with the sidebar, resize your browser window to be narrow until the sidebar merges with the main text.

## Table of Contents

- [Nuclei isolation](#nuclei-isolation)
- [Tiny-Sci](#tiny-sci)
- [Nuclei/Cell Fixation](#nucleicell-fixation)
- [References](#references)

## Protocol

### Nuclei isolation

**For extremely small samples (2-3 mm), skip to [Tiny-Sci](#tiny-sci)**

<aside>
<span class="timing">Timing: 2 h</span>
<span class="critical">CRITICAL:</span> Keep everything cold and on ice at all times.<br>
</aside>

1. Things to prepare beforehand.
   - Pre-cool a microcentrifuge to 4°C.
   - Pre-cool a centrifuge that will hold 50-ml tubes to 4°C.
   - Prepare two ice buckets with wet ice.
   - A nearby -80°C freezer or a bucket with crushed dry ice to hold your frozen tissues.
   - A thick, flat slab of dry ice or metal for smashing tissues.
   - A pre-chilled hammer at -80°C.
   - Pieces of aluminum foil folded four times for each sample.
     <aside>
  Adult tissues and tissues high in RNases will necessitate a bigger lysis volume.
   - An E13.5 mouse embryo (~200 mg) requires 5 ml of lysis buffer.
   - An E16.5 embryo (~500 mg) will need 20 ml. An adult mouse heart needs 5 ml.
   - Adult mouse kidneys need 5 ml per kidney.
   - Adult mouse liver needs 20 ml.
   - Adult mouse pancreas needs 15 ml.
   </aside>
<span class="caution">CAUTION:</span> DEPC is flammable and toxic. Avoid breathing vapors. The following steps should be performed in the chemical hood from this point until the DEPC is washed from the sample. Or at the very least, add 100% DEPC in the fume hood.</span>
   - Determine the amount of lysis buffer that you need, for every 1 ml of lysis buffer needed,
     - add 2.5 μl of 10% (vol/vol) IGEPAL
     - add 10 μl of DEPC to the hypotonic lysis buffer solution (and 40 μl of BSA if using lysis buffer B) and then vortex the solution.

1. Place the folded aluminum foil between the slab and hammer to chill.

2. Remove your tissue from the storage tube. Try using a pipette tip to poke the tissue out you can also warm the tube slightly with your hands to loosen the tissue from the tube. If all fails, smash the tube inside the aluminum foil.

3. Place your frozen tissue inside this foil and hold it firmly closed on the dry ice and smash it with a hammer (Fig. 4 and Supplementary Video 1). You want to be gentle enough not to tear the foil, but thorough enough to make a powder of the tissue. <span class="critical">Do not let the tissue thaw.</span> Check that you are smashing the tissue.

4. Use the foil to guide your powdered tissue into the tube of the lysis buffer. It will stick a bit; pipette some of the lysis buffer from the tube to rinse the sample from the foil into the tube. <span class="critical">Try to make sure that the sample is thawing only if it is in the lysis buffer.</span>

5. Cap the 50-ml tube and vortex it to disperse the chunks in the buffer. Let it sit on ice for 10 min. Triturate the chunks with a 1-ml pipette tip to help tease them apart a bit.

6. Set up another 50-ml tube on ice with a 40-μm cell strainer on top. Using a 1 ml pipette, hold the pipette vertically and force push the sample through the strainer. Move around slightly if clogged. If there are a lot of chunks, use a disposable pestle to coax the tissue through the filter.

7. Wash the filter with 500 μl of the lysis buffer to retrieve nuclei that are stuck on the filter.

8. _Typically not necessary, DEPC kills everything_. Take a 45-μl sample of the filtered lysate and check for RNase activity with the IDT RNaseAlert kit. The RNaseAlert test will guide you on whether to proceed or not. There should not be any RNase detected, and if there is, you will have to restart with a new sample and adjust either the sample size or the volume of lysis buffer

10. Spin down the remainder of the lysate (1,000 g, 3 min, 4°C).  Keep the nuclei in the 50-ml tube.  Resuspend the nuclei in 1 ml of 0.3 M SPBSTM. (or more buffer if there are a lot of nuclei—roughly 1 ml of buffer per 200-500 mg of starting material at minimum).


## Nuclei/cell Fixation

<span class="timing">Timing 1 h</span>

1. For each sample, prepare fixative. In a 50-ml tube, add DSP to a final concentration of 0.5 mg/ml in methanol (a 1:100 dilution of the  50 mg/ml DSP stock) for every 1 ml of nuclei with which you are starting.

2. Add the prepared fixative gradually (over the course of 30 sec - 1 min) to the 50-ml tube containing the nuclei on a vortexer at low setting.

3. Fix on ice for 15 min, swirling occasionally.

> <span class="pause">PAUSE POINT</span> Fixed samples may be held here prior to rehydration. To pause, add 0.1 volume of 1 M glycine pH 8.5 or 1 M Tris pH 7.4 to quench DSP. Store at −80°C.

4. Add 2 volumes of 0.3 M SPBSTM **with 50 mM Tris pH 7.4 _(or PBS-T if using cells)_** gradually, 2–3 ml at a time, swirling between additions to rehydrate the nuclei. For instance, with 1 ml of nuclei and 4 ml of fixative, you would need 10 ml of buffer to rehydrate.

5. Spin down the nuclei at **1,000 g** for 2 min at 4°C.

6. Carefully remove the supernatant and dispose properly. The nuclei pellet is at the bottom and should look a little white-ish from the DSP.

7. Resuspend the nuclei in ≥1 ml of 0.3 M SPBSTM **_(or PBS-T if using cells)_**. Triturate gently with a pipette tip to separate nuclei.
 
8. Divide fixed nuclei into aliquots of ~2 million nuclei (Fig. 5) in microcentrifuge tubes. Spin at **1,000 g** for 3 min at 4°C and remove and discard the supernatant.

9. (**Optional**) If continuing with the protocol the same day and there are obvious clumps at this point that will not tease apart, you will need to sonicate them to break them up. Sonicate (Diagenode Bioruptor Plus) on low intensity for 12 s only at 4°C. Spin and resuspend the nuclei in 500 μl of 0.3M SPBSTM (or PBS-T) as in Step 21.

  - In our case, we first try the table top sonicator. Swirl the 1.5 ml tube around the bath for 10 s. Non-resistant clumps should break at this point.
  - If things are still clumpy, we use a Branson 250 W sonicator with a 3 mm tip with 40% duty cycle at the lowest power setting (around 2) for 3-4 cycles in a 1.5 ml tube with at least 750 μl of SPBSTM. Keep the tip at least 5 mm in the solution to avoid foaming. Do not let the tip get in contact with the tube. Put on ice right away. This should obliterate everything. We have verified that the DAPI signal remains unchanged after the sonication.


## Tiny-Sci (optional approach)

1. Samples should be no more than **2-3 mm** in size, should be frozen individually in a microcentrifuge tube and kept on dry ice until lysis. The key to these small samples is to limit pipetting  and tube transfers that will leave behind precious nuclei.

2. You will need 100 μl of lysis buffer B per embryo, but make up enough for several samples.

3. Right before lysis, for every 1 ml of lysis buffer needed, add 2.5 μl of 10% (vol/vol) IGEPAL, 40 μl of BSA (20 mg/ml) and 10 μl of DEPC and then vortex the solution to disperse the DEPC throughout.

> <span class="caution">CAUTION:</span> You must work in the hood because the DEPC is toxic.

4. Add 100 μl of complete lysis buffer (with BSA/DEPC/IGEPAL) to the tube with the frozen embryo and make sure that the embryo is actually in the buffer. Let it sit a couple of minutes on ice and then triturate the embryo slowly and gently with a pipette set to 50 μl with a yellow (200 μl) tip. You should not see any chunks left. Lysis time is only ~5 min.

5. (Optional) You can take 1 μl of this and mix it with 9 μl of diluted Yoyo dye to quickly check under a microscope with a GFP filter to make sure that you are seeing intact, separate nuclei.

6. Mix fixative: 400 μl of ice-cold methanol + 10 μl of DSP stock solution. Add 400 μl to the embryo on ice dropwise over 1–2 min. Do not pipette up and down; instead, flick gently to mix and repeat occasionally over 5–10 min. You may see some clumping now.

7. Add 1 ml of 0.3 M SPBSTM dropwise, slowly and mixing gently by flicking. Do not pipette up and down.

8. Spin at **1,000 g** for 3 min at 4°C. You should see a very tiny pellet. Remove all but ~50 μl of the supernatant and discard, without disturbing the pellet.

9. Add 500 μl of 0.3 M SPBSTM. Set a 1-ml pipette to 100 μl and resuspend by pipetting gently.

10. If you got clumps from fixing, sonicate the tube for 12 s on low at 4°C.

11. Spin again at **1,000 g** for 3 min at 4°C. Carefully remove the supernatant and resuspend the nuclei pellet gently in SPBSTM so that the volume is 42.5 μl. Add 2.5 μl of 10 mM dNTPs and put 5 μl into each well of one column on a plate, noting into which wells the nuclei went.

12. Fill up the plate with more embryos or some other nuclei of which you have a lot and continue with the sci procedure.
transcription.

## References

[^ref]
