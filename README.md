# Garment Stitch Defect Classification

Deep learning classification of 11 sewing stitch defect types across 11 fabric
types, with an analysis of how well models generalise to **unseen fabrics**.

> **Status:** in progress — dataset analysis complete, modelling underway.

## The problem

Automated garment inspection models are usually evaluated with a random
train/test split. That leaks fabric identity between the two sets: the model
sees denim in training and denim in testing, so the score reflects performance
on *known* materials.

A real factory constantly introduces new fabrics. This project measures the gap
between the two settings:

- **Random split** — the conventional benchmark
- **Leave-one-fabric-out** — train on 10 fabrics, test on the 11th, repeated 11×

## Dataset

[StitchingNet](https://github.com/hyungjungkim/StitchingNet-dataset) — 14,565
images (224×224 RGB), captured on an industrial sewing machine.

| Property | Value |
|---|---|
| Images | 14,565 (0 corrupt) |
| Classes | 11 — Normal + 10 defect types |
| Fabrics | 11 |
| Class balance | Imbalance ratio 2.10, normalised entropy 0.988 |
| Coverage | All 11 classes present in all 11 fabrics |

Defect types: skipped stitch, broken stitch, pinched fabric, crooked seam,
thread sagging, puckering, stain and damage, needle mark, bobbin thread pulling
up, overlapped stitch.

The dataset is **not** redistributed here — see Setup.

## Results

_Pending — see Status above._

## Setup

_Pending._

## Licensing

Code: MIT (see `LICENSE`).

The StitchingNet dataset is licensed separately under **CC BY-NC 4.0**
(non-commercial) and is not included in this repository. Obtain it from the
authors: https://github.com/hyungjungkim/StitchingNet-dataset

Jung et al. (2025), *Journal of Computational Design and Engineering* 12(4).
