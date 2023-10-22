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

## Results

this addon will import medial axis transform as several objects:

- Medial mesh
- Medial sphere
- Medial cone
- Medial slab


| <img src=".\render_results\medial mesh.PNG" alt="medial mesh" style="zoom:33%;" /> | <img src=".\render_results\sphere.PNG" alt="sphere" style="zoom:33%;" /> | <img src=".\render_results\cone.PNG" alt="cone" style="zoom:33%;" /> | <img src=".\render_results\slab.PNG" alt="slab" style="zoom:33%;" /> | <img src=".\render_results\result.PNG" alt="result" style="zoom:33%;" /> |
| :-: | :-: | :-: | :-: | :-: |
| medial mesh | medial spheres | medial cones | medial slabs | combined |

## Requirements

- Blender 2.80.0 or older

## MA file structure

> /# number of vertex(medial sphere)/edge(medial cone)/face(medial slab)
>
> vertices edges faces
>
> \# v/e/f indicates the type represented by current line
>
> /# (x,y,z): center of the medial sphere; r: radius
>
> v x y z r
>
> /# two end vertices of the edge
>
> e v1 v2
>
> /# three vertices of a triangle face
>
> f v3 v4 v5
>
> \#  comment lines in MA file should start with #