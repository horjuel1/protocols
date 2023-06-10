---
title: MERFISH Prep
---

## MERFISH Prep

We use the [FCS 4](https://bioptechs.com/fcs-chamber-system/) chamber system to flow fluid over our sample.

## Silanization

The system uses [40 mm coverslips](https://bioptechs.com/product/40mmcoverslips/).
In order to embed our sample in polyacrylamide for either tissue clearing or expansion,
we need to functionalize the glass with an allyl group.

### Acid Etch

This is Method 1 from [@crasComparisonChemical1999]. The idea is to remove sodium and carbon atoms at the surface and expose silanol (Si-OH) groups on the glass surface by etching away the SiO2 layer followed by silanization [@a.schlechtFunctionalizationGlass2011].

1. In a fume hood, mix 1:1 HCl:MeOH in a glass beaker. [**Always add acid**](https://www.thoughtco.com/do-you-add-acid-to-water-608152) to methanol.
I typically make about 100 mL total.
2. Drop the coverslips one-by-one into the beaker in order to expose the surface to the acid. Use [PTFE tweezers](https://www.tedpella.com/Tweezers_html/pelco-pro.aspx) to avoid scratching the glass while preventing the tweezer itself from dissolving.
3. Incubate for 30 minutes with agitation to make sure that all surfaces are treated. You can use a sonicator (place the beaker into the sonicator, do not pour the acid), but I typically just swirl the beaker every 5 minutes or so.
4. Rinse the coverslips with DI water by picking out the coverslips from the acid solution.
The acid solution can be saved for later use (in a glass container not plastic).
5. Replace DI water and sonicate or swirl the coverslips until the pH of the water is close to neutral (pH > 6) using a pH paper.
6. Dehydrate the coverslips completely. Ideally, dry the coverslips under nitrogen for at least 1 hour. We do not have a nitrogen supply, I have been using a hybridization oven at 70°C with Kimwipes in the interior.

### Silanize

7. Silanize with 0.2% allyltrichlorosilane and 0.1% triethylamine (basic catalyst) in chloroform for 30 minutes. **Allyltrichlorosilane is highly reactive to water. Bring to RT before opening in the fume hood.**
8. Incubate for 30 minutes with agitation. I typically seal the beaker with aluminum foil and tape and use a shaker for this. Do not use Parafilm: it will dissolve in chloroform.
9. Rinse once with chloroform and then 2 times with ethanol.
10. Dry under nitrogen or in a 70°C oven for at least 1 hour.
11. Store desiccated "for weeks". I use a dessicator with silica beads from Amazon. Do not use a vacuum, the coverslip seems to crack over time.

To test for silanization, drop distilled water on to the coverslip.
If the water beads and slides off without residue when tilted, the silanization was successful.
Compare water behavior on a silanized and non-silanized coverslip.

It is also helpful to test the coverslip before using.
Coverslips stored under normal atmosphere for weeks lose their hydrophobicity.

### Optional: Poly-lysine Coating

1. If your cells need it, you can coat the coverslips with poly-lysine by dropping ~100 μl 0.01% lysine solution at the center of the coverslip inside a 60-mm dish.
Do not let the poly-lysine solution get between the coverslip and the dish, it will make it difficult to remove the coverslip.
2. Incubate for >1 hour at RT or 37°C. **NOT the cell culture incubator. That has 5% CO2 and will ruin the pH of your reaction**.
3. Wash thoroughly with sterile water. Free polynucleotides are toxic to cells.

Try to use the coverslips generated this way as soon as possible. Coating with poly-lysine seems to displace a lot of the allyl groups and can (has) result in the polyacrylamide gel not adhering to the coverslip. 3T3 cells seem fine without poly-lysine, HEK293T needs it.
