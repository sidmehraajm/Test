---
description: >-
  Level: Beginner | Version 1.0 | Date: 13-Feb-2022 | By -Siddarth Mehra,
  Himanshi Ahuja
---

# 🕸 Geometry Check before Rigging

## Why does Geometry matter?

In quality character animation, all the steps in creating are equally important, starting from the design, to the animation part. \
For getting the perfect deformation one of the most important aspects is the topology of the mesh, even though there are many deformers and stuff that can help get good deformation, the basic requirement is a clean and properly distributed mesh, we'll discuss more on this below

![](../.gitbook/assets/maya\_bHaTNPipgX.gif)

## 1. Topology

Topology matters a lot as when rigging a character not only the topology needs to be clean and properly organized but also has the flow of deformation. \
The flow of deformation means creating the mesh flow by thinking about how it will be deformed.

### How to Check Topology

1. Switching on the Default Lighting, Wireframe on mesh, Default colour & Turning off textures to check the flow properly
2. Checking the places which are going to have extreme deformations&#x20;
3. Making sure the Normals are facing the right direction. (Tip: Switch off Two-sided lighting )

{% embed url="https://youtu.be/57uRXf6BBs4" %}

### Checking the normals&#x20;

> Normal may not create any issues in Riggig but can have issues in rendering further down the line, so to prevent re rigging or transfering weights and anything repetitive rigging should check it once before starting to rig. In the below example as we can see if Two Sided Lighting is switched on we can miss flipped normals.

![](../.gitbook/assets/maya\_u6YPHrsfXk.gif)

> Learn more about normals -

{% content-ref url="polygon-normals.md" %}
[polygon-normals.md](polygon-normals.md)
{% endcontent-ref %}

### Cleaning up the Scene&#x20;

> A clean scene with no unncessary nodes and predefined groups for specific objects such as geometry levels, non rendering geos and rigging stuff helps a lot while setting up the pipeline tools. Additionally these redundant node(unused shaders, namespaes, ) can make the scene heavier and even cause problesm

* ### Tools to check & Fix model issues

1. Switching on the Default Lighting, Wireframe on mesh, Default color & Turning off textures to check the flow properly
2. Checking the places which are going to have extreme deformations&#x20;
3. Making sure the Normals are facing the right direction. (Tip: Switch off Two sided lighting )

### Tools to check model

1. modelChecker

{% embed url="https://github.com/JakobJK/modelChecker" %}

2\. abSymMesh

{% embed url="https://www.highend3d.com/maya/script/absymmesh-for-maya" %}

<details>

<summary>References </summary>

[https://sketchfab.com/3d-models/base-mesh-01-7fd03337ae85486192094b506722375c](https://sketchfab.com/3d-models/base-mesh-01-7fd03337ae85486192094b506722375c)

</details>
