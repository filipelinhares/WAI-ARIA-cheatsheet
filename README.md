# WAI-ARIA cheatsheet
Accessible Rich Internet Applications (ARIA) defines ways to make Web content and Web applications (especially those developed with Ajax and JavaScript) more accessible to people with disabilities. For example, ARIA enables accessible navigation landmarks, JavaScript widgets, form hints and error messages, live content updates, and more.  
*- Source [MDN](https://developer.mozilla.org/pt-BR/docs/Web/Accessibility/ARIA)*

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
| token                | token list |


#### Widget attributes
- aria-autocomplete
- aria-checked ***(state)***
- aria-disabled ***(state)***
- aria-expanded ***(state)***
- aria-haspopup
- aria-hidden ***(state)***
- aria-invalid ***(state)***
- aria-label
- aria-level
- aria-multiline
- aria-multiselectable
- aria-orientation
- aria-pressed ***(state)***
- aria-readonly
- aria-required
- aria-selected ***(state)***
- aria-sort
- aria-valuemax
- aria-valuemin
- aria-valuenow
- aria-valuetext

#### Live region attributes
- aria-atomic
- aria-busy ***(state)***
- aria-live
- aria-relevant

#### Drag-and-Drop Attributes
- aria-dropeffect
- aria-grabbed ***(state)***

#### Relationship Attributes
- aria-activedescendant
- aria-controls
- aria-describedby
- aria-flowto
- aria-labelledby
- aria-owns
- aria-posinset
- aria-setsize

## License
[MIT](LICENSE.md) © Filipe Linhares
