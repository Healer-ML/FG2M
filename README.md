# FG²M: Reliability-Aware Fine-Grained Matching for Farmland Remote-Sensing Image–Text Retrieval

**FG²M** is a reliability-aware fine-grained matching framework for farmland remote-sensing image–text retrieval. It addresses repetitive visual patterns, partial image–text correspondence, and semantically compatible but unpaired samples.

> **Status:** pre-publication manuscript. The implementation code will be released after paper acceptance.

## Method

FG²M combines bidirectional false-negative exclusion, anchor-mediated cross-modal refinement, global-guided node saliency, and dustbin-augmented optimal transport in a two-stage retrieval framework.

<p align="center">
  <img src="assets/fg2m-model.png" alt="FG²M model architecture" width="94%">
</p>

## FarmR-Bench

FarmR-Bench evaluates retrieval under landscape, temporal, and geographic shifts. It contains FGL-CMR (2,606 images), FCD-CMR (11,218 images), and FES-CMR (7,598 images); each image is associated with three captions. Captions belonging to the same image remain in the same split and are treated as simultaneous positive targets.

**Dataset construction**

<p align="center">
  <img src="assets/benchmark-construction.png" alt="FarmR-Bench construction" width="92%">
</p>

**Geographic coverage**

<p align="center">
  <img src="assets/farmr-bench-map.png" alt="FarmR-Bench geographic coverage" width="92%">
</p>

## Experimental results

The following figures reproduce the existing manuscript tables without reformatting or recalculating the reported values. Click any table to view it at full resolution.

**FES-CMR and FRS-CMR**

<p align="center">
  <a href="assets/table-fes-frs.png"><img src="assets/table-fes-frs.png" alt="FES-CMR and FRS-CMR results" width="96%"></a>
</p>

**FGL-CMR and FCD-CMR**

<p align="center">
  <a href="assets/table-fgl-fcd.png"><img src="assets/table-fgl-fcd.png" alt="FGL-CMR and FCD-CMR results" width="96%"></a>
</p>

**Province-wise FRS-CMR results**

<p align="center">
  <a href="assets/table-province.png"><img src="assets/table-province.png" alt="Province-wise FRS-CMR results" width="96%"></a>
</p>

## Data sources

The benchmark is constructed from publicly available remote-sensing datasets. Please cite the original dataset papers: FGFD (Li *et al.*, TGRS 2025), Hi-CNA (Sun *et al.*, ISPRS J. Photogramm. Remote Sens. 2024), and AI4Boundaries (d'Andrimont *et al.*, ESSD 2023).

## Availability

This repository intentionally contains only the paper summary, selected figures, and existing result-table images. Source code and training scripts will be released after acceptance.
