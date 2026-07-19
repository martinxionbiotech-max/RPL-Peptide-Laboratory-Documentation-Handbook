---
title: Molecular Weight Glossary
category: Chemical Terms
keywords:
- molecular weight
- MW
- monoisotopic mass
- average mass
- peptide mass
---

# Molecular Weight

## Definition

Molecular weight (MW) is the sum of the atomic weights of all atoms in a peptide molecule, expressed in Daltons (Da). It is a fundamental identifier used to confirm peptide identity by mass spectrometry.

## Overview

The molecular weight of a peptide is calculated from its amino acid sequence plus any chemical modifications. It is the primary parameter measured by mass spectrometry to confirm identity.

## Technical Explanation

**Average vs. Monoisotopic Mass:**

| Type | Definition | Use |
|---|---|---|
| Average Mass | Weighted average of all natural isotopes | General reference |
| Monoisotopic Mass | Mass using the most abundant isotope of each element | MS peak assignment |

**Calculation:**
MW = Sum of residue masses + mass of terminal groups + mass of modifications

**Example:** For a peptide with sequence A-B-C:
- Sum individual amino acid residue masses (each residue mass = amino acid MW − 18 Da for water loss)
- Add H₂O at ends (18 Da)
- Add modification masses (if any)

**Impact of Counter-Ion:**
The molecular weight reported is typically the peptide free base or peptide salt, depending on convention. Always verify which form is being reported.

## Importance in Peptide Documentation

Theoretical and experimental (MS-observed) molecular weights are compared on the COA to confirm identity. A match within ±0.5 Da confirms correct peptide synthesis and modification.

## Related Terms

- [Mass Spectrometry](../analytical-terms/mass-spectrometry.md)
- [Identity](../analytical-terms/identity.md)
- [Counter-Ion](./counter-ion.md)
- [Molecular Formula](./molecular-formula.md)

## Frequently Asked Questions

**Q: What is the molecular weight range of research peptides?**
A: Most research peptides range from ~200 Da (dipeptides) to ~5000 Da (50-mers), though longer sequences are possible.

**Q: Why might observed and theoretical MW not match exactly?**
A: Differences can indicate incorrect sequence, incomplete or excessive modifications, counter-ion presence, or adduct formation (sodium, potassium) during MS analysis.
