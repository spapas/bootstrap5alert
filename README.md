# bootstrap5alert

A simple alert utility similar to sweet-alert. It uses the bootstrap 5 css and javascript. No other requirements beyond bootstrap.

## Installation

Just include it in your project using a `<script>` tag.

## Usage

Just run ``bootstrap5Alert(options)``

where options has the following parameters:

* `message`: The message to display (required)
* `title`: The title to display (default is `Alert`)
* `color`: The color/styling of the alert. By default it is `danger` (i.e red). Other options are `warning`, `info` and `success`.
* `cb`: An optional callback function. If it is defined an action button will be also created that will run the callback when clicked.
* `actionText`: The text to display in the action button (if there's a callback), default is "Ok".

There are also two helpful functions: 

* `confirmDelete(selector)`: Just pass it an selector for a form to display a modal asking you if you want to delete or not. 

* `confirmFormAction(options)`: The options are `{sel, message, title, color}` where the selector is an element selector for a form and the other parameters are the same as for the ``bootstrap5Alert``. It will display an alert and if Yes is pressed it will submit the form. 

## Examples

```
bootstrap5Alert({message: 'Hello, I am an alert!'})
```

![Simple alert](images/simple-alert.png?raw=true "Simple alert")

```
bootstrap5Alert({title: 'More options', message: 'message', color: 'info', cb: () => { console.log("CB") }, actionText: 'Yes' })
```

![More options](images/more-options.png?raw=true "More options")