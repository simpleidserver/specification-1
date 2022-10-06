# Form.IO

## Core Concepts

### Resources

Resources are the `structured` data objects that support your application. 
Anything that has a static data structure can be defined as a `Resource`. 

### Forms

Represent the `unstructured` data that is used to supplement a Resource. 
For example, a `Customer Survey` may have free-form questions (fields) like `Did-you enjoy your visit`? and those three-form fields should be associated to the customer who submitted it.
A `Customer Survey` would be a `Form` that references the `Customer` resource.

## User Management Access

Roles and Permissions allow users to be granted certain permissions to perform certain actions and have access to forms and submissions within a project.

There are different roles:

* **Manager** : User with this role can manage other users.
* **Associate** : A user who has access to read all submission data, but cannot create new records or manage other users.
* **Anonymous** : A special role granted to users who are not authenticated.
* **Authenticated** : A special role granted to users who are authenticated.
* **Admin** : A user who has access to everything within a single project.

## Actions

Actions executed when a form is submitted. For example, you can authenticate a user account against your User Resource, send an email or fire off a webhook to send the data to an external system.

## Types of Form

There are different types of Form

### Form

Form is displayed in one page.

### Wizard

Form is displayed in multiple pages.

### PDF

Take any existing PDF form document and convert it into a Javascript Powered HTML webform.
