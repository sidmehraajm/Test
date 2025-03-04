---
description: 'Level: Beginner | Version 1.0 | Date: 31-Jan-2022 | By - Siddarth Mehra'
---

# 📦 Maya Architecture

## The Architecture & Structure&#x20;

> Maya's true power lies in it's expandability & adaptability. So before we start learning about Rigging we need to understand how Maya is working under the hood.&#x20;
>
> Maya uses a Node based Architecture, meaning anything and everything in a scene is a node. Meaning that every time we do something in maya it may be executing a command or creating something, all of that tells maya to create some kind of node and some connections .



## Dag And Dag Hierarchy

> DAG stands for directed acyclic graph. In essence, the DAG is a breakdown of how an instance of an object is constructed from a piece of geometry. The DAG hierarchy (also known as an object hierarchy) refers to the parent-child relationships of all nodes that make up an object.&#x20;
>
> An object's DAG hierarchy always includes two types of nodes, transforms and shapes.

{% embed url="https://youtu.be/y9pqG2wYiLQ" %}

> When you create a polygon sphere, for example, you can see in the Attribute Editor that it includes a shape node and a transform node. The shape node has attributes to define the geometry, while the transform node contains attributes that control the sphere's position, scale, or rotation. The shape node is the child of the transform node.

![](../.gitbook/assets/asf.gif)

## DG or Dependency Graph

> The dependency graph (DG) is a collection of entities connected together. Unlike the DAG, these connections can be cyclic, and do not represent a parenting relationship. Instead, the connections in the graph allow data to move from one entity in the graph to another. Dependency graph nodes are used for almost everything in Maya such as model creation, deformation, animation, simulation, and audio processing.

![](<../.gitbook/assets/DG cycle.gif>)

> Most objects in Maya are dependency graph nodes, or networks of nodes (several nodes connected together). For example, DAG nodes are dependency graph nodes, and shaders are networks of nodes.

{% embed url="https://youtu.be/_l9oM7sx_98" %}

### Transformation Hierarchy (DAG)

The transformation hierarchy or DAG (Directed Acyclic Graph) is a hierarchy where objects are defined relative to the transformations on their parent objects. These objects are dependency nodes and are referred to as dag nodes. There are basically two types of dag nodes: transforms and shapes. Transform nodes are grouping nodes that can have any number of other dag nodes below them. Transform nodes have affine transformation information which is applied to nodes below them. Shape nodes are leaf level nodes and cannot have any other nodes below them. Shape nodes must have at least one transform node as a parent. Dag nodes can have more than one parent. That is, they can be in more than one hierarchy. This makes the transformation hierarchy a graph instead of a tree. Dag nodes that are in more than one hierarchy are said to be "instanced".

{% embed url="https://help.autodesk.com/cloudhelp/2015/ENU/Maya-Tech-Docs/Nodes/dagNode.html" %}
