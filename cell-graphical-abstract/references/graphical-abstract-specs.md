# Cell Press Graphical Abstract — Complete Specifications Reference

## Official Cell Press Requirements (2024–2025)

### Submission Requirements

All Cell Press journals **require** a Graphical Abstract at the time of manuscript submission. This includes:
- Cell
- Molecular Cell
- Cell Stem Cell
- Cell Reports
- Cell Systems
- Cell Chemical Biology
- Cell Host & Microbe
- Immunity
- Neuron
- Developmental Cell
- Current Biology
- Cell Metabolism
- Cell Genomics
- Cell Reports Medicine
- Cell Reports Methods
- Med
- iScience

### Technical Specifications

| Parameter | Requirement |
|-----------|-------------|
| Aspect ratio | 1:1 (square) |
| Minimum dimensions | 1200 × 1200 pixels |
| Recommended dimensions | 1500 × 1500 pixels |
| Maximum dimensions | 3000 × 3000 pixels |
| Resolution | 300 DPI minimum |
| File formats (vector) | PDF, EPS, AI |
| File formats (raster) | TIFF, PNG (high-quality) |
| NOT accepted | JPEG, GIF, BMP |
| Color mode | RGB |
| Maximum file size | 10 MB |
| Background | White (#FFFFFF) preferred |

### Content Guidelines

#### MUST
- Convey the main finding of the paper
- Be understandable without reading the text
- Use simple, bold, conceptual imagery
- Maintain scientific accuracy
- Be original artwork (created by the authors)
- Use consistent color coding with main figures
- Be accessible to colorblind readers

#### MUST NOT
- Contain more than 4 panels
- Include text smaller than 5 pt
- Use copyrighted material from other publications
- Be a direct copy of any figure from the manuscript
- Include excessive abbreviations
- Be overly complex or data-dense
- Use decorative elements that don't convey information

### Display Contexts

The Graphical Abstract will appear at these sizes:

| Context | Display Size | Key Consideration |
|---------|-------------|-------------------|
| Article TOC (web) | ~200 × 200 px | Must be readable as thumbnail |
| Article header (web) | ~600 × 600 px | Main online display |
| Social media (Twitter/X) | ~500 × 500 px | High visual impact needed |
| Cell Press app | ~300 × 300 px | Mobile-optimized clarity |
| Print TOC (rare) | ~6 × 6 cm @ 300 DPI | Print-quality vector preferred |

## Design Best Practices

### Composition Principles

1. **Visual hierarchy**: Most important element should be largest/most central
2. **Reading direction**: Western readers scan left-to-right, top-to-bottom
3. **Focal point**: One clear visual center of attention
4. **Negative space**: Use white space to separate conceptual units
5. **Balance**: Distribute visual weight evenly across the square
6. **Unity**: All elements should feel like one cohesive image

### Arrow and Connector Usage

| Arrow Type | Meaning | Visual |
|-----------|---------|--------|
| Solid → | Leads to / causes | ──── → |
| Dashed → | Indirect effect | - - - → |
| Bar-headed ⊣ | Inhibits / blocks | ────⊣ |
| Bidirectional ↔ | Mutual interaction | ← ──── → |
| Curved ↷ | Feedback / cycling | ↷ |
| Bold → | Main pathway | ═══ → |
| Thin → | Secondary pathway | ─── → |

### Icon Design Standards

#### Size Hierarchy
- **Primary elements** (main discovery): 25–35% of canvas width
- **Secondary elements** (context): 15–25% of canvas width
- **Labels/text**: 3–8% of canvas height per line
- **Arrows/connectors**: 2–4 px stroke width at 1200px canvas

#### Cellular Components Reference

```
DNA double helix:    ╱╲╱╲╱╲    (simplified)
RNA:                 ∿∿∿∿∿     (wavy single strand)
Protein:             ⬭         (blob/ribbon)
Antibody:            Y          (Y-shape)
Receptor:            ⊤          (transmembrane)
Ion channel:         ⊞          (pore in membrane)
Vesicle:             ○          (circle)
Nucleus:             ◎          (circle in circle)
Cell:                ⬭          (rounded rectangle)
Mitochondria:        ⬭≋         (oval with lines)
```

### Color Application Rules

1. **Maximum 5 distinct colors** in one GA (including black and gray)
2. **One accent color** for the key finding (Cell Red #C9302C recommended)
3. **Neutral colors** (gray, light blue) for context/background elements
4. **Green** for positive outcomes / activation
5. **Red** for negative outcomes / inhibition / disease
6. **Blue** for neutral processes / tools / methods
7. **Never rely on color alone** — use shape, size, or pattern as redundant coding

### Text Usage Guidelines

| Text Element | Recommended Size | Style |
|-------------|-----------------|-------|
| Main title/label | 10–14 pt | Bold, Arial |
| Element labels | 8–10 pt | Regular, Arial |
| Small annotations | 5–7 pt | Regular, Arial |
| Gene names | 8–10 pt | Italic, Arial |

**Rules:**
- Minimum text possible — if you can replace text with a recognizable icon, do so
- All text must be horizontal (no rotated text)
- Text must have sufficient contrast against background (WCAG AA minimum)
- Avoid text on colored backgrounds — use white label boxes if needed

## Examples of Common Paper Types → GA Strategies

### Type 1: Mechanistic Discovery
**Paper**: "Protein X phosphorylates Y, activating pathway Z in disease"
**Strategy**: Linear pathway flow
**Layout**: [Normal cell] → [Kinase activity] → [Pathway activation] → [Disease phenotype]
**Key visual**: Phosphorylation event (P in circle) as central element

### Type 2: Therapeutic Intervention
**Paper**: "Drug A inhibits target B, reversing phenotype C"
**Strategy**: Before/After comparison
**Layout**: Left panel (disease + target) | Drug in center | Right panel (healthy)
**Key visual**: Drug molecule blocking target protein

### Type 3: Omics/Screening Discovery
**Paper**: "CRISPR screen identifies 50 essential genes for process X"
**Strategy**: Funnel/filtering
**Layout**: [Large gene set] → [Screen/Filter] → [Key hits] → [Biological validation]
**Key visual**: Funnel narrowing from many to few

### Type 4: Developmental/Differentiation Study
**Paper**: "Cell type A differentiates through intermediate B to become C"
**Strategy**: Trajectory/timeline
**Layout**: Left (progenitor) → Center (intermediate) → Right (mature)
**Key visual**: Cell morphology changes along trajectory with key markers

### Type 5: Structural Biology
**Paper**: "Cryo-EM reveals mechanism of channel gating"
**Strategy**: Structure-function
**Layout**: [Closed state structure] → [Stimulus] → [Open state structure]
**Key visual**: 3D protein structure (simplified ribbon) in two conformations

### Type 6: Computational/Resource
**Paper**: "New algorithm predicts protein interactions with 95% accuracy"
**Strategy**: Input → Tool → Output
**Layout**: [Raw data/sequences] → [Algorithm/Tool box] → [Predictions + validation]
**Key visual**: The tool/algorithm as a central processing unit

## Production Tools

### Recommended Software
| Tool | Best for | Cost |
|------|---------|------|
| Adobe Illustrator | Professional vector GA | Paid |
| Inkscape | Free vector alternative | Free |
| BioRender | Biology-specific icons | Freemium |
| Affinity Designer | Vector, one-time purchase | Paid |
| Python (matplotlib + PIL) | Programmatic generation | Free |
| Figma | Collaborative design | Freemium |

### Python Generation Template

```python
import matplotlib.pyplot as plt
import matplotlib.patches as mpatches
from matplotlib.patches import FancyArrowPatch
import numpy as np

# Cell Press GA specifications
fig, ax = plt.subplots(1, 1, figsize=(12, 12), dpi=300)
ax.set_xlim(0, 100)
ax.set_ylim(0, 100)
ax.set_aspect('equal')
ax.axis('off')
fig.patch.set_facecolor('white')

# Cell Press Red accent
CELL_RED = '#C9302C'
DARK_GRAY = '#333333'
LIGHT_GRAY = '#9E9E9E'
BLUE = '#2196F3'
GREEN = '#4CAF50'

# Add elements here...
# [Context] → [Discovery] → [Outcome]

plt.tight_layout(pad=2)
plt.savefig('graphical_abstract.png', dpi=300, bbox_inches='tight',
            facecolor='white', edgecolor='none')
plt.savefig('graphical_abstract.pdf', bbox_inches='tight',
            facecolor='white', edgecolor='none')
```

## Quality Assurance Checklist

### Pre-submission Verification

#### Technical
- [ ] Dimensions: exactly 1:1 ratio
- [ ] Resolution: ≥ 1200 × 1200 px
- [ ] File format: TIFF/PDF/EPS/PNG (not JPEG)
- [ ] File size: ≤ 10 MB
- [ ] Background: white (#FFFFFF)
- [ ] Color mode: RGB

#### Content
- [ ] Conveys main finding without text explanation
- [ ] Passes 3-second glance test
- [ ] Maximum 4 panels
- [ ] All text ≥ 5 pt
- [ ] No copyrighted material
- [ ] Scientifically accurate
- [ ] Colors consistent with main figures

#### Accessibility
- [ ] Readable at 200 × 200 px thumbnail
- [ ] Colorblind-safe (no red-green only distinctions)
- [ ] Sufficient contrast for all elements
- [ ] Shape/pattern redundancy for color-coded elements

#### Style
- [ ] Simple, bold, conceptual
- [ ] Not a data figure
- [ ] Not text-heavy
- [ ] Professional appearance
- [ ] Consistent with Cell Press visual standards
