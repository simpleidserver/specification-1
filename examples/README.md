# Examples

## Hello World

### Task Process Definition

<table>
<tr>
    <th>JSON</th>
    <th>YAML</th>
</tr>
<tr>
<td valign="top">

```json
{
"id": "helloWorld",
"version": "1.0.0",
"specVersion": "0.1",
"name": "Hello world",
"start": "helloWorld",
"steps": [
	{
		"name": "helloWorld",
		"type": "humantask",
		"humantask": "helloWorldTask"
	}
],
"renderingMethods": [{
	"name": "helloWorldRendering",
	"lib": "default",
	"content": {
		"components": {
			"key": "firstName",
			"label": "Firstname",
			"type": "textfield",
			"validate": {
				"required": true
			},
			"id": "Field_firstName"
		}
	}
}],
"humanTasks":[{
	"name": "helloWorldTask",
	"rendering": "helloWorldRendering"
}]
}
```

</td>
<td valign="top">			
</td>
</tr>
</table>

## Two Human Tasks executed in sequence

### Task Process Definition

<table>
<tr>
    <th>JSON</th>
    <th>YAML</th>
</tr>
<tr>
<td valign="top">

```json
{
"id": "twoTasksInSequence",
"version": "1.0.0",
"specVersion": "0.1",
"name": "Two tasks in sequence",
"start": "firstStep",
"steps": [
	{
		"name": "firstStep",
		"type": "humantask",
		"humantask": "firstTask",
		"transition": "secondStep"
	},
	{
		"name": "secondStep",
		"type": "humantask",
		"humantask": "secondTask"
	}
],
"renderingMethods": [{
	"name": "firstTaskRendering",
	"lib": "default",
	"content": {
		"components": {
			"key": "firstName",
			"label": "Firstname",
			"type": "textfield",
			"validate": {
				"required": true
			},
			"id": "Field_firstName"
		}
	}
},{
	"name": "secondTaskRendering",
	"lib": "default",
	"content": {
		"components": {
			"key": "firstName",
			"label": "Firstname",
			"type": "textfield",
			"validate": {
				"required": true
			},
			"id": "Field_firstName"
		}
	}
}],
"humanTasks":[{
	"name": "firstTask",
	"rendering": "firstTaskRendering"
}, {
	"name": "secondTask",
	"rendering": "secondTaskRendering"
}]
}
```

</td>
<td valign="top">			
</td>
</tr>
</table>