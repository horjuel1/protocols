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

The target is 2.4M cells/plate or 200,000 cells/column.

1. Resuspend an aliquot of frozen nuclei in 500 μl of 0.3 M SPBSTM to start and count. Dilute nuclei if necessary to get an accurate count.
  _If nuclei are clumpy, sonicate (Diagenode Bioruptor Plus) on low intensity for 12 s only at 4°C.
  If there is still an excess of clumps, put the nuclei over a 40-μm Flow-mi pipette tip filter before counting.
  Use of a Flow-mi filter is a last resort because it results in nuclei loss but is helpful if you have an excess of nuclei._

2. Bring predispensed primer plates out and quickly spin. There's 2 μl of primer in each well.
3. Set the thermal cycler up to be ready (lid at 65°C). (from ISAACC-Seq)
  | Step | Temperature                          | Time   |
  | ---- | ------------------------------------ | ------ |
  | 1    | 50°C                                 | 10 min |
  | 2    | 8°C                                  | 12  s  |
  | 3    | 15°C                                 | 45  s  |
  | 4    | 20°C                                 | 45  s  |
  | 5    | 30°C                                 | 30  s  |
  | 6    | 42°C                                 | 2  min |
  | 7    | 50°C                                 | 3  min |
  | 8    | 65°C                                 | 1 min  |
  |      | Go to step 3, 2 more times (3 total) |        |
  | 9    | 50 °C                                | 5 min  |

