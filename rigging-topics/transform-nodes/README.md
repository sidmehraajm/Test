---
description: 'Level: Beginner | Version 1.0 | Date: 21-Feb-2022 | By - Siddarth Mehra'
---

# ☦ Transform Nodes

## Transforms (A Rigger's right hand)

> Transform nodes are [**dagNodes** ](./#dag-and-dag-hierarchy)that are used to group and transform other dagNodes. \
> Even though when _**Shapes**_ is switched off in Outliner It seems like the transform node ICON changes and looks like it's, we need to understand that-\
> **All dagNodes that are not transform nodes in Maya must exist as a child of some transform node**. For example, a Sphere shape has to be under a tranform node always.

![](../../.gitbook/assets/maya\_cgzPWEp8ty.gif)

### Mysterious Transform Icons in Maya

{% hint style="success" %}
Maya Transform nodes can be confusing at the start because of how it displays the icons For example If we had a Transform, a locator, a Camera & a Mesh.\
Whichever is the _**First Child DAG Node**_ that _**Child's Shape**_ will be shown as the icon of that transform
{% endhint %}

![](../../.gitbook/assets/maya\_3BkxPrmk2Y.gif)



```
'''
To change a shape node's parent select the child shape and then the parent. 
'''
#mel
parent -r -s
#python 
'''python
import maya.cmds as cmds
cmds.parent(r=1,s=1)
'''
```



## World and Local Coordinates&#x20;

> For understanding World and local cordinates, first of all, we need to know that there is an origin in the maya scene from which all the calculations takes place,\
> For example, if there is a grid and we need to find the mathematical position of something in that grid we would need to know the origin that is xy(0,0) in a 2d space and xyz(0,0,0) in a 3d space.
>
> ![](<../../.gitbook/assets/image (7).png>)

### World Coordinates(World Space)

> World space is the coordinate system for the entire scene. Its origin is at the center of the scene. The grid you see in view windows shows the world space axes.(0,0,0)
>
> ![](https://help.autodesk.com/cloudhelp/2018/ENU/Maya-Basics/images/GUID-8B7AD211-47B4-4790-8543-82777029C75A.png)



### Object Space

> Object space is the coordinate system from an object’s point of view. The origin of object space is at the object’s pivot point, and its axes are rotated with the object.
>
> ![](https://help.autodesk.com/cloudhelp/2018/ENU/Maya-Basics/images/GUID-BB1C65CF-70BB-4B06-AC52-D50AAC0988FC.png)

### Local Space

> Local Space is similar to Object space, and is really important to understand for example if we have a orange on a grid and we move from  0 to 2 we moved it 2 points and it has local transform value of 2 spaces, but if we put that orange in a basket and move that basket to 2 spaces it's local transform value is 0 but it's world transform position changes to 2
>
> It can be a bit complicated to understand, in this maya scene I have created an example for this and tried to make it visual using bifrost

![](../../.gitbook/assets/maya\_NBJp4EpmIP.gif)

{% hint style="warning" %}
### Local & World Space example:

So it can be understood by this simple example, if I give you my address or coordinates to my location, it is the position in the world, whereas if I give you a relative direction like my house is 1mile from the bus stand, that would be local space.
{% endhint %}

## Transform Node Attributes

> **I would suggest looking into** [**Transform Node Attributes**](transform-node-attributes.md) **Page before jumping further**

{% content-ref url="transform-node-attributes.md" %}
[transform-node-attributes.md](transform-node-attributes.md)
{% endcontent-ref %}

![](../../.gitbook/assets/maya\_gohDDARDIQ.gif)

### Transformation MATRIX

> Transformation Matrix (DAG) transform nodes have many attributes that make up the final transformation matrix as represented by the matrix attribute. This breakdown provides animators fine control over the animation of these parameters. Therefore, it is necessary to describe the order in which these attributes are applied to build the final matrix attribute.

> A transformation matrix is composed of the following components:
>
> * **Scale pivot point** point around which scales are performed \[Sp]
> * **Scale** scaling about x, y, z axes \[S]
> * **Shear** shearing in xy, xz, yx \[Sh]
> * **Scale pivot translation** translation introduced to preserve existing scale transformations when moving pivot. This is used to prevent the object from moving when the objects pivot point is not at the origin and a non-unit scale is applied to the object \[St].
> * **Rotate pivot point** point about which rotations are performed \[Rp]
> * **Rotation orientation** rotation to orient local rotation space \[Ro]
> * **Rotation** rotation \[R]
> * **Rotate pivot translation** translation introduced to preserve exisitng rotate transformations when moving pivot. This is used to prevent the object from moving when the objects pivot point is not at the origin and the pivot is moved. \[Rt]
> * **Translate** translation in x, y, z axes \[T]
>
> Note that the default RotationOrder is kXYZ.
>
> The matrices are post-multiplied in Maya. For example, to transform a point P from object-space to world-space (P') you would need to post-multiply by the worldMatrix. (P' = P x WM)



{% hint style="warning" %}
All transformations in the DAG are affine transformations. All dag node transformations can be represented by a 4x4 transformation matrix where the fourth column contains the vector (0,0,0,1), the fourth row contains the vector (tx, ty, tz, 1) and represents a translational component. This implies objects are transformed by post multiplying their position by the transformation matrix.
{% endhint %}



{% embed url="https://help.autodesk.com/cloudhelp/2015/ENU/Maya-Tech-Docs/Nodes/transform.html" %}
