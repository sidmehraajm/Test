---
description: 'Level: Beginner | Version 1.0 | Date: 30-March-2022 | By - Siddarth Mehra'
---

# 🏢 Transform Node Attributes

<details>

<summary><strong>Attribute Index</strong></summary>

[#1.-translate-t-double3](transform-node-attributes.md#1.-translate-t-double3 "mention")

[#2.-rotate-r-double3](transform-node-attributes.md#2.-rotate-r-double3 "mention")

[#3.-scale-s-double3](transform-node-attributes.md#3.-scale-s-double3 "mention")

[#shear-sh-double3](transform-node-attributes.md#shear-sh-double3 "mention")

</details>

## 1. translate(t) - _<mark style="color:green;">double3</mark>_

* translateX (tx) - _<mark style="color:green;">double</mark>_
* translateY (ty) - _<mark style="color:green;">double</mark>_
* translateZ (tz) - _<mark style="color:green;">double</mark>_

<details>

<summary>Specifies the object’s translation (Translate X, Y, and Z) attribute values in world space</summary>

* <mark style="color:green;">Is Keyable</mark>&#x20;
* <mark style="color:green;"></mark>![](<../../../.gitbook/assets/image (5) (1).png>)

</details>

Translation can be seen in channelBox and can be queried by -

```python
import pymel.core as pm
obj = pm.PyNode('objName')
obj.getTranslation()
```

## 2. rotate(r) - _<mark style="color:green;">double3</mark>_

* rotateX(rx) - _<mark style="color:green;">double</mark>_
* rotateY (ry) - _<mark style="color:green;">double</mark>_
* rotateZ (rz) - _<mark style="color:green;">double</mark>_

<details>

<summary>Specifies the object's scale ( Scale X, Y, and Z) attribute values in local space</summary>

* Unlike translation and rotation attributes, scale uses only the Local coordinate system.
* <mark style="color:green;">Is Keyable</mark>&#x20;
* ![](<../../../.gitbook/assets/image (5).png>)

</details>

Rotation can be seen in channelBox and can be queried by -

```python
import pymel.core as pm
obj = pm.PyNode('objName')
obj.getRotation()
```

## 3. scale(s) - _<mark style="color:green;">double3</mark>_

* scaleX(sx) - _<mark style="color:green;">double</mark>_
* scaleY (sy) - _<mark style="color:green;">double</mark>_
* scaleZ (sz) - _<mark style="color:green;">double</mark>_

<details>

<summary><strong>Scale</strong> is used to scale a dag node in a 3D space</summary>

* <mark style="color:green;">Is Keyable</mark>&#x20;
* ![](<../../../.gitbook/assets/image (9).png>)

</details>

Scale can be seen in channelBox and can be queried by -

```python
import pymel.core as pm
obj = pm.PyNode('objName')
obj.getScale()
```

## 4. shear(sh)- _<mark style="color:green;">double3</mark>_

* shearXY(shxy) _- <mark style="color:green;">double</mark>_
* shearXZ(shxz) _- <mark style="color:green;">double</mark>_
* shearYZ(shyz) _- <mark style="color:green;">double</mark>_

<details>

<summary>When the Shear XYZ values are changed from 0,0,0, shears or non-proportionately scales the selected geometry.</summary>

* <mark style="color:green;">Is Keyable</mark>&#x20;
* <mark style="color:green;"></mark>![](<../../../.gitbook/assets/image (6).png>)<mark style="color:green;"></mark>
* ![](../../../.gitbook/assets/maya\_AKKPH3Vdz7.gif)

</details>



Shear can be seen in AttributeEditor and can be queried by -

```python
import pymel.core as pm
obj = pm.PyNode('objName')
obj.getShear()
```

