# Camunda

## Core concepts

### Form

Contains visual elements.

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

One task definition can have one or more running instances.
An instance can be assigned to one user and can have one of the following state :
* Created
* Completed
* Canceled

For more information, please refer to the graphql documentation : https://docs.camunda.io/assets/files/tasklist-24f4acf1bf3799b067e9e7921749c6b8.graphqls

## User Management Access

Every task instance can be assigned to either a group of people, or a specific individual.
An individual can `claim` a task, indicating that they are picking the task from the pool.

In a Business Process (BPMN or CMMN), Human Tasks should be assigned to groups of people instead of specific individuals.
