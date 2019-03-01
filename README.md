# WAI-ARIA cheatsheet
Accessible Rich Internet Applications (ARIA) defines ways to make Web content and Web applications (especially those developed with Ajax and JavaScript) more accessible to people with disabilities. For example, ARIA enables accessible navigation landmarks, JavaScript widgets, form hints and error messages, live content updates, and more.  
*- Source [MDN](https://developer.mozilla.org/pt-BR/docs/Web/Accessibility/ARIA)*

- [Roles](#roles)
  - [Widget roles](#widget-roles)
    - [alert](#alert)
    - [alertdialog](#alertdialog)
    - [button](#button)
    - [checkbox](#checkbox)
    - [dialog](#dialog)
    - [gridcell](#gridcell)
    - [link](#link)
    - [log](#log)
    - [marquee](#marquee)
    - [menuitem](#menuitem)
    - [menuitemcheckbox](#menuitemcheckbox)
    - [menuitemradio](#menuitemradio)
    - [option](#option)
    - [progressbar](#progressbar)
    - [radio](#radio)
    - [scrollbar](#scrollbar)
    - [slider](#slider)
    - [spinbutton](#spinbutton)
    - [status](#status)
    - [tab](#tab)
    - [tabpanel](#tabpanel)
    - [textbox](#textbox)
    - [timer](#timer)
    - [tooltip](#tooltip)
    - [treeitem](#treeitem)
    - [combobox](#combobox)
    - [grid](#grid)
    - [listbox](#listbox)
    - [menu](#menu)
    - [menubar](#menubar)
    - [radiogroup](#radiogroup)
    - [tablist](#tablist)
    - [tree](#tree)
    - [treegrid](#treegrid)
  - [Document structure roles](#document-structure-roles)
    - [article](#article)
    - [columnheader](#columnheader)
    - [definition](#definition)
    - [directory](#directory)
    - [document](#document)
    - [group](#group)
    - [heading](#heading)
    - [img](#img)
    - [list](#list)
    - [listitem](#listitem)
    - [math](#math)
    - [note](#note)
    - [presentation](#presentation)
    - [region](#region)
    - [row](#row)
    - [rowgroup](#rowgroup)
    - [rowheader](#rowheader)
    - [separator](#separator)
    - [toolbar](#toolbar)
  - [Landmark roles](#landmark-roles)
    - [application](#application)
    - [banner](#banner)
    - [complementary](#complementary)
    - [contentinfo](#contentinfo)
    - [form](#form)
    - [main](#main)
    - [navigation](#navigation)
    - [search](#search)
- [State and properties](#state-and-properties)
  - [Potential Value Types](#potential-value-types)
  - [Widget attributes](#widget-attributes)
    - [aria-autocomplete](#aria-autocomplete)
    - [aria-checked - *(state)*](#aria-checked---state)
    - [aria-current - *(state)*](#aria-current---state)
    - [aria-disabled - *(state)*](#aria-disabled---state)
    - [aria-expanded - *(state)*](#aria-expanded---state)
    - [aria-haspopup](#aria-haspopup)
    - [aria-hidden - *(state)*](#aria-hidden---state)
    - [aria-invalid - *(state)*](#aria-invalid---state)
    - [aria-label](#aria-label)
    - [aria-level](#aria-level)
    - [aria-multiline](#aria-multiline)
    - [aria-multiselectable](#aria-multiselectable)
    - [aria-orientation](#aria-orientation)
    - [aria-pressed - *(state)*](#aria-pressed---state)
    - [aria-readonly](#aria-readonly)
    - [aria-required](#aria-required)
    - [aria-selected - *(state)*](#aria-selected---state)
    - [aria-sort](#aria-sort)
    - [aria-valuemax](#aria-valuemax)
    - [aria-valuemin](#aria-valuemin)
    - [aria-valuenow](#aria-valuenow)
    - [aria-valuetext](#aria-valuetext)
  - [Live region attributes](#live-region-attributes)
    - [aria-atomic](#aria-atomic)
    - [aria-busy - *(state)*](#aria-busy---state)
    - [aria-live](#aria-live)
    - [aria-relevant](#aria-relevant)
  - [Drag-and-Drop Attributes](#drag-and-drop-attributes)
    - [aria-dropeffect](#aria-dropeffect)
    - [aria-grabbed](#aria-grabbed)
  - [Relationship Attributes](#relationship-attributes)
    - [aria-activedescendant](#aria-activedescendant)
    - [aria-controls](#aria-controls)
    - [aria-describedby](#aria-describedby)
    - [aria-flowto](#aria-flowto)
    - [aria-labelledby](#aria-labelledby)
    - [aria-owns](#aria-owns)
    - [aria-posinset](#aria-posinset)
    - [aria-setsize](#aria-setsize)

## Roles
ARIA allows developers to declare a semantic **role** for an element that otherwise offers incorrect or no semantics. For example, when an unordered list is used to create a menu, the `<ul>` should be given a **role** of menubar and each `<li>` should be given a **role** of menuitem.

The role of an element should not change. Instead, remove the original element and replace it with an element with the new role.

### Widget roles

The following roles act as standalone user interface widgets or as part of larger, composite widgets.

#### alert
A message with important, and usually time-sensitive, information. See related alertdialog and status.

#### alertdialog
A type of dialog that contains an alert message, where initial focus goes to an element within the dialog. See related alert and dialog.

#### button
An input that allows for user-triggered actions when clicked or pressed. See related link.
> HTML related: `<button>, <input type="submit">, <input type="reset">, <input type="image">`

#### checkbox
A checkable input that has three possible values: true, false, or mixed

> HTML related: `<input type="checkbox">`

#### dialog
A dialog is an application window that is designed to interrupt the current processing of an application in order to prompt the user to enter information or require a response. See related alertdialog.

#### gridcell  
A cell in a grid or treegrid.
> HTML related: `<td>`

#### link
An interactive reference to an internal or external resource that, when activated, causes the user agent to navigate to that resource. See related button.
> HTML related: `<a href...>, <area>`

#### log
A type of live region where new information is added in meaningful order and old information may disappear. See related marquee.
> Note: Elements with the role log have an implicit aria-live value of polite.

#### marquee
A type of live region where non-essential information changes frequently. See related log.
> Note: Elements with the role marquee maintain the default aria-live value of off.

#### menuitem
An option in a group of choices contained by a menu or menubar.

#### menuitemcheckbox
A checkable menuitem that has three possible values: true, false, or mixed.

#### menuitemradio
A checkable menuitem in a group of menuitemradio roles, only one of which can be checked at a time.

#### option
A selectable item in a select list.
> HTML related: `<option>`

#### progressbar
An element that displays the progress status for tasks that take a long time.
> HTML related: `<progress>`
> Note: Elements with the role progressbar have an implicit aria-readonly value of true.

#### radio
A checkable input in a group of radio roles, only one of which can be checked at a time.
> HTML related: `<input type="radio">`

#### scrollbar
A graphical object that controls the scrolling of content within a viewing area, regardless of whether the content is fully displayed within the viewing area.
> Note: Elements with the role progressbar have an implicit aria-readonly value of true.

#### slider
A user input where the user selects a value from within a given range.
> HTML related: `<input type="range">`

#### spinbutton
A form of range that expects the user to select from among discrete choices.
> HTML related: input element with a type attribute in the Number state

#### status
A container whose content is advisory information for the user but is not important enough to justify an alert, often but not necessarily presented as a status bar. See related alert.
> HTML related: `<output>`
> Note: Elements with the role status have an implicit aria-live value of polite.

#### tab
A grouping label providing a mechanism for selecting the tab content that is to be rendered to the user.

#### tabpanel
A container for the resources associated with a tab, where each tab is contained in a tablist.

#### textbox
nput that allows free-form text as its value.
> HTML related: `<textarea>, <input type="text">` (and other text-like inputs, such as 'password', 'email', etc.).

#### timer
A type of live region containing a numerical counter which indicates an amount of elapsed time from a start point, or the time remaining until an end point.

#### tooltip
A contextual popup that displays a description for an element.

#### treeitem
An option item of a tree. This is an element within a tree that may be expanded or collapsed if it contains a sub-level group of treeitems.

* * *
**The following roles act as composite user interface widgets. These roles typically act as containers that manage other, contained widgets.**

#### combobox
A presentation of a select; usually similar to a textbox where users can type ahead to select an option, or type to enter arbitrary text as a new item in the list. See related listbox.
> HTML related: `<select>`, HTML5 input types which provide suggestions

#### grid
A grid is an interactive control which contains cells of tabular data arranged in rows and columns, like a table.
> HTML related: `<table>`

#### listbox
A widget that allows the user to select one or more items from a list of choices. See related combobox and list.
> HTML related: `<select>, <datalist>` (when aria-multiselectable set to false on listbox)

#### menu
A type of widget that offers a list of choices to the user.
HTML related: `<menu type="list">`

#### menubar
A presentation of menu that usually remains visible and is usually presented horizontally.

#### radiogroup
A group of radio buttons.

#### tablist
A list of tab elements, which are references to tabpanel elements.

#### tree
A type of list that may contain sub-level nested groups that can be collapsed and expanded.

#### treegrid
A grid whose rows can be expanded and collapsed in the same manner as for a tree.

* * *

### Document structure roles

The following roles describe structures that organize content in a page. Document structures are not usually interactive.

#### article
A section of a page that consists of a composition that forms an independent part of a document, page, or site.
> HTML related: `<article>`

#### columnheader
A cell containing header information for a column.
> HTML related: `<th scope="col">`

#### definition
A definition of a term or concept.

#### directory
A list of references to members of a group, such as a static table of contents.

#### document
A region containing related information that is declared as document content, as opposed to a web application.
> HTML related: `<body>`

#### group
A set of user interface objects which are not intended to be included in a page summary or table of contents by assistive technologies.
> HTML related: `<fieldset>, <optgroup>`

#### heading
A heading for a section of the page.
> HTML related: `<h1>, <h2>, etc.`
> Note: aria-level must be set appropriately

#### img
A container for a collection of elements that form an image.
> HTML related: `<img>`

#### list
A group of non-interactive list items. See related listbox.
> HTML related: `<ul>, <ol>`

#### listitem
A single item in a list or directory.
> HTML related: `<li>`

#### math
Content that represents a mathematical expression.

#### note
A section whose content is parenthetic or ancillary to the main content of the resource.

#### presentation
An element whose implicit native role semantics will not be mapped to the accessibility API.
> HTML related: `alt=""`

#### region
A large perceivable section of a web page or document, that the author feels is important enough to be included in a page summary or table of contents, for example, an area of the page containing live sporting event statistics.
> HTML related: `<div>, <frame>, <section>`

#### row
A row of cells in a grid.
> HTML related: `<tr>`

#### rowgroup
A group containing one or more row elements in a grid.
> HTML related: `<thead>, <tfoot>, <tbody>`

#### rowheader
A cell containing header information for a row in a grid.
> HTML related: `<th scope="row">`

#### separator
A divider that separates and distinguishes sections of content or groups of menuitems.
> HTML related: `<hr>`

#### toolbar
A collection of commonly used function buttons represented in compact visual form.
> HTML related: `<menu type="toolbar">`

* * *

### Landmark roles

The following roles are regions of the page intended as navigational landmarks.

#### application
A region declared as a web application, as opposed to a web document.

#### banner
A region that contains mostly site-oriented content, rather than page-specific content.
> HTML related: `<header>, <div class="header">`

#### complementary
A supporting section of the document, designed to be complementary to the main content at a similar level in the DOM hierarchy, but remains meaningful when separated from the main content.
> HTML related: `<aside>`

#### contentinfo
A large perceivable region that contains information about the parent document.
> HTML related: `<footer>`]

#### form
A landmark region that contains a collection of items and objects that, as a whole, combine to create a form. See related search
> HTML related: `<form>`

#### main
The main content of a document.
> HTML related: `<main>, <div class="content">`

#### navigation
A collection of navigational elements (usually links) for navigating the document or related documents.
> HTML related: `<nav>`

#### search
A landmark region that contains a collection of items and objects that, as a whole, combine to create a search facility. See related form.

## State and properties
### Potential Value Types
| Value                | Description |
|----------------------|-------------|
| true/false           | Value representing either true or false, with a default "false" value. |
| tristate             | Value representing true or false, with an intermediate "mixed" value. Default value is "false" unless otherwise specified |
| true/false/undefined | Value representing true or false, with a default "undefined" value indicating the state or property is not relevant. |
| ID reference         | Reference to the ID of another element in the same document |
| ID reference list    | A list of one or more ID references. |
| integer              | A numerical value without a fractional component. |
| number               | Any real numerical value. |
| string               | Unconstrained value type. |
| token                | One of a limited set of allowed values. |

* * *

### Widget attributes

#### aria-autocomplete
Indicates whether user input completion suggestions are provided.  
Values: `<element aria-autocomplete="inline|list|both|none" ... />`

| Value | Condition |
|--------|--------|
|   inline     |    The system provides text after the caret as a suggestion for how to complete the field.    |
|    list    |    A list of choices appears from which the user can choose, but the edit box retains focus.    |
|    both    |    A list of choices appears and the currently selected suggestion also appears inline.    |
|    none    |    No input completion suggestions are provided.    |

#### aria-checked - *(state)*
Indicates the current "checked" state of checkboxes, radio buttons, and other widgets. See related aria-pressed and aria-selected.  
Values: `<element aria-checked="true|false|mixed" ... >`

| Value | Condition |
|--------|--------|
|   true     |    The element is selected.    |
|    false    |    The element is not selected.    |
|    mixed    |    The element indicates both selected and unselected states.    |

#### aria-current - *(state)*
Indicates the element that represents the current item within a container or set of related elements. The aria-current attribute is used when an element within a set of related elements is visually styled to indicate it is the current item in the set.  
Values: `<element aria-current="page|step|location|date|time|true|false" ... >`

| Value | Condition |
|--------|--------|
| page | Represents the current page within a set of pages. |
| step | Represents the current step within a process. |
| location | Represents the current location within an environment or context. |
| date | Represents the current date within a collection of dates. |
| time | Represents the current time within a set of times. |
| true | Represents the current item within a set. |
| false | (default) 	Does not represent the current item within a set. |

#### aria-disabled - *(state)*
Indicates that the element is perceivable but disabled, so it is not editable or otherwise operable. See related aria-hidden and aria-readonly.  
Values: `<element aria-disabled="true|false" ... >`

#### aria-expanded - *(state)*
Indicates whether the element, or another grouping element it controls, is currently expanded or collapsed.  
Values: `<element aria-expanded="true|false|undefined" ... >`

#### aria-haspopup
Indicates that the element has a popup context menu or sub-level menu.  
Values: `<element aria-haspopup="true|false" ... >`

#### aria-hidden - *(state)*
Indicates that the element and all of its descendants are not visible or perceivable to any user as implemented by the author. See related aria-disabled.  
Values: `<element aria-hidden="true|false" ... >`

#### aria-invalid - *(state)*
Indicates the entered value does not conform to the format expected by the application.  
Values: `<element aria-invalid="true|false|grammar|spelling" ... >`

| Value | Condition |
|--------|--------|
|   true     |    The element is selected.    |
|    false    |    The element is not selected.    |
|    grammar    |    A grammatical error has been detected.    |
|spelling | A spelling error has been detected. |

#### aria-label
Defines a string value that labels the current element. See related aria-labelledby.  
Values: `<element aria-label="string" ... >`

#### aria-level
Defines the hierarchical level of an element within a structure.  
Values: `<element aria-level="integer" ... >`

#### aria-multiline
Indicates whether a text box accepts multiple lines of input or only a single line.  
Values: `<element aria-multiline="true|false" ... >`

#### aria-multiselectable
Indicates that the user may select more than one item from the current selectable descendants.  
Values: `<element aria-multiselectable="true|false" ... >`

#### aria-orientation
Indicates whether the element and orientation is horizontal or vertical.  
Values: `<element aria-orientation="true|false" ... >`

| Value | Condition |
|--------|--------|
|   vertical     |    The element is oriented vertically.    |
|    horizontal(default)    |    The element is not selected.    |
|    grammar    |    The element is oriented horizontally.    |

#### aria-pressed - *(state)*
Indicates the current "pressed" state of toggle buttons. See related aria-checked and aria-selected.  
Values: `<element aria-pressed="true|false|mixed" ... >`

#### aria-readonly
Indicates that the element is not editable, but is otherwise operable. See related aria-disabled.  
Values: `<element aria-readonly="true|false" ... >`

#### aria-required
Indicates that user input is required on the element before a form may be submitted.  
Values: `<element aria-required="true|false" ... >`

#### aria-selected - *(state)*
Indicates the current "selected" state of various widgets. See related aria-checked and aria-pressed.  
Values: `<element aria-selected="true|false|undefined" ... >`

#### aria-sort
Indicates if items in a table or grid are sorted in ascending or descending order.  
Values: `<element aria-sort="ascending|descending|none|other" ... />`

| Value | Condition |
|--------|--------|
|   ascending     |    Items are sorted in ascending order by this column.    |
|    descending    |    Items are sorted in descending order by this column.   |
|    none    |    There is no defined sort applied to the column.    |
|   other | A sort algorithm other than ascending or descending has been applied.|

#### aria-valuemax
Defines the maximum allowed value for a range widget.  
Values: `<element aria-valuemax="number" ... />`

#### aria-valuemin
Defines the minimum allowed value for a range widget.  
Values: `<element aria-valuemin="number" ... />`

#### aria-valuenow
Defines the current value for a range widget. See related aria-valuetext.  
Values: `<element aria-valuenow="number" ... />`

#### aria-valuetext
Defines the human readable text alternative of aria-valuenow for a range widget.  
Values: `<element aria-valuetext="integer" ... />`

* * *

### Live region attributes

#### aria-atomic
Indicates whether assistive technologies will present all, or only parts of, the changed region based on the change notifications defined by the aria-relevant attribute. See related aria-relevant.  
Values: `<element aria-atomic="true|false" ... />`

#### aria-busy - *(state)*
Indicates whether an element, and its subtree, are currently being updated.  
Values: `<element aria-busy="true|false" ... />`

#### aria-live
Indicates that an element will be updated, and describes the types of updates the user agents, assistive technologies, and user can expect from the live region.  
Values: `<element aria-live="off|polite|assertive" ... />`

| Value | Condition |
|--------|--------|
|off | Default. Updates should not be announced. |
|polite | Updates should only be announced if the user is idle.	  |
|assertive | Updates should be announced to the user as soon as possible. |

#### aria-relevant
Indicates what user agent change notifications (additions, removals, etc.) assistive technologies will receive within a live region. See related aria-atomic.  
Values: `<element aria-relevant="additions|removals|text|all|additions text:" ... />`

| Value | Condition |
|--------|--------|
|additions | Element nodes are added to the DOM within the live region. |
|removals | Text or element nodes within the live region are removed from the DOM.	  |
|text | Text is added to any DOM descendant nodes of the live region. |
|all| Equivalent to the combination of all values, "additions removals text". |
|additions text(default)| Equivalent to the combination of values, "additions text". |
* * *

### Drag-and-Drop Attributes
#### aria-dropeffect
Indicates what functions can be performed when the dragged object is released on the drop target. This allows assistive technologies to convey the possible drag options available to users, including whether a pop-up menu of choices is provided by the application. Typically, drop effect functions can only be provided once an object has been grabbed for a drag operation as the drop effect functions available are dependent on the object being dragged.  
Values: `<element aria-grabbed="copy|move|link|execute|popup|none" ... />`

| Value | Condition |
|--------|----------|
| copy | A duplicate of the source object will be dropped into the target. |
| move | The source object will be removed from its current location and dropped into the target. |
| link | A reference or shortcut to the dragged object will be created in the target object. |
| execute | A function supported by the drop target is executed, using the drag source as an input. |
| popup | There is a popup menu or dialog that allows the user to choose one of the drag operations (copy, move, link, execute) and any other drag functionality, such as cancel. |
| none | No operation can be performed; effectively cancels the drag operation if an attempt is made to drop on this object. Ignored if combined with any other token value. e.g. 'none copy' is equivalent to a 'copy' value. |


#### aria-grabbed
Indicates an element's "grabbed" state in a drag-and-drop operation.  
Values: `<element aria-grabbed="true|false|undefined" ... />`

* * *

### Relationship Attributes

#### aria-activedescendant
Identifies the currently active descendant of a composite widget. Used to deal with multiple focusable children, ie. in a tree menu.  
Values: `<element aria-activedescendant="#id-reference" ... />`

#### aria-controls
Identifies the element (or elements) whose contents or presence are controlled by the current element. See related aria-owns. Announced for form controls.  
Values: `<element aria-controls="#id-reference" ... />`

#### aria-describedby
Identifies the element (or elements) that describes the object. See related aria-labelledby.  
Values: `<element aria-describedby="#id-reference" ... />`

#### aria-flowto
Identifies the next element (or elements) in an alternate reading order of content which, at the user's discretion, allows assistive technology to override the general default of reading in document source order.  
Values: `<element aria-flowto="#id-reference" ... />`

#### aria-labelledby
Identifies the element (or elements) that labels the current element. See related aria-label and aria-describedby.  
Values: `<element aria-labelledby="#id-reference" ... />`

#### aria-owns
Identifies an element (or elements) in order to define a visual, functional, or contextual parent/child relationship between DOM elements where the DOM hierarchy cannot be used to represent the relationship. See related aria-controls.  
Values: `<element aria-owns="#id-reference" ... />`

#### aria-posinset
Defines an element's number or position in the current set of listitems or treeitems. Not required if all elements in the set are present in the DOM. See related aria-setsize.  
Values: `<element aria-posinset="integer" ... />`

#### aria-setsize
Defines the number of items in the current set of listitems or treeitems. Not required if all elements in the set are present in the DOM. See related aria-posinset.  
Values: `<element aria-setsize="integer" ... />`

## License
[MIT](LICENSE.md) © Filipe Linhares
