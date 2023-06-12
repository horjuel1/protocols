---
title: sci Protocol
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

Main reference is [@martinOptimizedSinglenucleus2023].
All modifications/improvements are derivative of this base protocol.

Note that their volume estimate is way overkill, 10% extra for pipetting is enough.

Changes are in bold.

To print with the sidebar, resize your browser window to be narrow until the sidebar merges with the main text.

## Table of Contents

- [Nuclei isolation](#nuclei-isolation)
- [Nuclei/Cell Fixation](#nucleicell-fixation)
- [Reverse Transcription](#reverse-transcription)
- [Ligation](#ligation)
- [Final distribution](#final-distribution)
- [Second-strand synthesis](#second-strand-synthesis)
- [Protease Digestion](#protease-digestion)
- [Tagmentation](#tagmentation)
- [Library Amplification](#library-amplification)
  - [Concentration of library](#concentration-of-library-and-agarose-gel-purification)
- [References](#references)

## Protocol

### Nuclei isolation

<aside>
<span class="timing">Timing: 2 h</span>

> <span class="critical">CRITICAL:</span> Keep everything cold and on ice at all times. Pre-cool tubes on ice before adding cells/nuclei. <br>

> <span class="critical">CRITICAL:</span> LoBind (DNA/RNA) microcentrifuge tubes are preferred for all steps in which they are used for collecting nuclei. <br>

</aside>
<aside>
Tiny-Sci (optional approach)

1. Samples should be no more than 2-3 mm in size, should be frozen individually in a microcentrifuge tube and kept on dry ice until lysis. The key to these small samples is to limit pipetting  and tube transfers that will leave behind precious nuclei.

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

12. Fill up the plate with more embryos or some other nuclei of which you have a lot and continue with the sci procedure at Step 24 of the reverse
transcription.

</aside>

1. Prepare two ice buckets with wet ice, a bucket with crushed dry ice to hold your frozen tissues, and a thick, flat slab of dry ice for smashing tissues. <br>
Pre-cool both a centrifuge that will hold 50-ml tubes and a microcentrifuge to 4°C.

2. Determine how much lysis buffer you will need for the tissue you will be processing. (For extremely small samples, skip to Box 1: Tiny-Sci.) An E13.5 mouse embryo (~200 mg) requires 5 ml of lysis buffer. An E16.5 embryo (~500 mg) will need 20 ml. An adult mouse heart needs 5 ml. Adult mouse kidneys need 5 ml per kidney. Adult mouse liver needs 20 ml. Adult mouse pancreas needs 15 ml. Adult tissues and tissues high in RNases will necessitate a bigger lysis volume. The buffer is inexpensive to make, so do not worry about using too much.

> <span class="caution">CAUTION:</span> DEPC is flammable and toxic. Avoid breathing vapors. The following steps should be performed in the chemical hood from this point until the DEPC is washed from the sample.

1. For every 1 ml of lysis buffer needed, add 2.5 μl of 10% (vol/vol) IGEPAL and 10 μl of DEPC to the hypotonic lysis buffer solution (and 40 μl of BSA if using lysis buffer B) and then vortex the solution to disperse the DEPC throughout. Have complete lysis buffer in a 50-ml tube for each sample on ice ready to go.

2. Fold a piece of aluminum foil four times so that you have a small pouch with eight layers of foil on each side. Place this on a slab of dry ice to chill.

3. Place your frozen tissue inside this foil and hold it firmly closed on the dry ice and smash it with a hammer (Fig. 4 and Supplementary Video 1). You want to be gentle enough not to tear the foil, but thorough enough to make a powder of the tissue. Do not let the tissue thaw.

4. Use the foil to guide your powdered tissue into the tube of the lysis buffer. It will stick a bit; pipette some of the lysis buffer from the tube to rinse the sample from the foil into the tube. Try to make sure that the sample is thawing only if it is in the lysis buffer.

5. Cap the 50-ml tube and shake it to disperse the chunks in the buffer. Let it sit on ice for 10 min. Triturate the chunks with a 1-ml pipette tip to help tease them apart a bit.

6. Set up another 50-ml tube on ice with a 40-μm cell strainer on top. Pour your lysate through that; there will still be a lot of chunks. Use a disposable pestle to coax the tissue through the filter. Do not worry about getting all of it through.

7. _Typically not necessary, DEPC kills everything_. Take a 45-μl sample of the filtered lysate and check for RNase activity with the IDT RNaseAlert kit. The RNaseAlert test will guide you on whether to proceed or not. There should not be any RNase detected, and if there is, you will have to restart with a new sample and adjust either the sample size or the volume of lysis buffer

8. While the RNaseAlert sample is incubating, spin down the remainder of the lysate (**1,000 g**, 3 min, 4°C).  Keep the nuclei in the 50-ml tube.  Resuspend the nuclei in 1 ml of 0.3 M SPBSTM with 10 μl of DEPC added (or more buffer if there are a lot of nuclei—roughly 1 ml of buffer per 200-500 mg of starting material at minimum).

## Nuclei/cell Fixation

<span class="timing">Timing 1 h</span>

1. For each sample, prepare fixative. In a 5-ml tube, add 100 μl of 50 mg/ml DSP stock solution to 4 ml of ice-cold methanol for every 1 ml of nuclei with which you are starting.

2. Add the prepared fixative gradually to the 50-ml tube containing the nuclei, swirling as you are adding it.

3. Fix on ice for 15 min, swirling occasionally.

> <span class="pause">PAUSE POINT</span> Fixed samples may be held here prior to rehydration. To pause, add 0.1 volume of 1 M glycine pH 8.5 or 1 M Tris pH 7.4 to quench DSP. Store at −80°C

4. Add 2 volumes of 0.3 M SPBSTM **_(or PBS-T if using cells)_** gradually, 2–3 ml at a time, swirling between additions to rehydrate the nuclei. For instance, with 1 ml of nuclei and 4 ml of fixative, you would need 10 ml of buffer to rehydrate.

5. Spin down the nuclei at **1,000 g** for 2 min at 4°C.

6. Carefully remove the supernatant and dispose properly. The nuclei pellet is at the bottom and should look a little white-ish from the DSP.

7. Resuspend the nuclei in ≥1 ml of 0.3 M SPBSTM **_(or PBS-T if using cells)_**. Triturate gently with a pipette tip to separate nuclei.

8. Divide fixed nuclei into aliquots of ~2 million nuclei (Fig. 5) in microcentrifuge tubes. Spin at **1,000 g** for 3 min at 4°C and remove and discard the supernatant.

9. (**Optional**) If continuing with the protocol the same day and there are obvious clumps at this point that will not tease apart, you will need to sonicate them to break them up. Sonicate (Diagenode Bioruptor Plus) on low intensity for 12 s only at 4°C. Spin and resuspend the nuclei in 500 μl of 0.3M SPBSTM (or PBS-T) as in Step 21.

## Reverse Transcription

<aside>
 <span class="timing">Timing: 2-3 h</span>
</aside>

Follow the chart below to determine how many starting nuclei you need and their volume.

| No. of cells           | 2,000,000 | 1,000,000 | 800,000 | 500,000 | 400,000 | 200,000 |
| ---------------------- | --------- | --------- | ------- | ------- | ------- | ------- |
| **No. of columns**     | 12        | 6         | 4       | 3       | 2       | 1       |
| **Nuclei volume (μl)** | 500       | 250       | 170     | 125     | 85      | 42.5    |
| **10 mM dNTP (μl)**    | 56        | 28        | 19      | 14      | 9.5     | 4.75    |

If you are dividing the plate among multiple samples, then the chart will outline the cell number you need depending on how many columns in the plate each sample will occupy. For example, if you will have two samples on one plate, each one will take six columns, you will need 1 million cells of each sample in a tube to start with in a volume of 250 μl each, and you will add 28 μl of dNTPs to each before distributing to their RT plate wells.

1. Resuspend an aliquot of frozen nuclei in 500 μl of 0.3 M SPBSTM to start and count. Dilute nuclei if necessary to get an accurate count.<br>
  _If nuclei are clumpy, sonicate (Diagenode Bioruptor Plus) on low intensity for 12 s only at 4°C.
  If there is still an excess of clumps, put the nuclei over a 40-μm Flow-mi pipette tip filter before counting.
  Use of a Flow-mi μlter is a last resort because it results in nuclei loss but is helpful if you have an excess of nuclei._
2. Pull out the desired amount of nuclei into a new tube and spin. Remove the supernatant and resuspend nuclei in the necessary volume of 0.3 M SPBSTM determined by the chart above and add the appropriate amount of dNTPs.
3. Distribute 5-μl aliquots of nuclei+dNTP mix to each well of the plate on ice.
4. Quickly spin RT primers (**plate 1**) (10 μM)
5. Add 2 μl of primer to each well. Do not pipette up and down to mix; just stir gently with the pipette tips.
6. Incubate the plate at 55°C for 5 min in a PCR machine (heated lid set to 65°C), then immediately place on ice or **4°C in the thermocycler**.
7. While this is incubating, make the reaction mix.<br>
  _We do not include dithiothreitol in this mix because it will undo the DSP cross-links (it is not necessary for the RT to work)._

| RT mix per plate                  | 1 well | x110 |
| --------------------------------- | ------ | ---- |
| 5× Superscript IV buffer (μl)     | 2      | 220  |
| Maxima RT H Minus (μl)            | 0.25   | 27.5 |
| Nuclease-free H<sub>2</sub>O (μl) | 0.75   | 82.5 |

**Do NOT use 5x Maxima buffer as it contains DTT**

8. Put 3 μl of reaction mix into each well (45 μl of mix × 8 in a strip tube for multichannel pipetting), stirring gently with tips.
  <br>The total volume per well is now 10 μl.
9. Incubate at 50°C for 30 min (heated lid at 65°C) and then immediately place on ice.
10. Ice plates until they are cold (>2 min).
11. Add 5 μl of cold 0.3 M SPBSTM per well.<br>
  _To maximize recovery, pool wells by using a 12-multichannel pipette with 200 μl tips to pipette gently up and down
  (the pipetting up and down is important to dislodge the nuclei, but try to avoid creating excessive bubbles)
  and combine each row of the plate into the bottom row. You can use the same tips for the whole plate.
  Collect these wells into two cold microcentrifuge tubes.
  (The solution will be bubbly, so it is difficult to squeeze into one tube.) although if you do it properly, one tube is enough (or use 2ml LoBind tubes)_
12. Spin at **1,000 g** for 3 min at 4°C. The pellet will be small, but you should be able to see it. Remove and discard the supernatant. **1,000 g** 1 min
13. Combine tubes and wash once more in 1 ml of cold 0.3 M SPBSTM. Spin at **1,000 g** for 3 min at 4°C.
Remove and discard the supernatant.

## Ligation

<aside>

<span class="timing">Timing: 1.5 h</span>

</aside>

| 4x Ligation master mix w/ 12% 1,2-propanediol | 200 μl |
| --------------------------------------------- | ------ |
| 10x T4 buffer                                 | 80 μl  |
| 1,2-propanediol                               | 96 μl  |
| T4 ligase                                     | 20 μl  |
| Nuclease-free H<sub>2</sub>O                  | 4 μl   |

> \*_Make and store at -20°C. Should not freeze._

1. Resuspend nuclei in 1,200 μl of 0.3 M SPBSTM.
2. Distribute 5 μl to each well of a new plate on ice.
3. Quick-spin the plate of **ligation primers (plate 2)** (10 μM).
4. Add 2 μl of primer to each well. Do not pipette up and down.
5. Add 2.5 μl of 4x ligation master mix to each well (45 μl of mix × 8 in a strip tube for multichannel pipetting), stirring gently with tips.<br>
  _The total volume per well is now 9.5 μl._
6. Incubate for 20 min at room temperature.
7. Ice plates until cold.
8. Add 10 μl of cold SPBSTM to each well. This helps keep the nuclei from clumping and allows for more nuclei to be recovered.
9. Pool wells by using a 12-multichannel to pipette gently up and down (the pipetting up and down is important to dislodge the nuclei) and combine each row of the plate into the bottom row. Then, collect these wells into two cold microcentrifuge tubes.
10. Spin at **1,000 g** for 1 min at 4°C. Remove and discard the supernatant.
11. Combine the two tubes and wash twice more with 1 ml of 0.3 M SPBSTM per wash.
12. Resuspend in 1 ml of 0.3 M SPBSTM to count.
  <br>If nuclei are clumpy and cannot be teased apart with gentle pipetting, sonicate on low intensity for 6 s only at 4°C and recount. Note that this is a shorter sonication step than before.

## Final distribution

<aside>

<span class="timing">Timing: 1 h</span>

</aside>

Sort if possible.

> <span class="critical">CRITICAL:</span>  In the final plate, you will want ~1,000 nuclei/well (or 4,000/well if you have scaled up the experiment to 384 × 384 × 384). You should have enough nuclei to freeze multiple plates if you like.

1. Make 400 μl of 1× second-strand synthesis buffer for each plate in the final distribution.
2. Spin down 100,000 nuclei for each plate desired for the final distribution. For each plate, resuspend in 400 μl of 1× second-strand synthesis buffer<br>
  _(400,000 per plate if this is a 384 × 384 × 384 experiment)._
3. Put 4 μl of nuclei into each well of a regular, not LoBind, plate on ice.
4. Cover with foil seals and freeze plates at -80°C or proceed with second-strand synthesis.

> <span class="pause">PAUSE POINT</span> Plates may be kept frozen at -80°C for &le;6 months.

## Second-strand synthesis

<aside>

<span class="timing">Timing: 3 h (or overnight)</span>

</aside>

1. Thaw plate on ice.
2. Make second-strand synthesis mix on ice as follows:

| Reaction mix per plate            | 1 well | ×140 |
| --------------------------------- | ------ | ---- |
| Nuclease-free H<sub>2</sub>O (μl) | 0.675  | 94.5 |
| Second-strand buffer (10×) (μl)   | 0.075  | 10.5 |
| Second-strand enzyme (20×) (μl)   | 0.25   | 35   |

3. Put 1 μl of second-strand synthesis mix into each well (17 μl of mix ×8 in a strip tube for multichannel pipetting).<br>
  _The total volume per well is now 5 μl._
4. Incubate for 2.5 h at 16°C in a PCR machine (no heated lid).

> <span class="pause">PAUSE POINT</span> Keep the plate at 4°C for &le;24 h.

## Protease Digestion

<aside>

<span class="timing">Timing: 2 h</span>

</aside>

1. Add 1 μl of protease to each well.

> <span class="critical">CRITICAL:</span> This is not proteinase K. Using Qiagen protease (cat. no 19157) is important because it can be heat-inactivated. See Reagent setup.

2. Incubate at 37°C for 40 min in a PCR machine (47°C heated lid).<br>
  _Usually not necessary_. Check 1 μl on a microscope: mix a 1-μl sample with 2 μl of diluted Yoyo-1 dye. **DAPI works as well if you have the cube**, put this on a slide and check on the GFP channel.
  You should see whisps of DNA instead of intact nuclei. If not, incubate for another 10 min before proceeding to heat inactivation.

3. Heat-inactivate the protease at 75°C for 20 min (85°C heated lid).

> <span class="critical">CRITICAL:</span> Do not lower this temperature and do not shorten this time. Qiagen lists different conditions for heat-inactivating their protease, but it is not sufficient. Put the plate on ice after inactivating.

> <span class="pause">PAUSE POINT</span> Store the plate at 4°C for &le;1 week.

## Tagmentation

<aside>

<span class="timing">Timing: 1h</span>

</aside>

1. On ice, make tagmentation mix as follows:

   | Reaction mix per plate            | 1well | x110   |
   | --------------------------------- | ----- | ------ |
   | 2x Tagment DNA buffer (μl)        | 2.5   | 275    |
   | Nuclease-free H<sub>2</sub>O (μl) | 2.375 | 262    |
   | N7-loaded Tn5 (μl)                | 0.125 | 13.75  |
   | Total (μl)                        | 5     | 550.75 |

2. On ice, add 5 μl of tagmentation mix to each well.<br>
  The total volume per well is now ~10-11 μl.
3. Incubate for 5 min at 55°C in a PCR machine (65°C heated lid).<br>
  _Do not put on ice afterwards;
  just keep on the bench at room temperature as you add the next reaction mix,
  or else the SDS will come out of solution at the next step._
4. Remove the transposases with this buffer (keep at room temperature):

   | Reaction mix per plate            | 1 well | x120 |
   | --------------------------------- | ------ | ---- |
   | 1% (wt/vol) SDS (μl)              | 0.4    | 48   |
   | BSA (μl)                          | 0.4    | 48   |
   | Nuclease-free H<sub>2</sub>O (μl) | 1.8    | 216  |
   | Total (μl)                        | 2.6    | 312  |

5. Add 2.6 μl to each well and mix (39 μl ×8 into a strip tube for multichannel pipetting).
6. Incubate for 15 min at 55°C in a PCR machine (65°C heated lid).
7. Quench SDS by adding 2 μl of 10% (vol/vol) Tween 20 to each well.

## Library Amplification

<aside>

<span class="timing">Timing 1h</span>
</aside>

1. Assemble the PCR master mix. PCR is done with 96 indexed P7 primers and 1 P5 primer. You can also add an optional index sequence on the P5 primer for multiplexing multiple plates. The primers are as follows: plate of 96 indexed PCR P7 primers <span class="sequence">(5'-CAAGCAGAAGACGGCATACGAGA T[PCR P7 index]GTCTCGTGGGCTCGG-3'</span>) and TruSeqP5 primer(s) <span class="sequence">(5'-AATGATACGGCGAC CACCGAGATCTACAC[PCR P5 index]ACACTCTTTCCCTACACGACGCTCTTCCGATCT-3'</span>).

| Reaction mix per plate            | 1 well | x110  |
| --------------------------------- | ------ | ----- |
| 2x NEBNext (μl)                   | 20     | 2,200 |
| TruSeqP5 primer(s) (μl)           | 0.2    | 22    |
| Nuclease-free H<sub>2</sub>O (μl) | 3.2    | 352   |
| Total (μl)                        | 23.4   | 2,574 |

2. Add 2 μl of indexed P7 primers (10 μM) to each well.
3. Add 23.4 μl of PCR master mix to each well.
4. Amplify in a PCR machine by using 16 cycles **withOUT** a pre-extension step in the following program:

   | Step | Temperature                 | Time  |
   | ---- | --------------------------- | ----- |
   | 1    | 98ºC                        | 30 s  |
   | 2    | 98ºC                        | 10 s  |
   | 3    | 63ºC                        | 30 s  |
   | 4    | 72ºC                        | 1 min |
   | 5    | go to Step 3, 15 more times |       |
   | 6    | 72ºC                        | 5 min |

5. Run 1.5 μl of a few wells on a 6% PAGE gel in TBE buffer at 200V for 30 min to check amplification. You should see a smear of products with primer-dimers underneath. We isolate a section of the smear centered on 400 bp.

### Concentration of library and agarose gel purification

1. Pool 3 μl of each well and do a 0.8× AMPure XP cleanup (230 μl of beads) by following the manufacturer's protocol.<br>
  _Save the remaining plate by covering with foil and storing at room temperature or at 4°C for &le;6 months, in case you need to redo cleanup or if you anticipate needing more library for a large NovaSeq run._
2. Wash the AMPure bead pellet twice gently with 70% (vol/vol) ethanol and elute the pool in 50 μl.
3. **Perform size selection with 0.6-0.8x SPRISelect beads or homemade beads. See 10x v3 protocol for details.**
4. Run the library on NextSeq (or NovaSeq depending on the final cell numbers or sequencing depth desired) by using standard primers:

## References

[^ref]
