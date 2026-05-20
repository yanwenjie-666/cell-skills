# Cell Press Figure Specifications — Detailed Reference

## Source
Based on Cell Press Author Guidelines (2024–2025) and "Information for Authors" documents from Cell, Molecular Cell, Cell Reports, and other Cell Press journals.

## Figure Dimensions

### Page Layout
- Cell Press journals use a two-column layout
- Full page text width: 17.4 cm (6.85 inches)
- Single column width: 8.5 cm (3.35 inches)
- 1.5 column width: ~11.4 cm (4.49 inches)
- Maximum figure height: 23.5 cm (9.25 inches)

### Recommended Aspect Ratios
- Standard single panel: 8.5 × 8.5 cm (square)
- Full-width multi-panel: 17.4 × 10–15 cm
- Vertical multi-panel: 8.5 × 20 cm (single column, tall)

## Resolution Requirements

| Figure Type | Minimum DPI | Recommended DPI |
|-------------|-------------|-----------------|
| Line art (diagrams, schematics) | 600 | 1000 |
| Halftones (photos, gels, microscopy) | 300 | 600 |
| Combination (lines + halftone) | 600 | 600 |
| Color photographs | 300 | 300 |

## Font Specifications

### Allowed Fonts
- **Primary**: Arial
- **Alternative**: Helvetica
- **Specialty**: Symbol font for Greek letters only if needed
- **NOT allowed**: Times New Roman, Courier, decorative fonts

### Size Rules
- All text must be legible at final print size
- Minimum: 6 pt after scaling
- Recommended body text in figure: 7 pt
- Panel labels: 8–10 pt, bold
- Axis labels: 7–8 pt
- Tick labels: 6–7 pt

## Color Guidelines

### Colorblind Safety
Cell Press requires all figures to be interpretable by readers with color vision deficiency (~8% of males). Recommendations:

1. **Never use red-green contrast alone** to convey information
2. Use **shape + color** for scatter plots
3. Use **pattern + color** for bar charts when possible
4. Test with colorblind simulators (e.g., Coblis, Color Oracle)

### Recommended Palettes
- **Okabe-Ito** (8 colors): #000000, #E69F00, #56B4E9, #009E73, #F0E442, #0072B2, #D55E00, #CC79A7
- **Viridis** family (continuous): viridis, plasma, inferno, magma
- **ColorBrewer** qualitative sets: Set2, Dark2, Paired

### Color Encoding Conventions
- **Heatmaps**: Blue-white-red (diverging) or viridis (sequential)
- **Up/Down regulation**: Blue (down) / Red (up) — must be defined in legend
- **Significance**: Grayscale or single accent color for highlighted data

## Panel Labels

### Format
- **Style**: Uppercase, bold, sans-serif (Arial)
- **Position**: Top-left corner of each panel, outside the plot area
- **Size**: 8–10 pt bold
- **Sequence**: A, B, C, D, E, F... (single letter; use A', A'' for related sub-panels only if necessary)

### What NOT to do
- ❌ Lowercase labels (a, b, c)
- ❌ Parenthesized labels ((A), (B))
- ❌ Labels inside plot area overlapping data
- ❌ Inconsistent positioning across panels

## Statistical Annotations

### Error Bars (define in legend)
- **SD**: Standard deviation (for showing spread of data)
- **SEM**: Standard error of the mean (for showing precision of mean estimate)
- **95% CI**: Confidence interval (for showing range of plausible true values)
- Always state: "Error bars represent [SD/SEM/95% CI], n = X [biological/technical replicates]"

### Significance Notation
| Symbol | p-value range |
|--------|--------------|
| ns | p ≥ 0.05 |
| * | p < 0.05 |
| ** | p < 0.01 |
| *** | p < 0.001 |
| **** | p < 0.0001 |

### Required Statistical Information
- Name of statistical test
- Whether test is one-tailed or two-tailed
- Exact p-values when possible (not just significance stars)
- Multiple comparison correction method if applicable
- n for each group

## Special Figure Types

### Western Blots / Gel Images
- Cropped blots acceptable but must show molecular weight markers
- Full uncropped blots in supplementary (required)
- Brightness/contrast adjustments must be applied to entire image uniformly
- No nonlinear adjustments (gamma correction) unless stated
- Lanes from different gels must NOT be spliced together without clear indication (dividing line)

### Microscopy Images
- Scale bar required in every panel (bottom-right preferred)
- State objective lens and magnification in legend
- If pseudo-colored, state original channel and lookup table
- Any image processing must be described in STAR Methods
- Processing applied uniformly to entire field of view

### Flow Cytometry
- Full gating strategy in supplementary
- Percentage in each gate visible
- Axis labels: protein name and fluorochrome (e.g., "CD4 PE-Cy7")
- Sequential gates shown in logical order

### Survival Curves (Kaplan-Meier)
- Number at risk shown below plot at regular intervals
- Censoring events marked as tick marks
- Hazard ratio, 95% CI, and p-value stated
- Log-rank test (or specified alternative)

### Genomic Data Tracks
- Consistent scale across compared tracks
- Y-axis range stated
- Gene models shown below
- Peak calls or significant regions highlighted

## Multi-Panel Figure Assembly

### Tools
- Adobe Illustrator (industry standard)
- Inkscape (free, open source)
- Python: matplotlib with GridSpec
- R: cowplot::plot_grid() or patchwork

### Assembly Guidelines
1. Export individual panels as vector (PDF) or high-res raster (TIFF)
2. Assemble in vector editor for precise alignment
3. Maintain consistent spacing (2–4 mm between panels)
4. Ensure panel labels don't overlap figure elements
5. Save final composite as PDF (vector) or TIFF (300+ DPI raster)

## Supplementary Figure Standards
- Same quality as main figures
- Label: "Figure S1" (not "Supplementary Figure 1" or "Supp Fig 1")
- Can span multiple pages
- Must be cited in main text: "(Figure S1A)"
- Legend in same document as the figure

## Common Rejection Reasons (Figure-Related)
1. Resolution too low (< 300 DPI)
2. Text illegible at print size (< 6 pt)
3. Red-green color scheme without alternative encoding
4. Missing scale bars on microscopy
5. Error bars undefined in legend
6. Spliced gel lanes without clear demarcation
7. Missing statistical test details
8. Panel labels inconsistent or missing
9. Figure too large (exceeds 17.4 cm width)
10. Wrong file format (JPEG instead of TIFF/PDF)
