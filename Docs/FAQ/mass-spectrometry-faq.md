---
title: Mass Spectrometry FAQ
document_id: RPL-FAQ-MS-001
document_type: FAQ
category: Analytical
version: 1.0
revision_date: July 2026
status: Current
publisher: RPL Peptide (Qingdao RPL Biotechnology Co., Ltd.)
keywords: mass spectrometry, LC-MS, ESI-TOF, MALDI-TOF, m/z, identity, peptide confirmation, peptide modifications
---

| Field | Value |
|-------|-------|
| **Document ID** | RPL-FAQ-MS-001 |
| **Document Type** | FAQ |
| **Category** | Analytical — Mass Spectrometry |
| **Publisher** | RPL Peptide (Qingdao RPL Biotechnology Co., Ltd.) |
| **Version** | 1.0 |
| **Revision Date** | July 2026 |
| **Status** | Current |
| **URL** | https://rplpeptides.com |

---

# Mass Spectrometry FAQ

## (1) MS Fundamentals

### Q1: What is mass spectrometry and why is it essential for peptide analysis?
**A:** Mass spectrometry (MS) is an analytical technique that measures the mass-to-charge ratio (m/z) of ions to determine the molecular weight of compounds. It is the gold standard for peptide **identity confirmation** because it provides direct evidence that the synthesized peptide has the correct molecular weight (and therefore the correct sequence).

While HPLC tells you **how pure** the sample is, MS tells you **what it actually is**. A sample could be 99% pure by HPLC but be the wrong peptide entirely — only MS can confirm identity.

### Q2: What is the difference between ESI-TOF and MALDI-TOF?
**A:** ESI (Electrospray Ionization) and MALDI (Matrix-Assisted Laser Desorption/Ionization) are two common ionization methods used with Time-of-Flight (TOF) mass analyzers:

| Feature | ESI-TOF | MALDI-TOF |
|---------|:-------:|:----------:|
| **Ionization method** | Liquid spray with high voltage | Laser desorption from matrix crystal |
| **Charge states** | Multiply charged ions (z = 2+ to 10+) | Predominantly singly charged (z = 1+) |
| **Mass range** | Moderate (up to ~100 kDa) | Very wide (up to ~500 kDa) |
| **Sample state** | Solution (online with HPLC) | Solid on target plate |
| **Mass accuracy** | Very high (±0.001–0.01 Da) | High (±0.01–0.1 Da) |
| **Coupling to HPLC** | Naturally online (LC-MS) | Offline only |
| **Advantage** | Better for complex mixtures; provides charge state series that aids deconvolution | Faster; tolerant of salts and buffers; simpler spectra |
| **Common use for peptides** | Primary method for QC identity confirmation | Quick mass checks; large protein analysis |

For routine peptide QC, **ESI-TOF** is preferred because it couples directly to HPLC (LC-MS), allowing simultaneous purity and identity assessment of each separated peak.

### Q3: What does m/z mean and how do I interpret it?
**A:** The m/z value is the **mass-to-charge ratio** of an ion — the ion's mass (in Daltons) divided by the number of charges it carries. In a mass spectrum:

**Example for a peptide with MW = 2000 Da:**
| Charge State | m/z Value | How It's Calculated |
|:------------:|:---------:|:--------------------|
| 1+ | 2001.0 | (2000 + 1H⁺) / 1 |
| 2+ | 1000.5 | (2000 + 2H⁺) / 2 |
| 3+ | 667.3 | (2000 + 3H⁺) / 3 |
| 4+ | 500.8 | (2000 + 4H⁺) / 4 |

ESI produces a **charge state envelope** — a series of peaks at different m/z values, all corresponding to the same peptide carrying different numbers of protons. Deconvolution software uses the spacing between adjacent charge states to calculate the **neutral molecular weight** (M, without any charges). The result is a deconvoluted spectrum showing a single peak at the true molecular weight.

### Q4: What does a good mass spectrum look like?
**A:** A high-quality mass spectrum for peptide identity confirmation should show:

- A clean **charge state series** (multiple evenly spaced peaks in ESI) or a single dominant peak (in MALDI)
- The deconvoluted spectrum should show **one major peak** at the expected molecular weight (±0.5 Da)
- **Minimal background noise** — a flat baseline between peaks
- **No unexpected adduct peaks** — sodium adducts (+22 Da), potassium adducts (+38 Da), or TFA adducts (+114 Da) should be minimal
- **Sufficient signal intensity** — the main peak(s) should be at least 10× the baseline noise

For example, a clean deconvoluted spectrum for BPC-157 (calculated MW 1419.53 Da) should show one dominant peak at approximately 1419.5–1419.7 Da.

### Q5: What mass accuracy is needed for identity confirmation of peptides?
**A:** For most research peptides (MW 500–5000 Da), a mass accuracy of **±0.5 Da** between the expected (calculated) and observed (measured) molecular weight is considered sufficient for identity confirmation.

