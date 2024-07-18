# Skill Extraction: benchmarks

This is the official repository containing three skill extraction datasets, from the following papers:

1. [Design of Negative Sampling Strategies for Distantly Supervised Skill Extraction](https://arxiv.org/abs/2209.05987)
2. [Extreme Multi-Label Skill Extraction Training using Large Language Models](https://arxiv.org/abs/2307.10778)

## Dataset description

The `TECH` and `HOUSE` subsets form an extention of the SkillSpan [[1]](#1) dataset, in which spans of skill mentions in sentences have been labeled with corresponding ESCO [[2]](#2) skills.

The `TECHWOLF` subset, although smaller, represents a more generic distribution of job descriptions and skill spans. ESCO skills are directly annotated on the full sentence level, thus omitting the intermediate span identification step.

The ESCO skills in the dataset are referenced by their preferred label, in the 1.1.0 ESCO version.

| Dataset statistics  | TECH      |           | HOUSE     |           | TECHWOLF  |
|-------------------------------|-----------|-----------|-----------|-----------|-----------|
|                               | val       | test      | val       | test      | test      |
| # sentences                   | 470       | 1882      | 243       | 973       | 326       |
| # spans                       | 262       | 1024      | 191       | 786       | 588       |
| # spans with ESCO label       | 152       | 644       | 131       | 532       | 588       |

## Usage

It is recommended to use the HuggingFace datasets for ease of use:
- [TECH](https://huggingface.co/datasets/jensjorisdecorte/skill-extraction-tech)
- [HOUSE](https://huggingface.co/datasets/jensjorisdecorte/skill-extraction-house)
- [TECHWOLF](https://huggingface.co/datasets/jensjorisdecorte/skill-extraction-techwolf)

However, the raw dataset files are also kept under the [data](data) directory. 

## Cite

If you use the `TECH` or `HOUSE` dataset, please include the following reference:

```
@inproceedings{8770980,
  articleno    = {{4}},
  author       = {{Decorte, Jens-Joris and Van Hautte, Jeroen and Deleu, Johannes and Develder, Chris and Demeester, Thomas}},
  booktitle    = {{Proceedings of the 2nd Workshop on Recommender Systems for Human Resources (RecSys-in-HR 2022)}},
  editor       = {{Kaya, Mesut and Bogers, Toine and Graus, David and Mesbah, Sepideh and Johnson, Chris and Gutiérrez, Francisco}},
  isbn         = {{9781450398565}},
  issn         = {{1613-0073}},
  language     = {{eng}},
  location     = {{Seatle, USA}},
  pages        = {{7}},
  publisher    = {{CEUR}},
  title        = {{Design of negative sampling strategies for distantly supervised skill extraction}},
  url          = {{https://ceur-ws.org/Vol-3218/RecSysHR2022-paper_4.pdf}},
  volume       = {{3218}},
  year         = {{2022}},
}
```

If you use the `TECHWOLF` dataset, please include the following refence:

```
@misc{decorte2023extrememultilabelskillextraction,
      title={Extreme Multi-Label Skill Extraction Training using Large Language Models}, 
      author={Jens-Joris Decorte and Severine Verlinden and Jeroen Van Hautte and Johannes Deleu and Chris Develder and Thomas Demeester},
      year={2023},
      eprint={2307.10778},
      archivePrefix={arXiv},
      primaryClass={cs.CL},
      url={https://arxiv.org/abs/2307.10778}, 
}
```

## Reference

<a id="1">[1]</a> Zhang, Mike, et al. "Skillspan: Hard and soft skill extraction from english job postings." arXiv preprint arXiv:2204.12811 (2022).

<a id="2">[2]</a> https://esco.ec.europa.eu/en/classification/skill_main
