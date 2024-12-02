# Complementary Data for "Automated galaxy sizes in Euclid images using the Segment Anything Model".

This repository contains data and images related to the manuscript "Automated galaxy sizes in Euclid images using the Segment Anything Model" published in Astronomy & Astrophysics.

## Data description

Explore the `data/` directory for the available data.

- `data/SAM-Euclid-sizes.csv`

This file contains galaxy size measurements and associated parameters. The columns are described below:

| Column Name            | Description                                                                  |
|-------------------------|-----------------------------------------------------------------------------|
| `gals`                 | Unique identifier for each galaxy.                                           |
| `field`                | Name of the observational field/survey.                                      |
| `morph`                | Morphological classification ([Huertas-Company et al. 2015](https://ui.adsabs.harvard.edu/abs/2015ApJS..221....8H/abstract)).                  |                                  
| `z`                    | Redshift of the galaxy.                                               |
| `log_m`.               | Logarithmic of the stellar mass of the galaxy (in solar masses).             |
| `r_edge`               | Edge radius of the galaxy as measured by BT24 (in kpc).                      |
| `sigma_edge`           | Error in edge radius of the galaxy as measured by BT24 (in kpc).             |
| `ar`                   | Minor to major axis ratio of the elliptical truncation of the galaxy (`b/a`).|
| `pa`                   | Position angle of the elliptical truncation of the galaxy (in degrees).      |
| `f1`                   | F1 score of the SAM segmentation for this galaxy (majority voting).          |
| `rec`                  | Recall of the SAM segmentation for this galaxy (majority voting).            |
| `prec`                 | Precision of the SAM segmentation for this galaxy (majority voting).         |
| `r_0.5`                | Galaxy size derived from the majority voting at the 0.5 threshold (in kpc).  |
| `Deltar_0.5`           | Relative error in the measurement of the size of the SAM truncation          |

See also [Buitrago & Trujillo 2024](https://ui.adsabs.harvard.edu/abs/2024A%26A...682A.110B/abstract), for more details on the different parameters.

- `data/segmentation_masks/`

This folder contains segmentation masks for each galaxy in FITS format. Each file corresponds to a single galaxy and can be visualized using standard astronomical software.

- `data/images/`

This folder contains PDF visualizations for each galaxy. Each PDF includes:
- **Galaxy Parameters**: A table summarizing key properties (e.g., size, redshift, segmentation metrics).
- **RGB Image**: Composite image of the galaxy.
- **Averaged Segmentation Map**: Visualization of the segmentation results from SAM along with the truncation at a 0.5 and 0.7 thresholds.

## Citation
If you use this data, please cite our manuscript:
- [DOI or arXiv link]