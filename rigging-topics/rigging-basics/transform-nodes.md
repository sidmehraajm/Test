---
description: 'Level: Beginner | Version 1.0 | Date: 21-Feb-2022 | By - Siddarth Mehra'
---

# ☦ Transform Nodes

## Transforms (A Rigger's right hand)

> Transform nodes are [**dagNodes** ](transform-nodes.md#dag-and-dag-hierarchy)that are used to group and transform other dagNodes. \
> Even though when _**Shapes**_ is switched off in Outliner It seems like the transform node ICON changes and looks like it's , But we need to understand that-\
> **All dagNodes that are not transform nodes in Maya must exist as a child of some transform node**. For example a Sphere shape has to be under a tranform node always.

![](../../.gitbook/assets/maya\_cgzPWEp8ty.gif)

### Mysterious Transform Icons in Maya

{% hint style="success" %}
Maya Transform nodes can be confusing at the start because of how it displays the icons For example If we had a Transform, a locator, a Camera & a Mesh.\
Whichever is the _**First Child DAG Node**_ that _**Child's Shape**_ will be shown as the icon of that transform
{% endhint %}

![](../../.gitbook/assets/maya\_3BkxPrmk2Y.gif)

### Local Space & World Space



### Transformation MATRIX

> Transformation Matrix (DAG) transform nodes have many attributes that make up the final transformation matrix as represented by the matrix attribute. This breakdown provides animators fine control over the animation of these parameters. Therefore, it is necessary to describe the order in which these attributes are applied to build the final matrix attribute.

{% embed url="https://help.autodesk.com/cloudhelp/2015/ENU/Maya-Tech-Docs/Nodes/transform.html" %}
