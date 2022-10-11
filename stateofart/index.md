# Human Task Management

Before going further and go though all the existing solutions. 
It is important to understand the main concepts of the `Human Task Management`.

According to the document (http://ceur-ws.org/Vol-847/paper14.pdf), a good `Human Task Management` software must contains the following features :
* Staff resolution : Assign tasks to potentials workers.
* Worker task list : Potential workers can claim one or more tasks.
* Personal task list : List of tasks claimed by one worker.
* Lifecycle : Instanciate one or more `Human Task instance`. Each instance can have one of the following status :
  * New
  * Unassigned
  * Claimed / Assigned
  * Delegated
  * Completed

# State of the art

The table below, gives a quick overview of the existing `Human Task Management` solution.

| Software | Form builder (UI) | Data Management | Create one or more task instance | Staff resolution       | Worker task list | Personal task list 	| Respect Human Task Management concepts | Composite task | Website                                                                                                   |
| -------- | ----------------- | --------------- | -------------------------------- | ---------------------- | -----------------| ------------------ 	| -------------------------------------- | -------------- | --------------------------------------------------------------------------------------------------------- |
| FormIO   | Yes		       | Yes             | No                               | Yes                    | No               | No                    | No                                     | No             | https://www.form.io/                                                                                      |
| Camunda  | Yes               | No              | Yes                              | Yes                    | Yes              | Yes                   | Yes                                    | No             | https://docs.camunda.io/docs/components/best-practices/architecture/understanding-human-tasks-management/ |
| Tallify  | Yes               | Yes             | Yes                              | Yes                    | Yes              | Yes                   | Yes                                    | Yes            | https://tallyfy.com/                                                                                      |
| Pega     | Yes               | Yes             | Yes                              | Yes                    | Yes              | Yes                   | Yes                                    | Yes            | https://www.pega.com/fr                                                                                   |

**Data Management** : When a Form is submitted then data are stored into a database.

**Composite task** : Complex task with substructures are called composite tasks; they can be considered as composition of mulitple (sub tasks).