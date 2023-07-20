---
title: Maleimide conjugation
---

# Maleimide antibody conjugation

# Maleimide-mTz-TCO-NHS conjugation

Based on

- [Fluidigm MaxPar conjugation kit](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6687300/)
- [Polymer-Based Elemental Tags for Sensitive Bioassays](https://onlinelibrary.wiley.com/doi/full/10.1002/anie.200700796)
- [CODEX multiplexed tissue imaging with DNA-conjugated antibodies](https://www.nature.com/articles/s41596-021-00556-8)
- [CITE-seq Hyper Antibody-Oligo Conjugation](https://citeseq.files.wordpress.com/2019/03/cite-seq_hyper_conjugation_190321.pdf)

**Equilibrate all moisture-sensitive reagents to room temperature before opening to avoid condensation.**

Column
- [Amicon Ultra 0.5 50 kDa](https://www.emdmillipore.com/US/en/product/Amicon-Ultra-0.5-Centrifugal-Filter-Unit,MM_NF-UFC505096) Regenerated cellulose membrane
- [Vivaspin 500 50 kDa](https://www.sartorius.com/shop/ww/en/usd/applications-laboratory-filtration-ultrafiltration/vivaspin-500%2C-50%2C000-mwco-pes%2C-25pc/p/VS0131) PES membrane, should work as well.

Reagents

- [mTz-PEG4-maleimide](https://clickchemistrytools.com/product/methyltetrazine-peg4-maleimide/)
- Tris-EDTA 100 mM Tris-HCl pH 7.2 2.5 mM EDTA
  - Need high buffering capacity for the reduction reaction. EDTA chelates divalent cations to reduce oxidation.
- TBS: 20 mM Tris-HCl pH 7.0 150 mM NaCl
  - Maleimide reactions prefer sulfhydryls over amines at lower pH (pH 6.5-7.5).
- High-salt PBS: PBS + 1.0M NaCl

Stock concentration

- 20 mM mTz-PEG4-maleimide. Dissolve 10 mg in 970 μl anhydrous DMSO. **Maleimide hydrolyzes in alkaline solution**.
  - Dilute 5-fold in DMSO to 4 mM for working concentration.

For 100 μg = 0.67 nmol IgG.

1. Partially reduce antibody

   - Prepare fresh 4 mM TCEP solution from 0.5 M stock. (2 μl of 0.5 M to 8 μl Tris-EDTA, then 4 μl + 96 μl Tris-EDTA)
   - Buffer exchange into Buffer R with a 50 kDa filtration unit. Centrifuge at 14,000g for 4 minutes (can be more).
     Volume should not exceed 20 μl after spin.
   - Add 100 μl of 4 mM TCEP to the filtered antibody inside the column and mix by pipetting.
   - Incubate at 37°C in a **water bath** for **exactly 30 min**.
   - Wash with TBS 3 times (400 μl). [TCEP](https://www.thermofisher.com/document-connect/document-connect.html?url=https://assets.thermofisher.com/TFS-Assets%2FLSG%2Fmanuals%2FMAN0011306_TCEP_HCl_UG.pdf) can reduce conjugation yield but this is not as bad as DTT.

2. Conjugate with mTz-PEG4-maleimide

   - Use 10-fold molar excess of mTz-PEG4-maleimide. Final concentration is 66.7 μM.
     Use 1.675 μl from 4 mM working concentration and 78.325 μl TBS and add directly to antibody in the column.
   - Incubate at 37°C in a water bath for 90 min.
   - Wash in TBS and wash 3 times in BBS pH 8.5. (Maleimide-thiol conjugates can undergo a reverse reaction.
     Hydrolysis of maleimide in an alkaline solution prevents this.
     [Mild Method for Succinimide Hydrolysis on ADCs: Impact on ADC Potency, Stability, Exposure, and Efficacy](https://pubs.acs.org/doi/10.1021/bc500357n)
     ![Michael addition of the thiol to the maleimide results in the maleimide-thiol conjugate, the thiosuccinimide.
The reaction is fast, but the conjugate is relatively unstable and can undergo further reaction via one of two pathways:
(i) it can undergo irreversible ring-opening hydrolysis to yield a stable hydrolyzate (succinamic acid thioether),
which prevents elimination of the maleimide-thiol conjugate;
(ii) it can undergo a retro-Michael conversion back to the starting thiol and maleimide.](https://user-images.githubusercontent.com/34997334/197348174-238a272f-f142-4184-953f-89e55029aa14.png)
   - The concentrated antibody should have a slight pinkish hue from the methyltetrazine.

3. Conjugate with TCO-labelled oligo
   - Mix with 3 nmol of oligo for a conjugation ratio of 5:1. Incubate at room temperature O/N. Probably overkill but at least this opens more of our maleimide ring.
   - Wash with High-salt PBS 4 times (tested oligo retention in high-salt PBS in a 50 kDa unit, undetectable after 3 washes).
   - Wash last time with PBS.
   - Flip the centrifugation unit into a new tube and centrifuge at 1,000g for 2 min to elute.
   - Quantify with BCA.
