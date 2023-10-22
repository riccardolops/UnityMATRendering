# UnityMATRendering
Medial Axis Transform rendering, implemented in Unity3D.

Pls refer to [link](https://songshibo.github.io/2021/04/12/Medial-Axis-Transform-Mesh-Generation/) for detailed generation process.

And this [post](https://songshibo.github.io/2022/01/04/Updates-for-blender-mat-addon/) for the strategy of detecting degenerated slab.

This addon will generate medial meshes & interpolated MATs from MA files in blender

MA file(Different from [mayAscii](https://download.autodesk.com/us/maya/2011help/index.html?url=./files/Maya_ASCII_file_format.htm,topicNumber=d0e702047)) stores the the information of medial mesh. It can be generated using [Q-MAT](https://binwangthss.github.io/qmat/qmat.html) or [Q-MAT+](https://personal.utdallas.edu/~xguo/GMP2019.pdf).

---
If UnityMATRendering contributes to an academic publication, cite it as:

```bib
@misc{UnityMATRendering,
  title = {UnityMATRendering},
  author = {Riccardo Lops},
  note = {https://github.com/riccardolops/UnityMATRendering},
  year = {2023}
}
```