| Mass Accuracy | Confidence Level | Typical Instrument |
|:------------:|:----------------:|:------------------|
| ±0.5 Da | Standard QC acceptance | Single quadrupole or unit-resolution MS |
| ±0.1 Da | Good confidence | Quadrupole-TOF, high-resolution |
| ±0.01 Da | High confidence | Q-TOF, Orbitrap |
| ±0.001 Da | Definitive identity confirmation | FT-ICR, high-resolution Orbitrap |

At ±0.5 Da, most single-residue errors (e.g., Gly vs. Ala = +14 Da, Val vs. Leu = +14 Da — actually isomeric) or common modifications (+16 Da for Met oxidation) are easily detected. RPL Peptide uses ±0.5 Da as the standard specification for identity confirmation on all COAs.

## (2) LC-MS for Peptide Analysis

### Q6: What is LC-MS and how is it different from HPLC alone?
**A:** LC-MS (Liquid Chromatography-Mass Spectrometry) couples an HPLC separation directly to a mass spectrometer. The HPLC separates sample components by retention time, and as each component elutes, it is ionized and analyzed by the mass spectrometer.

**Advantages of LC-MS over HPLC alone:**

| Capability | HPLC Alone | LC-MS |
|------------|:----------:|:-----:|
| Purity (area %) | Yes | Yes |
| Identity confirmation | No (retention time only) | Yes (molecular weight) |
| Impurity identification | No | Yes (mass of each impurity peak) |
| Co-eluting peak resolution | No | Yes (different masses) |
| Modification detection | No | Yes (mass shifts) |
| Sensitivity for trace impurities | Moderate | High (selected ion monitoring) |

For comprehensive peptide quality assessment, LC-MS provides both separation and identification in a single analysis — making it superior for impurity characterization while HPLC-UV remains the quantitative standard for purity reporting.

### Q7: How does LC-MS detect and identify impurities that HPLC might miss?
**A:** LC-MS can detect impurities that HPLC alone may miss in several ways:

- **Co-eluting impurities:** Two compounds eluting at the same retention time on HPLC appear as one peak. LC-MS separates them in the mass dimension — each compound has a distinct m/z. For example, a co-eluting deletion peptide (−1 amino acid = mass shift of −57 to −186 Da) would be invisible on HPLC but clearly distinguishable on MS.

- **Non-UV-absorbing impurities:** Some impurities may not absorb UV at 214 nm (e.g., certain residual solvents, some non-peptide species). MS detects all ionizable species regardless of UV absorbance.

- **Trace-level detection:** MS can detect and identify impurities at levels well below the HPLC UV detection limit (down to parts-per-million in some modes).

- **Targeted impurity search:** By using extracted ion chromatograms (EIC), analysts can search for specific masses corresponding to known impurities, even if they are hidden under the main peak.

### Q8: What is the Total Ion Chromatogram (TIC) and how does it relate to the UV chromatogram?
**A:** In LC-MS analysis, the **Total Ion Chromatogram (TIC)** is analogous to the UV chromatogram but uses ion current as the signal:

| Feature | UV Chromatogram | TIC (MS) |
|---------|:---------------:|:---------:|
| Y-axis signal | Absorbance (mAU) | Total ion current |
| Detects | UV-absorbing compounds | All ionizable compounds |
| Response linearity | Highly linear | Can vary by compound |
| Signal-to-noise | Excellent | Good (depends on ionization efficiency) |
| Information provided | Quantitation (peak area) | Qualification (m/z per peak) |

The UV chromatogram is the primary tool for **quantitative purity assessment** because UV response is more linear across different peptides. The TIC provides **qualitative identity data** — each peak's mass spectrum confirms what it is. When reviewing an LC-MS report, compare the UV chromatogram with the TIC to ensure the main peak in the UV trace corresponds to the expected mass in the MS.

### Q9: What is MS/MS and when is it used for peptide analysis?
**A:** MS/MS (tandem mass spectrometry) involves selecting a specific ion (the precursor), fragmenting it by collision with an inert gas, and analyzing the resulting fragment ions. This provides **structural information** about the peptide:

| Application | What MS/MS Reveals |
|-------------|-------------------|
| Sequence confirmation | Fragment ion series (b- and y-ions) confirm the amino acid sequence |
| Modification site location | Mass shifts on specific fragments pinpoint the modified residue |
| Disulfide bond mapping | Fragmentation patterns identify linked cysteine residues |
| Impurity structure | Fragment masses help identify the exact structure of unknown impurities |

For routine peptide QC, single-stage MS (MS¹) is sufficient for identity confirmation. MS/MS is typically reserved for:
- Characterizing unknown impurities found during development
- Confirming site-specific modifications
- Detailed structural analysis of complex peptides (disulfide-rich, cyclic)

## (3) Identity Confirmation

### Q10: How does mass spectrometry confirm peptide identity?
**A:** Identity confirmation by MS follows a systematic workflow:

1. **Calculate theoretical mass:** The expected monoisotopic or average molecular weight is calculated from the amino acid sequence. For a generic 15-mer, this might be 1847.92 Da.

2. **Acquire the mass spectrum:** The sample is analyzed by LC-MS (typically ESI-TOF in positive mode), producing a charge state envelope of multiply charged ions.

3. **Deconvolute the spectrum:** Software converts the m/z series into a single neutral mass value. For the example above, the observed value might be 1847.85 Da.

