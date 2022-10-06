# Camunda

## Core concepts

### Form

Contains visual elements of a form.

Structure of a Form is written as a JSON structure :

```
{
  "components": [
    {
      "text": "# File an Invoice\n\nAdd your invoice details below.",
      "type": "text",
      "id": "Field_1b5xinr"
    },
    {
      "key": "creditor",
      "label": "Creditor",
      "type": "textfield",
      "validate": {
        "required": true
      },
      "id": "Field_1xc7rxk"
    }
  ],
  "schemaVersion": 5,
  "exporter": {
    "name": "form-js (https://demo.bpmn.io)",
    "version": "0.9.3"
  },
  "type": "default",
  "id": "Form_1lzgspt"
}
```

### Task definition

Unique Identifier of a task. Used by BPMN or CMMN process to instantiate a task.

### Task instance

Instance of a Task. It can be assigned to one user and can have one of the following state :
* Created
* Completed
* Canceled

For more information, please refer to the graphql documentation : https://docs.camunda.io/assets/files/tasklist-24f4acf1bf3799b067e9e7921749c6b8.graphqls

## User Management Access

Responbility of the CMMN or BPMN workflow to assign the permissions.
The property `candidateGroups` specifies the groups of users that the task can be assigned to.

https://docs.camunda.io/docs/components/modeler/bpmn/user-tasks/