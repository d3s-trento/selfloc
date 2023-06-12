# Anchor Self-Localization

> **_NOTE:_**  This repository is work in progress and more data, code, and instructions will be added over the following days/weeks.

This repository contains the source code and datasets of our paper 
**Self-Localization of Ultra-wideband Anchors: From Theory to Practice**
published at IEEE Access and openly available at
https://ieeexplore.ieee.org/abstract/document/10080967.

In this paper, we look at the problem of finding the positions of UWB anchors
in large spaces via self-localization. To this end, we exploit a multidimensional
scaling (MDS) algorithm, built atop Python [scikit-learn](https://scikit-learn.org/stable/)
library, to estimate the positions of the anchor devices deployed in three
real-world, large-scale, multi-hop UWB testbeds. These testbeds are:

1. **PLANT:** A 28-anchor deployment in a large industrial plant, covering a
rectangular area of ∼3000 m2. It is characterized by the presence of metallic
objects and NLoS conditions, typical of industrial settings.
2. **DEPARTMENT:** A 36-anchor deployment spanning an entire floor at the University
of Trento. The anchors cover an area of 80 m × 40 m, but are deployed mostly
along corridors, which are very narrow (2.7 m) and long. This yields
a very challenging geometry for localization, yet representative of many indoor
applications.
![UNITN Department](https://github.com/d3s-trento/selfloc/blob/main/img/unitn-department.png "UNITN DISI Department")

3. **RECEPTION:** A 19-anchor deployment covering a total of 720 m2 in the reception
floor of the University of Trento. The area is L-shaped, with two
nearly-separated areas connected only by a few NLoS links.
![UNITN Reception](https://github.com/d3s-trento/selfloc/blob/main/img/unitn-reception-talla.png "UNITN Reception")

The true positions of the anchor nodes can be found in
[selfloc/sw/deployments](https://github.com/d3s-trento/selfloc/tree/main/sw/deployments).

DEPARTMENT and RECEPTION are now part of the public
[CLOVES IoT Testbed](https://iottestbed.disi.unitn.it/cloves/) at the
University of Trento, which you can use right away following
[this page](https://iottestbed.disi.unitn.it/cloves/getting-started/).


## Repository Structure
```
.
├── README.md
├── data: ranging and connectivity data from the the three testbeds
│   ├── department
│   ├── plant
│   └── reception
├── img: image files used in this README.md and clean images to draw testbed maps
└── sw
    ├── deployments: true positions of testbed nodes

```

## Publications

Please consider citing our IEEE Access paper if you use the data or code
provided in this repository.

```
@article{selfloc,
  author={Corbal\'{a}n, Pablo and Picco, Gian Pietro and Coors, Martin and Jain, Vivek},
  journal={IEEE Access},
  title={{Self-Localization of Ultra-Wideband Anchors: From Theory to Practice}},
  year={2023},
  volume={11},
  number={},
  pages={29711-29725},
  doi={10.1109/ACCESS.2023.3261567}
}
```

## Disclaimer
We take no responsibility for and give no warranties in respect of using
the data and code provided in this repository.
