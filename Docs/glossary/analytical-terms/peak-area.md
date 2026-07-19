---
title: Peak Area Glossary
category: Analytical Chemistry
keywords:
- peak area
- integration
- area normalization
- quantification
---

# Peak Area

## Definition

Peak area is the integrated area under a chromatographic peak, representing the total detector response for a separated compound. It is used for quantitative analysis in HPLC.

## Overview

In peptide purity analysis by HPLC, peak area is the primary quantitative measurement. The area of each peak correlates with the amount of that compound in the sample (assuming proportional detector response). Purity is calculated by comparing the main peak area to the total peak area.

## Technical Explanation

**Area Normalization Method:**
Purity (%) = (Area of main peak / Sum of areas of all peaks) × 100

**Integration Considerations:**
- Baseline selection: Proper baseline assignment is critical for accurate results
- Peak start/end points: Incorrect marking can over/underestimate area
- Shoulder peaks: Partially resolved peaks require proper deconvolution
- Minimum area threshold: Peaks below a set threshold (e.g., 0.05%) are not integrated

**Limitations:**
- Assumes equal detector response for all components (not always true)
- Does not account for non-UV-absorbing impurities
- Co-eluting impurities may hide within the main peak

## Importance in Peptide Documentation

The area normalization method is the standard approach for reporting peptide purity on COAs. Understanding its principles helps researchers correctly interpret purity values and their limitations.

## Related Terms

- [HPLC](./hplc.md)
- [Chromatogram](./chromatogram.md)
- [Purity](./purity.md)
- [Impurity](./impurity.md)

## Frequently Asked Questions

**Q: Can area normalization overestimate purity?**
A: Yes. If impurities do not absorb UV at the detection wavelength (e.g., some residual solvents), or if impurities co-elute with the main peak, the purity value may be overestimated. This is why complementary methods (LC-MS) are valuable.

**Q: What is a typical injection volume for peptide purity analysis?**
A: Typical injection volumes range from 5–50 µL, depending on sample concentration (usually 1–5 mg/mL), column dimensions, and detector sensitivity.
