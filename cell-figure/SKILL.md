# cell-figure

## Description

You are an expert in creating publication-quality figures for Cell Press journals (Cell, Molecular Cell, Cell Stem Cell, Cell Reports, Cell Systems, Cell Chemical Biology, Cell Host & Microbe, Immunity, Neuron, Developmental Cell, Current Biology). You produce figures that strictly conform to Cell Press visual and technical standards.

## Cell Press Figure Specifications

### Dimensions and Resolution
- **Maximum width**: 17.4 cm (full page) or 8.5 cm (single column)
- **Resolution**: 300 DPI minimum for photographs; 600 DPI for line art; 300-600 DPI for combination figures
- **File formats**: PDF (preferred for vector), EPS, TIFF (for raster). Do NOT submit JPEG for final figures.
- **Color mode**: RGB for online; CMYK for print (Cell Press handles conversion)
- **Maximum file size**: 20 MB per figure

### Font Requirements
- **Font family**: Arial or Helvetica (sans-serif only)
- **Minimum font size**: 6 pt (after reduction to final print size)
- **Recommended font size**: 7–10 pt for panel labels; 6–8 pt for axis labels
- **Panel labels**: Uppercase bold letters (A, B, C, D...) — NOT lowercase, NOT parenthesized
- **Consistency**: Same font size and style throughout all panels of a figure

### Color Standards
- **Accessibility**: All figures must be interpretable by colorblind readers
- **Avoid**: Red-green combinations without additional distinguishing features (patterns, shapes)
- **Preferred palettes**: Use colorblind-safe palettes (e.g., Okabe-Ito, viridis, ColorBrewer)
- **Background**: White preferred; avoid gray backgrounds on plots
- **Scale bars**: Required for all microscopy and imaging data (state units in legend)

### Panel Organization
- **Layout**: Panels arranged in logical reading order (left-to-right, top-to-bottom)
- **Spacing**: Consistent spacing between panels (recommended 2–4 mm)
- **Alignment**: All panels aligned to grid; no ragged edges
- **White space**: Minimal but sufficient for clarity
- **Grouping**: Related panels grouped visually; conceptual flow matches narrative

### Statistical Displays
- **Error bars**: Must be defined in figure legend (SD, SEM, CI — specify n)
- **Significance markers**: Use standard notation (ns, *, **, ***, ****) with p-value thresholds defined in legend
- **Individual data points**: Show individual data points overlaid on bar/box plots when n < 20
- **Box plots**: Preferred over bar charts for distributions; show median, quartiles, whiskers
- **Sample size**: Always state n in the figure legend

## Workflow

1. **Assess the data type**: Determine appropriate visualization (scatter, bar, heatmap, micrograph composite, schematic, etc.)
2. **Plan panel layout**: Design grid arrangement matching the narrative flow in Results
3. **Apply Cell Press specifications**: Set dimensions, fonts, colors, resolution per the rules above
4. **Generate code or instructions**: Provide Python (matplotlib/seaborn), R (ggplot2), or Illustrator instructions
5. **Add statistical annotations**: Include error bars, significance markers, sample sizes
6. **Validate accessibility**: Check colorblind safety, font legibility at reduced size
7. **Format for submission**: Ensure correct file format, resolution, and naming convention

## Figure Legend Rules (Cell Press)

Figure legends in Cell Press journals follow a specific structure:

```
Figure N. Title (bold, single sentence describing the key conclusion)
(A) Description of panel A. Include sample sizes, statistical tests, and what error bars represent.
(B) Description of panel B.
...
Scale bars: X μm. Error bars represent mean ± SEM (n = X biological replicates).
See also Figure SX and Table SX.
```

### Legend Requirements
- **Title**: One sentence, states the main finding (not a description)
- **Panel descriptions**: Brief, informative; define all abbreviations on first use
- **Statistical info**: Test used, p-values, n, what error bars represent
- **Cross-references**: "See also" references to supplementary figures/tables
- **No methods**: Legends should NOT contain detailed methods (those go in STAR Methods)
- **Length**: Concise; typically 50–150 words per figure

## Supplementary Figures

- Label as "Figure S1, S2..." (not "Supplementary Figure 1")
- Same quality standards as main figures
- Can be multi-page
- Must be referenced from main text with "See also Figure SX"
- Legend format identical to main figures

## Python Code Template

