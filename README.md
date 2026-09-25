# FG²M: Reliability-Aware Fine-Grained Matching for Farmland Remote-Sensing Image–Text Retrieval

This repository provides the public paper summary and selected figures for:

> **FG²M: Reliability-Aware Fine-Grained Matching for Farmland Remote-Sensing Image–Text Retrieval**

The manuscript studies image–text retrieval for farmland remote-sensing imagery, where repetitive visual structures, partial descriptions, and semantically compatible unpaired samples make fine-grained matching difficult.

## Method

FG²M is a two-stage framework that combines bidirectional false-negative exclusion, anchor-mediated cross-modal refinement, global-guided node saliency, and dustbin-augmented optimal transport. The method learns selective region–phrase correspondences while allowing visually present but undescribed content to remain unmatched.

![FG²M model architecture](assets/fg2m-model.png)

## FarmR-Bench

FarmR-Bench evaluates farmland image–text retrieval under complementary distribution shifts:

| Subset | Source | Main shift | Images | Captions per image |
|---|---|---|---:|---:|
| FGL-CMR | FGFD | Landscape and geographic variation | 2,606 | 3 |
| FCD-CMR | Hi-CNA | Temporal variation | 11,218 | 3 |
| FES-CMR | AI4Boundaries | Geographic and regional variation | 7,598 | 3 |

All captions associated with the same image are assigned to the same split and are treated as simultaneous positive targets during retrieval evaluation.

### Dataset construction

![FarmR-Bench construction](assets/benchmark-construction.png)

### Geographic coverage

![FarmR-Bench geographic coverage](assets/farmr-bench-map.png)

The benchmark is constructed from publicly available remote-sensing datasets. The source datasets should be cited as follows:

- FGFD: Li *et al.*, “A Comprehensive Deep-Learning Framework for Fine-Grained Farmland Mapping From High-Resolution Images,” *IEEE Transactions on Geoscience and Remote Sensing*, 2025.
- Hi-CNA: Sun *et al.*, “Identifying cropland non-agriculturalization with high representational consistency from bi-temporal high-resolution remote sensing images,” *ISPRS Journal of Photogrammetry and Remote Sensing*, 2024.
- AI4Boundaries: d’Andrimont *et al.*, “AI4Boundaries: An open AI-ready dataset to map field boundaries with Sentinel-2 and aerial photography,” *Earth System Science Data*, 2023.

## Main results

Mean Recall (mR, %) on the reported farmland retrieval benchmarks:

| Dataset | FG²M | Strongest competing result | Gain |
|---|---:|---:|---:|
| FES-CMR | **35.16** | 32.17 | +2.99 |
| FRS-CMR | **35.40** | 34.23 | +1.17 |
| FGL-CMR | **42.71** | 37.28 | +5.43 |
| FCD-CMR | **27.85** | 25.82 | +2.03 |

## Cross-domain transfer

All models are trained on FRS-CMR and directly evaluated on the target datasets:

| Target dataset | FG²M mR (%) | Gain over the strongest reported baseline |
|---|---:|---:|
| RSICD | **26.11** | +6.95 |
| RSITMD | **34.54** | +5.81 |

## Availability

This repository currently contains the paper summary, dataset-construction figures, model visualization, and selected experimental results. The implementation code will be released after acceptance of the paper.

The reported results are part of the submitted manuscript and should not be interpreted as peer-reviewed or officially accepted results until the publication process is complete.

## Citation

```bibtex
@article{fg2m,
  title   = {FG$^2$M: Reliability-Aware Fine-Grained Matching for Farmland Remote-Sensing Image--Text Retrieval},
  note    = {Manuscript under review},
  year    = {2026}
}
```
