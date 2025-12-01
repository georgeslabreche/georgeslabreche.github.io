---
title: "marsrad v1.0.0: Mars Solar Radiation for R"
excerpt: "An R package to calculate solar irradiance and insolation on Mars."
header:
  overlay_image: /assets/images/posts/2025-12-01/shades-of-martian-darkness.jpg
  caption: "[Shades of Martian Darkness (NASA/JPL-Caltech/TAMU)](https://www.jpl.nasa.gov/images/pia22521-shades-of-martian-darkness/)"
categories:
  - research
tags:
  - mars
  - research
  - R
---

What is marsrad? It stands for "**mars** **rad**iation" and it's an R package to calculate solar irradiance and insolation on Mars for both horizontal and inclined surfaces.

It took a five-year break to go from research code to a proper release but [marsrad](https://github.com/georgeslabreche/marsrad) v1.0.0 is finally [available on CRAN](https://CRAN.R-project.org/package=marsrad). Writing functions is easy, but documenting them and cleaning up the code takes... some motivation.

### Citation

If you use this package in your research or publication, please cite the paper it was developed for:

> Labrèche, Georges and Cordes, Florian. (2020). **"Using a Rover's Active Suspension System as a 2-Axis Solar Tracker Mechanism."** 15th International Symposium on Artificial Intelligence, Robotics and Automation in Space (i-SAIRAS '20), October 2020. [https://www.hou.usra.edu/meetings/isairas2020fullpapers/pdf/5035.pdf](https://www.hou.usra.edu/meetings/isairas2020fullpapers/pdf/5035.pdf)

BibTeX:

```bibtex
@inproceedings{Labreche2020_iSAIRAS20_MarsRoverSherpaTT,
  title={Using a Rover's Active Suspension System as a 2-Axis Solar Tracker Mechanism},
  author={Labrèche, Georges and Cordes, Florian},
  booktitle={15th International Symposium on Artificial Intelligence, Robotics and Automation in Space (i-SAIRAS '20)},
  month={October},
  year={2020},
  url={https://www.hou.usra.edu/meetings/isairas2020fullpapers/pdf/5035.pdf}
}
```

### Background

The marsrad package implements equations from the Appelbaum et al. papers (NASA Technical Memoranda 102299, 103623, 105216, 106321, and 106700), published between 1989 and 1994.

The package is useful for:

- Designing solar power systems for Mars missions.
- Mission planning and energy budget analysis.
- Optimizing solar panel orientations for rovers and landers.
- Understanding how Martian atmospheric dust affects solar energy availability.

### Old School Cool

The Appelbaum formulas are based on Viking Lander optical depth measurements from the late 1970s and early 1980s. They're 36+ years old now and Mars science has moved on. More recent work includes:

- [An improved model for available solar energy on Mars: Optimizing solar panel orientation to assess potential spacecraft landing sites](https://www.sciencedirect.com/science/article/abs/pii/S0273117723002673) (Kerr et al., 2023).
- [A model to calculate solar radiation fluxes on the Martian surface](https://www.swsc-journal.org/articles/swsc/full_html/2015/01/swsc150027/swsc150027.html) (Vicente-Retortillo et al., 2015).
- [Fast and accurate estimation of solar irradiance on Martian slopes](https://agupubs.onlinelibrary.wiley.com/doi/full/10.1029/2008GL034956) (Spiga et al., 2008).

However, the Appelbaum formulas remain useful for first-order estimates, educational purposes, and quick trade studies. They're well-documented, easy to understand, analytically tractable, and give you reasonable ballpark figures for solar energy budgets on Mars. Just don't use them to design your actual flight hardware without consulting more recent atmospheric models.

### Key Features

The package provides [over 30 functions](https://github.com/georgeslabreche/marsrad/blob/master/FUNCTIONS.md) covering:

- **Irradiance calculations** (instantaneous power in W/m²): global, direct beam, diffuse, and albedo-reflected components.
- **Daily insolation** (energy per sol in Wh/m²-day): total solar energy over a full Martian day.
- **Custom period insolation**: energy calculations over any specified time range.
- **Utility functions**: sunrise/sunset times, optimal tilt angles, polar day/night detection, solar zenith angle, and atmospheric optical depth.

All calculations account for Martian atmospheric conditions, including dust opacity, and support various surface orientations and slope angles.

### Installation

Install from CRAN:

```r
install.packages("marsrad")
```

Or install the development version from GitHub:

```r
devtools::install_github("georgeslabreche/marsrad")
```

### Example Usage

```r
library(marsrad)

# Calculate global irradiance at Jezero Crater
# Using location from Ingenuity's final flight (Flight 72, January 18, 2024)
Gh <- G_h(Ls = 183, phi = 18, longitude = 77,
          Ts = 10.26, tau = 0.5, al = 0.2)

# Find optimal tilt angle for a solar panel at Jezero
optimal <- optimal_angle(Ls = 183, phi = 18, unit = 2)
```

### Publications

This package was developed as part of my [Master's thesis](https://www.diva-portal.org/smash/record.jsf?pid=diva2:1413245) at Luleå University of Technology, exploring how the SherpaTT rover's active suspension system could be used as a 2-axis solar tracker on Mars. The research was also published at [i-SAIRAS 2020](https://www.hou.usra.edu/meetings/isairas2020fullpapers/pdf/5035.pdf).

### Links

- [CRAN Package Page.](https://CRAN.R-project.org/package=marsrad)
- [GitHub Repository.](https://github.com/georgeslabreche/marsrad)
- [Package Documentation.](https://georges.fyi/marsrad/)
- [v1.0.0 Release Notes.](https://github.com/georgeslabreche/marsrad/releases/tag/v1.0.0)