4. Setup the master mix. PEG is viscous and is slow to mix with water. Make sure that everything well mixed before proceeding.
    **Do NOT use 5x Maxima buffer** as it contains DTT (unless you used DSS then it's fine.)
    | RT mix per plate                  | 1 well | x100 |
    | --------------------------------- | ------ | ---- |
    | 5× Superscript IV buffer (μl)     | 2      | 200  |
    | dNTPs                             | 0.5    | 50   |
    | 50% PEG                           | 1.5    | 150  |
    | Maxima RT H Minus (μl)            | 0.25   | 25   |
    | RNaseIn Plus                      | 0.05   | 5    |
    | Nuclease-free H<sub>2</sub>O (μl) | 3.75   | 375  |

5. Pull out the desired amount of nuclei into a new tube and spin. Remove the supernatant and resuspend nuclei in the RT reaction mix.
6. Dispense 8 μl of reaction mix into each well (65 μl of mix × 8 in a strip tube for multichannel pipetting). Do not touch the bottom of the plate if you do not want to change tips.
7. Start the thermal cycler program.
8. Ice plates until they are cold (>2 min).
9. Add 9 μl of cold 0.3 M PBS-T per well. SPBSTM may cause pelleting issues here.
  _To maximize recovery, pool wells by using a 12-multichannel pipette with 200 μl tips to pipette gently up and down
  (the pipetting up and down is important to dislodge the nuclei, but try to avoid creating excessive bubbles)
  and combine each row of the plate into the bottom row. You can use the same tips for the whole plate.
  Collect these wells into two cold microcentrifuge tubes.
  (The solution will be bubbly, so it is difficult to squeeze into one tube, although if you do it properly, one tube is enough (or use 2 ml tubes))
10. Spin at **1,000 g** for 3 min at 4°C. The pellet will be small, but you should be able to see it. Remove and discard the supernatant.
11. Combine tubes and wash once more in 1 ml of cold 0.3 M SPBSTM. Spin at **1,000 g** for 3 min at 4°C.
Remove and discard the supernatant.

## Ligation

<span class="timing">Timing: 1.5 h</span>

1. Thaw and spin down the ligation primer plate.
2. Prepare the ligation mix on ice:

| Ligation mix  | 1 well | 100 wells |
| ------------- | ------ | --------- |
| 10x T4 buffer | 1.0 μl | 100 μl    |
| 50% PEG       | 1.5 μl | 150 μl    |
| 20 mg/ml BSA  | 0.5 μl |  50 μl    |
| T4 ligase     | 0.2 μl |  20 μl    |
| Water         | 4.8 μl | 480 μl    |

3. Resuspend nuclei in the ligation mix at 4°C
4. Distribute 8 μl to each well of a new plate on ice.
5. Re-cover the plate with seals, spin-down, vortex at 2,000 rpm for 10 s, and spin-down.
6. Incubate for 10 min at room temperature.
7. Ice plates until cold.
8. Add 10 μl of cold SPBSTM to each well. This helps keep the nuclei from clumping and allows for more nuclei to be recovered.
9. Pool wells by using a 12-multichannel to pipette gently up and down (the pipetting up and down is important to dislodge the nuclei) and combine each row of the plate into the bottom row. Then, collect these wells into two cold microcentrifuge tubes.
10. Spin at **1,000 g** for 3 min at 4°C. Remove and discard the supernatant.
11. Combine the two tubes and wash once more with 1 ml of 0.3 M SPBSTM per wash.

## Final distribution

<span class="timing">Timing: 1 h</span>

<span class="critical">CRITICAL:</span>  In the final plate, you will want ~1,000 nuclei/well. You should have enough nuclei to freeze multiple plates if you like.

1. Spin down and resuspend in PBS with 0.5% DNase-free BSA w/ 1:1000 RNaseIn and 0.1 μg/ml DAPI for sorting. **Do not use SPBSTM**, the nozzle will leak due to the presence of Triton.
2. Sort nuclei into a 1.5 ml tube coated with 100 μl SPBSTM.
3. Centrifuge at **1,000 g** for 3 min at 4°C. Resuspend in 1× second-strand buffer targeting 5 μl/well. Base is 1,000 cells/well with 1 ligation plate, increase the concentration as needed.
4. If proceeding, add the enzyme mix. We usually sort an extra plate with a few extra strip of tubes for diagnostics.
5. Cover with foil seals and freeze plates at -80°C or proceed with second-strand synthesis.

<span class="pause">PAUSE POINT</span> Plates may be kept frozen at -80°C for &le;6 months.

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
| Second-strand enzyme (20×) (μl)   |  0.25  | 35.0 |

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

2. Incubate at 37°C for 1 h and heat-inactivate the protease at 75°C for 20 min in a PCR machine (85°C heated lid).

> <span class="critical">CRITICAL:</span> Do not lower this temperature and do not shorten this time. Qiagen lists different conditions for heat-inactivating their protease, but it is not sufficient. Put the plate on ice after inactivating.

<span class="pause">PAUSE POINT</span> Store the plate at 4°C for &le;1 week.

## Tagmentation

<aside>

<span class="timing">Timing: 1 h</span>

</aside>

1. On ice, make tagmentation mix as follows: (the extra 25 μl is extra volume.)

   | Reaction mix per plate            | 1well | x100   |
   | --------------------------------- | ----- | ------ |
   | 2x Tagment DNA buffer (μl)        |  2.5  |  250   |
   | Nuclease-free H<sub>2</sub>O (μl) |  2.5  |  250   |
   | N7-loaded Tn5 (μl)                | 0.25  |   25   |

2. On ice, add 5 μl of tagmentation mix to each well.
   The total volume per well is now ~10-11 μl.
3. Incubate for 5 min at 55°C in a PCR machine, heat-inactivate the transposase at 80°C for 5 min (85°C heated lid) and ramp down to 4°C.
4. | Step | Temperature                 | Time  |
   | ---- | --------------------------- | ----- |
   | 1    | 50°C                        | 5 min |
   | 2    | 80°C                        | 5 min |
   | 3    |  4°C                        | 15 s  |

## Library Amplification

<span class="timing">Timing 1h</span>

1. Prepare the primer plate 2 μl of indexed P7 primers (10 μM) to each well.
2. Add 20 μl of 2× Takara Ex Premier PCR mix and 4 μl of nuclease-free water to each well. You can make a master mix for this.
   Vortex at 2,000 rpm for 10 s and spin down.
3. Amplify in a thermocycler by using 17 cycles **withOUT** a pre-extension step in the following program:
   | Step | Temperature                 | Time  |
   | ---- | --------------------------- | ----- |
   | 1    | 94°C                        | 1 min |
   | 2    | 98°C                        | 10 s  |
   | 3    | 63°C                        | 15 s  |
   | 4    | 68°C                        | 45 s  |
   | 5    | go to Step 3, 16 more times |       |
   | 6    | 68°C                        | 3 min |
   | 7    |  4°C                        |  ∞    |

5. Pick a few wells, **dilute the product 20-fold in DI** and run on a Tapestation D5000 HS assay to check for amplification.

### Concentration of library and agarose gel purification

1. Pool 5 μl of each well and do a 0.8× AMPure XP cleanup (230 μl of beads) by following the manufacturer's protocol.<br>
  _Save the remaining plate by covering with foil and storing at room temperature or at 4°C for &le;6 months, in case you need to redo cleanup or if you anticipate needing more library for a large NovaSeq run._
2. Wash the AMPure bead pellet twice gently with 70% (vol/vol) ethanol and elute the pool in 50 μl.
3. **Perform size selection with 0.55-0.8x SPRISelect beads or homemade beads. See 10x v3 protocol for details.**
4. Run the library on NextSeq (or NovaSeq depending on the final cell numbers or sequencing depth desired) by using standard primers. (34x10x10xremaining)

## References

[^ref]
