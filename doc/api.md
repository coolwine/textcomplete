<!-- Generated by documentation.js. Update this documentation by updating the source code. -->

### Table of Contents

-   [Completer](#completer)
    -   [destroy](#destroy)
    -   [registerStrategy](#registerstrategy)
    -   [run](#run)
-   [DropdownItemOptions](#dropdownitemoptions)
-   [DropdownItem](#dropdownitem)
    -   [destroy](#destroy-1)
    -   [appended](#appended)
    -   [activate](#activate)
    -   [next](#next)
    -   [prev](#prev)
-   [DropdownOptions](#dropdownoptions)
-   [Dropdown](#dropdown)
    -   [destroy](#destroy-2)
    -   [render](#render)
    -   [deactivate](#deactivate)
    -   [select](#select)
    -   [up](#up)
    -   [down](#down)
    -   [getActiveItem](#getactiveitem)
-   [CursorOffset](#cursoroffset)
-   [Editor](#editor)
    -   [destroy](#destroy-3)
    -   [applySearchResult](#applysearchresult)
    -   [getCursorOffset](#getcursoroffset)
    -   [getBeforeCursor](#getbeforecursor)
    -   [emitMoveEvent](#emitmoveevent)
    -   [emitEnterEvent](#emitenterevent)
    -   [emitChangeEvent](#emitchangeevent)
    -   [emitEscEvent](#emitescevent)
    -   [getCode](#getcode)
-   [Query](#query)
    -   [execute](#execute)
    -   [build](#build)
-   [SearchResult](#searchresult)
-   [StrategyProperties](#strategyproperties)
-   [Strategy](#strategy)
    -   [destroy](#destroy-4)
    -   [replace](#replace)
-   [Textarea](#textarea)
    -   [destroy](#destroy-5)
    -   [applySearchResult](#applysearchresult-1)
    -   [getCursorOffset](#getcursoroffset-1)
    -   [getBeforeCursor](#getbeforecursor-1)
-   [TextcompleteOptions](#textcompleteoptions)
-   [Textcomplete](#textcomplete)
    -   [destroy](#destroy-6)
    -   [hide](#hide)
    -   [register](#register)
    -   [trigger](#trigger)

## Completer

**Extends EventEmitter**

Complete engine.

### destroy

Returns **this** 

### registerStrategy

Register a strategy to the completer.

**Parameters**

-   `strategy` **[Strategy](#strategy)** 

Returns **this** 

### run

**Parameters**

-   `text` **[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)** Head to input cursor.

Returns **void** 

## DropdownItemOptions

Type: {className: [string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)?}

**Properties**

-   `className` **[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)?** 

## DropdownItem

Encapsulate an item of dropdown.

**Parameters**

-   `searchResult` **[SearchResult](#searchresult)** 
-   `options` **[DropdownItemOptions](#dropdownitemoptions)** 

### destroy

Try to free resources and perform other cleanup operations.

### appended

-   **See: Dropdown#append**

Callbacked when it is appended to a dropdown.

**Parameters**

-   `dropdown` **[Dropdown](#dropdown)** 

### activate

Deactivate active item then activate itself.

Returns **this** 

### next

Get the next sibling.

Returns **[DropdownItem](#dropdownitem)?** 

### prev

Get the previous sibling.

Returns **[DropdownItem](#dropdownitem)?** 

## DropdownOptions

Type: {className: [string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)?, footer: function (any): ([string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String) \| [string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String))?, header: function (any): ([string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String) \| [string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String))?, maxCount: [number](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number)?, placement: [string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)?, rotate: [boolean](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Boolean)?, style: {}?, item: [DropdownItemOptions](#dropdownitemoptions)?}

**Properties**

-   `className` **[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)?** 
-   `footer` **function (any): ([string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String) \| [string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String))?** 
-   `header` **function (any): ([string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String) \| [string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String))?** 
-   `maxCount` **[number](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number)?** 
-   `placement` **[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)?** 
-   `rotate` **[boolean](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Boolean)?** 
-   `style` **{}?** 
-   `item` **[DropdownItemOptions](#dropdownitemoptions)?** 

## Dropdown

**Extends EventEmitter**

Encapsulate a dropdown view.

**Parameters**

-   `options` **[DropdownOptions](#dropdownoptions)** 

**Properties**

-   `shown` **[boolean](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Boolean)** Whether the #el is shown or not.
-   `items` **[Array](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array)&lt;[DropdownItem](#dropdownitem)>** The array of rendered dropdown items.

### destroy

Returns **this** 

### render

Render the given data as dropdown items.

**Parameters**

-   `searchResults` **[Array](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array)&lt;[SearchResult](#searchresult)>** 
-   `cursorOffset` **[CursorOffset](#cursoroffset)** 

Returns **this** 

### deactivate

Hide the dropdown then sweep out items.

Returns **this** 

### select

**Parameters**

-   `dropdownItem` **[DropdownItem](#dropdownitem)** 

Returns **this** 

### up

**Parameters**

-   `e` **[CustomEvent](https://developer.mozilla.org/docs/Web/API/CustomEvent/CustomEvent)** 

Returns **this** 

### down

**Parameters**

-   `e` **[CustomEvent](https://developer.mozilla.org/docs/Web/API/CustomEvent/CustomEvent)** 

Returns **this** 

### getActiveItem

Retrieve the active item.

Returns **([DropdownItem](#dropdownitem) | null)** 

## CursorOffset

Type: {lineHeight: [number](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number), top: [number](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number), left: [number](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number)?, right: [number](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number)?}

**Properties**

-   `lineHeight` **[number](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number)** 
-   `top` **[number](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number)** 
-   `left` **[number](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number)?** 
-   `right` **[number](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number)?** 

## Editor

**Extends EventEmitter**

Abstract class representing a editor target.

Editor classes must implement `#applySearchResult`, `#getCursorOffset` and
`#getBeforeCursor` methods.

Editor classes must invoke `#emitMoveEvent`, `#emitEnterEvent`,
`#emitChangeEvent` and `#emitEscEvent` at proper timing.

### destroy

It is called when associated textcomplete object is destroyed.

Returns **this** 

### applySearchResult

It is called when a search result is selected by a user.

**Parameters**

-   `_` **[SearchResult](#searchresult)** 

Returns **void** 

### getCursorOffset

The input cursor's absolute coordinates from the window's left
top corner.

Returns **[CursorOffset](#cursoroffset)** 

### getBeforeCursor

Editor string value from head to cursor.
Returns null if selection type is range not cursor.

Returns **[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)?** 

### emitMoveEvent

-   **See: [Textarea](#textarea) for live example.**

Emit a move event, which moves active dropdown element.
Child class must call this method at proper timing with proper parameter.

**Parameters**

-   `code` **(`"UP"` \| `"DOWN"`)** 

Returns **[CustomEvent](https://developer.mozilla.org/docs/Web/API/CustomEvent/CustomEvent)** 

### emitEnterEvent

-   **See: [Textarea](#textarea) for live example.**

Emit a enter event, which selects current search result.
Child class must call this method at proper timing.

Returns **[CustomEvent](https://developer.mozilla.org/docs/Web/API/CustomEvent/CustomEvent)** 

### emitChangeEvent

-   **See: [Textarea](#textarea) for live example.**

Emit a change event, which triggers auto completion.
Child class must call this method at proper timing.

Returns **[CustomEvent](https://developer.mozilla.org/docs/Web/API/CustomEvent/CustomEvent)** 

### emitEscEvent

-   **See: [Textarea](#textarea) for live example.**

Emit a esc event, which hides dropdown element.
Child class must call this method at proper timing.

Returns **[CustomEvent](https://developer.mozilla.org/docs/Web/API/CustomEvent/CustomEvent)** 

### getCode

-   **See: [Textarea](#textarea) for live example.**

Helper method for parsing KeyboardEvent.

**Parameters**

-   `e` **[KeyboardEvent](https://developer.mozilla.org/docs/Web/API/KeyboardEvent)** 

Returns **KeyCode** 

## Query

Encapsulate matching condition between a Strategy and current editor's value.

**Parameters**

-   `strategy` **[Strategy](#strategy)** 
-   `term` **[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)** 
-   `match` **MatchData** 

### execute

Invoke search strategy and callback the given function.

**Parameters**

-   `callback` **function ([Array](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array)&lt;[SearchResult](#searchresult)>): void** 

### build

Build a Query object by the given string if this matches to the string.

**Parameters**

-   `strategy` **[Strategy](#strategy)** 
-   `text` **[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)** Head to input cursor.

Returns **[Query](#query)?** 

## SearchResult

Encapsulate an result of each search results.

**Parameters**

-   `data` **[Object](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object)** 
-   `term` **[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)** 
-   `strategy` **[Strategy](#strategy)** 

## StrategyProperties

Properties for a strategy.

Type: {match: ([RegExp](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/RegExp) | function ([string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)): (MatchData | null)), search: [Function](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/function), replace: function (any): ([Array](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array)&lt;[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)> | [string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String) | null), cache: [boolean](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Boolean)?, context: [Function](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/function)?, template: function (any): [string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)?, index: [number](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number)?, id: [string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)?}

**Properties**

-   `match` **([RegExp](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/RegExp) | function ([string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)): (MatchData | null))** 
-   `search` **[Function](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/function)** 
-   `replace` **function (any): ([Array](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array)&lt;[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)> | [string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String) | null)** 
-   `cache` **[boolean](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Boolean)?** 
-   `context` **[Function](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/function)?** 
-   `template` **function (any): [string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)?** 
-   `index` **[number](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number)?** 
-   `id` **[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)?** 

## Strategy

Encapsulate a single strategy.

**Parameters**

-   `props` **[StrategyProperties](#strategyproperties)** 

### destroy

Returns **this** 

### replace

**Parameters**

-   `data` **[object](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object)** An element of array callbacked by search function.

## Textarea

**Extends Editor**

Encapsulate the target textarea element.

**Parameters**

-   `el` **[HTMLTextAreaElement](https://developer.mozilla.org/docs/Web/API/HTMLTextAreaElement)** 

### destroy

Returns **this** 

### applySearchResult

Implementation for [Editor#applySearchResult](#editorapplysearchresult)

**Parameters**

-   `searchResult` **[SearchResult](#searchresult)** 

### getCursorOffset

Implementation for [Editor#getCursorOffset](#editorgetcursoroffset)

### getBeforeCursor

Implementation for [Editor#getBeforeCursor](#editorgetbeforecursor)

## TextcompleteOptions

Type: {dropdown: [DropdownOptions](#dropdownoptions)?}

**Properties**

-   `dropdown` **[DropdownOptions](#dropdownoptions)?** 

## Textcomplete

**Extends EventEmitter**

The core of textcomplete. It acts as a mediator.

**Parameters**

-   `editor` **[Editor](#editor)** 
-   `options` **[TextcompleteOptions](#textcompleteoptions)**  (optional, default `{}`)

### destroy

**Parameters**

-   `destroyEditor` **[boolean](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Boolean)**  (optional, default `true`)

Returns **this** 

### hide

Returns **this** 

### register

**Parameters**

-   `strategyPropsArray` **[Array](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array)&lt;[StrategyProperties](#strategyproperties)>** 

**Examples**

```javascript
textcomplete.register([{
  match: /(^|\s)(\w+)$/,
  search: function (term, callback) {
    $.ajax({ ... })
      .done(callback)
      .fail([]);
  },
  replace: function (value) {
    return '$1' + value + ' ';
  }
}]);
```

Returns **this** 

### trigger

Start autocompleting.

**Parameters**

-   `text` **[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)** Head to input cursor.

Returns **this** 
