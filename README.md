#Dynamic Select Box
Select Box with multiple or single select functionality for Dynamic Framework.

## Features
* Open Select Box in modal.
* Dynamic option to act as multiple sector or single selector.
* Manage the click events item click.

## Scrrens
<img src='/screens/dynamic-select-box.gif' width=285px>


## Usage

[Download](http://www.opensourcetechnologies.com/product/dynamic-select-box) the files .


1.  Include `dynamic-select-box.css` in your index.html:
	`<link href="where-you-put-folder/dynamic-select-box/dist/dynamic-select-box.css" rel="stylesheet">`

2.	Include `dynamic-select-box.js` in your index.html:
	`<script type="text/javascript" src="where-you-put-folder/dynamic-select-box/dist/dynamic-select-box.js"></script>`

3.	Add the module `dynamic-select-box` to your application dependencies in your `app.js`:
	`angular.module('starter', ['dynamic', 'dynamic-select-box'])`
	
4.	Configure module:
	`App.config(function(selectboxProvider) {
        selectboxProvider.setTemplateUrl('where-you-put-folder/dynamic-select-box/dist/templates/item-template.html');
        selectboxProvider.setModalTemplateUrl('where-you-put-folder/dynamic-select-box/dist/templates/modal-template.html');
    });`

And you're ready to go.

## Directive

`
    <select-box
      header-text="Header"
      items="data"
      multiple=true
      text-property="value"
      value-property="id"          
      text="Text default Select Box"
      modal-template-url="where-you-put-folder/dynamic-select-box/dist/templates/input-template.html"
      template-url="bower_components/dynamic-multiselect/templates/dist/output-template.html"
      note-text="Note Text"
      value-changed="onValueChanged(value)">
    </select-box>
`
</br>
**Example of template object and event handler of Select Box in controller :**
```javascript
$scope.data = [
	{id: 1, value: "Item 1"},
	{id: 2, value: "Item 2"},
	{id: 3, value: "Item 3"},    
	{id: 4, value: "Item 4"},
	{id: 5, value: "Item 5"},
	{id: 6, value: "Item 6"},
	{id: 7, value: "Item 7"},
	{id: 8, value: "Item 8"}
];
$scope.onValueChanged = function(value){
  console.log(value);
}

```

## Attributes

1. header-text

	Type: String
	Used to specify the text that is shown in the Modal's header bar.

2. Items

	Type: Array
	A list of items that is bound to the select.
3. multiple

	Type: Boolean
	TRUE for for multiple select or FALSE for single select .

4. text-property

	Type: String
	Property description of item the array.

5. value-property

	Type: String
	Property id of item the array.

6. text

	Type: String
	Value default multiselect.

7. modal-template-url

	Type: URL
	An optional URL that can be used to customise the look and feel of the Modal

8. template-url

	Type: URL
	An optional URL that can be used to custom the look and feel of Select Box element.

9. note-text

	Type: String
	An optional note that can be displayed in the default Select Box element.

10. value-changed (Callback)

	Parameters: value - The currently selected value or list of values
	Raised when the current value changes.

Feel Free To Contact Us at [sales@opensourcetechnologies.com](mailto:sales@opensourcetechnologies.com?Subject=Dynamic%20Select%20Box%20plugin)
