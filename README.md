# OV-CAVED Resources

Official repository of the paper:

**Open Vocabulary Context Aware Video Event Detection**
Vincenzo Carletti, Antonio Greco, Mattia Marseglia, Mario Vento
Department of Information and Electrical Engineering and Applied Mathematics (DIEM), University of Salerno, Italy

*Submitted to the International Journal of Computer Vision (IJCV).*

| Author | E-mail | ORCID |
|---|---|---|
| Vincenzo Carletti | vcarletti@unisa.it | [0000-0002-9130-5533](https://orcid.org/0000-0002-9130-5533) |
| Antonio Greco | agreco@unisa.it | [0000-0002-5495-2432](https://orcid.org/0000-0002-5495-2432) |
| Mattia Marseglia | mmarseglia@unisa.it | [0009-0009-0507-6884](https://orcid.org/0009-0009-0507-6884) |
| Mario Vento | mvento@unisa.it | [0000-0002-2948-741X](https://orcid.org/0000-0002-2948-741X) |

> **Status:** this repository is a placeholder. The code and the benchmark will be released upon acceptance of the paper.

## Overview

**Open Vocabulary Context Aware Video Event Detection (OV-CAVED)** is a context aware and open vocabulary formulation for surveillance event verification. Each detection decision is conditioned on three complementary sources of information:

- the observed video evidence;
- an operational context describing the monitored scene;
- a natural-language query specifying the event of interest.

Instead of detecting generic abnormality or recognizing a fixed set of anomaly classes, OV-CAVED verifies whether a user-defined event is visually present in a video segment under the operational conditions of the monitored scene.

## Planned Content

Upon acceptance, this repository will contain:

```text
annotation_tool/     # LLM/VLM-based automatic annotation tool
evaluation/          # zero-shot evaluation protocol (row-level and video-level metrics)
```

### Automatic annotation tool

Given surveillance videos and their temporal event annotations (and, optionally, dense video descriptions), the tool generates the annotations required by OV-CAVED:

- structured operational contexts (21 fields in 5 areas) describing the monitored scene;
- natural-language event queries at three levels of granularity (coarse, mid, fine);
- plausible absent queries used as hard negatives;
- query-conditioned labels aligned with the temporal supports of the events.

The tool is dataset-agnostic and can be applied to any temporally annotated video anomaly detection dataset. Beyond benchmark construction, it can help operators define operational contexts and events of interest for real surveillance deployments.

### Evaluation protocol

Code to reproduce the zero-shot evaluation reported in the paper, including chunk-based querying of the model, row-level metrics (AP, AP_a, precision, recall, F1) and video-level alarm metrics.

## OV-CAVED UCF-Crime Benchmark

Using the annotation tool, we build **OV-CAVED UCF-Crime**, an OV-CAVED-compliant benchmark derived from UCF-Crime. Each video is paired with an operational context and with event queries at multiple granularities; test-set queries, temporal supports and contexts are manually reviewed. The benchmark enables the evaluation of context aware event verification at both row level and video level.

The benchmark will be released on Zenodo upon acceptance of the paper.

**Note on third-party data.** OV-CAVED UCF-Crime will contain annotations only. The original videos will not be redistributed and must be obtained from the official [UCF-Crime](https://www.crcv.ucf.edu/projects/real-world/) release, under its terms of use. Dense video descriptions used by the annotation tool are taken from UCA-Crime.

## Contact

For questions, please contact the corresponding author: Mattia Marseglia (mmarseglia@unisa.it).
