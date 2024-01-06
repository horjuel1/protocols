---
title: sci Protocol
subtitle: Modified sci-RNA-Seq3 protocol for single-cell/nucleus RNA-seq
date: Jan 6, 2024
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

## Reverse Transcription

<span class="timing">Timing: 2-3 h</span>

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
