# Pega

## Core concepts

### Work group

A work group identifies a cross-functional team that contains a manager, a set of operators and a work queue.
You create work groups so that resources can be shared among units, divisions, or the entire organization.

### Work basket and worklist

Application supports two models for distributing work : 
* Worklists
* Workbaskets

Both contain prioritized lists of assignments.
An assignment records the condition of an open work object within a flow, and the action required (by a user or an external system) for the work object to progress.
Assignments are created and prioritized by a flow operating on a work object but are not themselves part of the work object.

**Worklist**, automatically created for each operator ID (user), is a prioritized list of assignments for that user. 

**Workbasket** is a shared pool of assignments from which users can select work.