4. **Compare observed vs. expected:** The difference is calculated: 1847.85 − 1847.92 = −0.07 Da. This falls within the ±0.5 Da specification.

5. **Confirm with supporting evidence:** The retention time on HPLC should be consistent with known behavior, and the impurity profile should match expectations for the specific peptide.

If the mass difference exceeds ±0.5 Da, the identity is **not confirmed**. The batch should be investigated for sequence errors, modifications, or labeling issues.

### Q11: How does MS detect modifications (acetylation, amidation, oxidation)?
**A:** MS detects modifications by the **mass shift** they produce relative to the unmodified peptide:

| Modification | Mass Shift (Da) | Common Positions |
|-------------|:---------------:|:-----------------|
| **Acetylation** | +42.01 | N-terminus, Lys side chain |
| **Amidation** | −0.98 (vs. free acid) | C-terminus (common for bioactive peptides) |
| **Oxidation (Met → sulfoxide)** | +15.99 | Methionine |
| **Oxidation (Trp → kynurenine)** | +3.99 | Tryptophan |
| **Oxidation (Cys → cysteic acid)** | +47.98 | Cysteine |
| **Deamidation (Asn → Asp)** | +0.98 | Asparagine |
| **Phosphorylation** | +79.97 | Ser, Thr, Tyr |
| **Pyroglutamate formation** | −17.03 | N-terminal Gln or Glu |

For example, if a peptide with expected mass 1500.00 Da shows an observed mass of 1515.99 Da, the +15.99 Da shift suggests **methionine oxidation**. If the shift is +42.01 Da, it indicates **N-terminal acetylation**. The magnitude of the shift tells you both the presence and type of modification.

Peptides with multiple basic residues may also show adducts with TFA (+114 Da, from the HPLC mobile phase) or sodium (+22 Da, from glassware or buffers). These adducts are non-covalent and generally do not indicate a modification of the peptide itself.

### Q12: Can a peptide pass HPLC purity but fail MS identity?
**A:** Yes, and this is exactly why both tests are required. Consider these scenarios:

- **Wrong peptide:** A sample could be synthesized with an incorrect amino acid at one position (e.g., Ala instead of Gly, +14 Da). It might purify to ≥98% as a single peak on HPLC — but MS would reveal the mass shift of +14 Da, failing identity confirmation.

- **Missing modification:** A peptide specified with C-terminal amidation (required for biological activity) might be synthesized as the free acid (mass shift of −0.98 Da). HPLC purity would be high, but MS would detect the mass discrepancy.

- **Sequence truncation with similar retention:** A truncated peptide that happens to have similar hydrophobicity to the full-length target might co-elute or elute very close. HPLC alone would show a single peak, but MS would detect two masses.

This is why RPL Peptide provides **both HPLC purity data and LC-MS identity confirmation** on every batch COA.

### Q13: What is the deconvolution process and why is it necessary for ESI spectra?
**A:** ESI produces multiply charged ions, creating a spectrum with several peaks at different m/z values, all corresponding to the same peptide molecule with different numbers of attached protons. **Deconvolution** is the mathematical process that converts this charge state series into the neutral molecular weight (M).

**Why deconvolution is necessary:**
- The raw ESI spectrum shows peaks at m/z 1001.5, 751.4, 601.3, 501.3, etc. — none of which directly reads as the molecular weight
- Deconvolution uses the spacing between adjacent charge states to determine the charge of each peak and calculate the neutral mass
- The result is a single, clear peak at the actual molecular weight (e.g., 2001.0 Da)

**Before deconvolution:** A series of multiply charged peaks (hard to read directly)
**After deconvolution:** One clean peak at the neutral molecular weight (the number that matters)

Deconvolution is automated in modern LC-MS software and does not require manual calculation. However, understanding the process helps when reviewing mass spectra that may show ambiguous or overlapping charge state series.

### Q14: What should I check when reviewing an LC-MS spectrum on a COA?
**A:** When reviewing the LC-MS data on a Certificate of Analysis, check these key elements:

1. **Deconvoluted mass:** Does the observed mass match the calculated mass within ±0.5 Da?
2. **Charge state series:** Is there a clean, evenly spaced series of multiply charged peaks in the raw spectrum?
3. **Single dominant peak:** Does the deconvoluted spectrum show one major peak? Multiple peaks indicate a mixture.
4. **Sodium/potassium adducts:** Are there small peaks at +22 Da and +38 Da from the main peak? A few are acceptable; large adduct peaks suggest sample contamination.
5. **Signal intensity:** Is the signal-to-noise ratio adequate (≥10:1)?
6. **Instrument and method:** Is the ionization method (ESI, MALDI) and mass analyzer (TOF, Quadrupole) specified?

If any of these are unclear or missing, request clarification from the supplier. The mass spectrum should be interpretable at a glance — clean, well-labeled, and obviously consistent with the expected product.

---

## Revision History

| Version | Date | Author | Changes |
|:-------:|:----:|--------|---------|
| 1.0 | July 2026 | RPL Peptide Quality | Initial release |

---

© 2026 RPL Peptide

rplpeptides.com
