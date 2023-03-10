# Citing a repository

Sometimes you need to cite some software that you used to generate results in a paper. If the software contains instructions for how to cite it then you should use those instructions. For example, the repository might contain a [`CITATION.cff` file](gh-citable.md), see e.g https://github.com/finsberg/ldrb or it might contain instructions for how to cite the software in the README, see e.g https://github.com/ComputationalPhysiology/simcardems/blob/main/README.md#citing

If no instructions exists you should use the `@misc` entry, e.g
```
@misc{Finsberg_MPS_motion,
author = {Finsberg, Henrik},
title = {{MPS motion - Library for tracking motion in cardiac mps data}},
howpublished = {\url{https://github.com/ComputationalPhysiology/mps-motion}},
note = {Accessed: 2022-10-06},
year = {2022}
}
```
