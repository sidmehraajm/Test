---
description: 'Level: Beginner | Version 1.0 | Date: 30-March-2022 | By - Siddarth Mehra'
---

# 🏢 Transform Node Attributes

### 1. translate(t) - _<mark style="color:green;">double3</mark>_

* translateX (tx) - _<mark style="color:green;">double</mark>_
* translateY (ty) - _<mark style="color:green;">double</mark>_
* translateZ (tz) - _<mark style="color:green;">double</mark>_

<details>

<summary>Translation is used to move a dag node from one position to another in a 3D space</summary>

* <mark style="color:green;">Is Keyable</mark>&#x20;
* <mark style="color:green;"></mark>![](<../../../.gitbook/assets/image (5).png>)

translation can be seen in channelBox and can be queried by -

```
import pymel.core as pm
obj = pm.PyNode('objName')
obj.getTranslation()
```

</details>
