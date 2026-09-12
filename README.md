# PCD_Assignment01
Downsampling (Max, Average, Median) and Upsampling (NN, Bilinear, Bicubic).

Inputs: `images/malvin.jpeg` and `images/pemandangan.jpg`, supplied by the student. This version uses photographs, not the earlier synthetic images. "Medium" is interpreted as Median.


## Contents
- PCD_Assignment01.ipynb: notebook with code, explanations and locally executed outputs.
- sampling.py: matching executable source.
- images/: two original input files.
- results/processed_inputs/: exact RGB references used for evaluation.
- results/downsampled/: 12 reduced PNGs.
- results/upsampled/: 36 reconstructed PNGs.
- results/figures/: input and comparison figures, including detail crops.
- results/metrics.csv: 36 MSE/PSNR records.
- Report_Analysis.pdf: three-page English analysis.
- Report_Analysis.md: editable analysis text.
- requirements.txt: dependencies for local execution.

## Main result
Average + Bicubic has the highest PSNR for both photos at 2x and 4x. At 4x the portrait reaches 29.47 dB and the landscape 19.22 dB. These are pipeline measurements against the processed original, not a universal ranking.

## Local run
From this directory: `pip install -r requirements.txt`, then `python sampling.py`. Results are regenerated in results/. A results ZIP is also created for convenience; it does not need uploading to GitHub when results/ is already included.

## Image preprocessing
Portrait: 1200 x 1600 unchanged. Landscape: 474 x 842 cropped to 472 x 840 by removing two rightmost columns and bottom rows. No initial resizing or stretching. All dimensions are width x height.

## Sources
Photographs supplied by the student; this repository does not assert ownership of them.
Pillow filters: https://pillow.readthedocs.io/en/stable/handbook/concepts.html#filters