```python
import matplotlib.pyplot as plt
import matplotlib as mpl
import seaborn as sns
import numpy as np

# Cell Press figure setup
def setup_cell_press_style():
    """Configure matplotlib for Cell Press publication figures."""
    plt.rcParams.update({
        'font.family': 'Arial',
        'font.size': 7,
        'axes.labelsize': 8,
        'axes.titlesize': 8,
        'xtick.labelsize': 7,
        'ytick.labelsize': 7,
        'legend.fontsize': 7,
        'figure.dpi': 300,
        'savefig.dpi': 300,
        'axes.linewidth': 0.5,
        'xtick.major.width': 0.5,
        'ytick.major.width': 0.5,
        'xtick.major.size': 3,
        'ytick.major.size': 3,
        'lines.linewidth': 1.0,
        'axes.spines.top': False,
        'axes.spines.right': False,
    })

# Figure sizes (in inches, converted from cm)
CELL_FULL_WIDTH = 17.4 / 2.54  # ~6.85 inches
CELL_SINGLE_COL = 8.5 / 2.54   # ~3.35 inches
CELL_1_5_COL = 11.4 / 2.54     # ~4.49 inches

# Colorblind-safe palette (Okabe-Ito)
CELL_COLORS = [
    '#0072B2',  # blue
    '#D55E00',  # vermilion
    '#009E73',  # green
    '#CC79A7',  # pink
    '#F0E442',  # yellow
    '#56B4E9',  # sky blue
    '#E69F00',  # orange
    '#000000',  # black
]

def add_panel_label(ax, label, x=-0.15, y=1.05):
    """Add Cell Press style panel label (uppercase bold)."""
    ax.text(x, y, label, transform=ax.transAxes,
            fontsize=10, fontweight='bold', va='top', ha='left')

def add_significance(ax, x1, x2, y, p_value):
    """Add significance bracket and stars."""
    if p_value < 0.0001:
        sig = '****'
    elif p_value < 0.001:
        sig = '***'
    elif p_value < 0.01:
        sig = '**'
    elif p_value < 0.05:
        sig = '*'
    else:
        sig = 'ns'
    
    ax.plot([x1, x1, x2, x2], [y, y+0.02, y+0.02, y], 'k-', lw=0.5)
    ax.text((x1+x2)/2, y+0.02, sig, ha='center', va='bottom', fontsize=7)
```

## R Code Template

```r
library(ggplot2)
library(cowplot)

# Cell Press theme for ggplot2
theme_cell_press <- function(base_size = 7, base_family = "Arial") {
  theme_classic(base_size = base_size, base_family = base_family) %+replace%
    theme(
      axis.line = element_line(size = 0.3, color = "black"),
      axis.ticks = element_line(size = 0.3, color = "black"),
      axis.text = element_text(size = base_size, color = "black"),
      axis.title = element_text(size = base_size + 1),
      legend.text = element_text(size = base_size),
      legend.title = element_text(size = base_size + 1),
      strip.text = element_text(size = base_size + 1, face = "bold"),
      strip.background = element_blank(),
      panel.grid = element_blank(),
      plot.title = element_text(size = base_size + 2, face = "bold", hjust = 0)
    )
}

# Cell Press dimensions
cell_full_width <- 17.4  # cm
cell_single_col <- 8.5   # cm

# Colorblind-safe palette
cell_colors <- c("#0072B2", "#D55E00", "#009E73", "#CC79A7",
                 "#F0E442", "#56B4E9", "#E69F00", "#000000")

# Save figure with Cell Press specs
save_cell_figure <- function(plot, filename, width = 17.4, height = 10, units = "cm") {
  ggsave(filename, plot, width = width, height = height, units = units, dpi = 300)
}
```

## Common Figure Types and Guidelines

### Gel/Blot Images
- Show full uncropped blot in supplementary
- Mark molecular weight markers
- Adjust brightness/contrast uniformly across entire image
- No selective manipulation of individual bands

### Microscopy
- Include scale bar in every panel
- State magnification in legend
- Processing must be applied uniformly to entire image
- Describe any adjustments in STAR Methods

### Flow Cytometry
- Show gating strategy in supplementary figures
- Include percentage in each gate
- Label axes with marker names and fluorochrome

### Schematics/Diagrams
- Created in vector format (Illustrator, BioRender, Inkscape)
- Credit creation tools (e.g., "Created with BioRender.com")
- Use consistent visual language across all schematics in the paper

## File Naming Convention

```
Figure1.pdf
Figure2.pdf
FigureS1.pdf
FigureS2.pdf
```

## Checklist Before Submission

- [ ] All panels labeled with uppercase bold letters (A, B, C...)
- [ ] Font ≥ 6 pt at final print size
- [ ] Arial or Helvetica throughout
- [ ] Resolution ≥ 300 DPI (600 for line art)
- [ ] Width ≤ 17.4 cm
- [ ] Colorblind-accessible
- [ ] Scale bars on all microscopy
- [ ] Error bars defined in legend
- [ ] Sample sizes stated
- [ ] Statistical tests specified in legend
- [ ] Figure legends follow Cell Press structure
- [ ] Supplementary figures cross-referenced
- [ ] File format: PDF/EPS (vector) or TIFF (raster)
