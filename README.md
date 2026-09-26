# FG²M: Reliability-Aware Fine-Grained Matching for Farmland Remote-Sensing Image–Text Retrieval

**FG²M** is a reliability-aware fine-grained matching framework for farmland remote-sensing image–text retrieval. It addresses repetitive visual patterns, partial image–text correspondence, and semantically compatible but unpaired samples.

> [!IMPORTANT]
> **Code release:** The implementation code and training scripts will be released after paper acceptance.

## Method

FG²M combines bidirectional false-negative exclusion, anchor-mediated cross-modal refinement, global-guided node saliency, and dustbin-augmented optimal transport in a two-stage retrieval framework.

<div align="center"><img src="assets/fg2m-model.png" alt="FG²M model architecture" width="94%"></div>

## FarmR-Bench

FarmR-Bench evaluates retrieval under landscape, temporal, and geographic shifts. It contains FGL-CMR (2,606 images), FCD-CMR (11,218 images), and FES-CMR (7,598 images); each image is associated with three captions. Captions belonging to the same image remain in the same split and are treated as simultaneous positive targets.

<div><strong>Dataset construction</strong></div>
<div align="center"><img src="assets/benchmark-construction.png" alt="FarmR-Bench construction" width="92%"></div>
<div><strong>Geographic coverage</strong></div>
<div align="center"><img src="assets/farmr-bench-map.png" alt="FarmR-Bench geographic coverage" width="92%"></div>

## Experimental results

The following figures reproduce the existing manuscript tables without reformatting or recalculating the reported values. Click any table to view it at full resolution.

<div><strong>FES-CMR and FRS-CMR</strong></div>
<div align="center"><a href="assets/table-fes-frs.png"><img src="assets/table-fes-frs.png" alt="FES-CMR and FRS-CMR results" width="96%"></a></div>
<div><strong>FGL-CMR and FCD-CMR</strong></div>
<div align="center"><a href="assets/table-fgl-fcd.png"><img src="assets/table-fgl-fcd.png" alt="FGL-CMR and FCD-CMR results" width="96%"></a></div>
<div><strong>Province-wise FRS-CMR results</strong></div>
<div align="center"><a href="assets/table-province.png"><img src="assets/table-province.png" alt="Province-wise FRS-CMR results" width="96%"></a></div>

## Data sources

The benchmark is constructed from publicly available remote-sensing datasets. Please cite the original dataset papers: FGFD (Li *et al.*, TGRS 2025), Hi-CNA (Sun *et al.*, ISPRS J. Photogramm. Remote Sens. 2024), and AI4Boundaries (d'Andrimont *et al.*, ESSD 2023).


