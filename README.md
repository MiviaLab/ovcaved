# OV-CAVED Resources

This is the official repository associated with the paper:

**Open Vocabulary Context Aware Video Event Detection**

Authors Info: 
Name: Vincenzo Carletti, Antonio Greco, Mattia Marseglia, Mario Vento
e-mails: vcarletti@unisa.it (V. Carletti); agreco@unisa.it (A. Greco); mmarseglia@unisa.it (M. Marseglia); mvento@unisa.it (M. Vento)
ORCID(s): 0000-0002-9130-5533 (V. Carletti); 0000-0002-5495-2432 (A. Greco); 0009-0009-0507-6884 (M. Marseglia); 0000-0002-2948-741X (M. Vento)

submitted to *Information Fusion*.

This repository provides the resources related to **Open Vocabulary Context Aware Video Event Detection (OV-CAVED)**, a context-aware and open-vocabulary formulation for surveillance event verification.

OV-CAVED reformulates video anomaly detection by conditioning each detection decision on three complementary sources of information:

- the observed video evidence;
- the operational context describing the monitored scene;
- the natural-language query specifying the event of interest.

Instead of detecting generic abnormality or recognizing a fixed set of anomaly classes, OV-CAVED evaluates whether a user-defined event query is visually present in a video segment under the operational conditions of the monitored scene.

## Repository Content

This repository will contain the code of the automatic annotation tool proposed in the paper, organized in the following folder:

```text
annotation_tool/
```

The `annotation_tool/` folder will include the implementation of the LLM/VLM-assisted annotation pipeline used to generate OV-CAVED-compatible annotations from temporally annotated video anomaly detection datasets.

Given surveillance videos and temporal event annotations, the tool generates the contextual and semantic annotations required by the OV-CAVED framework, including:

- structured operational contexts describing the monitored scene;
- natural-language event queries at different levels of granularity;
- plausible but absent event queries for hard negative supervision;
- query-conditioned labels aligned with temporal event supports.

The annotation tool is designed to reduce the manual effort required to construct context-aware and open-vocabulary surveillance benchmarks. Beyond dataset creation, it can also support practical deployment scenarios by helping operators define operational contexts and events of interest from real surveillance videos.

## OV-CAVED UCF-Crime Benchmark

Using the proposed annotation tool, we build **OV-CAVED UCF-Crime**, an OV-CAVED-compliant benchmark derived from the widely used UCF-Crime dataset.

Each video is enriched with an operational context and natural-language event queries, enabling the evaluation of context-aware event verification at both chunk level and video level. The benchmark supports the analysis of how operational context, query specificity, and temporal grounding affect open-vocabulary surveillance event detection.

The dataset will be released on Zenodo after paper acceptance.

Dataset link:

```text
https://zenodo.org/records/20540649?token=eyJhbGciOiJIUzUxMiJ9.eyJpZCI6IjY5ZjNhMjU3LTcyY2EtNDcxZC05NWE5LTBiYWIxMzg4MzkwZiIsImRhdGEiOnt9LCJyYW5kb20iOiJkMmFjYjY1YjY5NzgwNDZlNmZkM2NiZjE1YjBlZjljMyJ9.QqCQ0fYv41Haa8hoV1A1H3uRdmtHE_r0HeaN7dOjmjs4MjGgSlbvu0CcislBiGa90Un4hH73CW1xqkyH87Gzxw
```

## Availability

The code of the automatic annotation tool and the link to the OV-CAVED UCF-Crime benchmark will be made publicly available after acceptance of the paper.

## Main Features

- Automatic generation of OV-CAVED-compatible annotations.
- Support for temporally annotated video anomaly detection datasets.
- Structured operational context generation.
- Multi-granularity event query generation.
- Plausible absent query generation for hard negative supervision and evaluation.
- Query-conditioned label generation.
- Dataset-agnostic design.
- Support for benchmark construction and surveillance system configuration.

## Contact

For questions or further information, please contact the authors of the paper.
