# longlist 2.0 - A Minimalist JavaScript List Pager

Forked from https://github.com/jekor/longtable and modified for lists.
Demo at http://www.minjs.com/#longtable

## Features

* paging
* minimal code
* controls rendered inside the list dynamically (in a `<li>`)
* no library dependencies

## How to Use

```JavaScript
var yourList = document.getElementById('yourList');
longlist(yourList);
```

## Options

`longlist()` takes an options argument as an optional second argument. The options are:

* `perPage`: how many rows to display per page (default: 10)
* `startPage`: which page to display initially (default: 1)
* `maxPageLinks`: how many page navigation links to display (default: 9)

Longlist will display fewer than `maxPageLinks` page navigation links if there are fewer pages. For best results, use an odd numbered `maxPageLinks` greater than equal to 3.

```JavaScript
longlist(yourList, {perPage: 20, maxPageLinks: 7});
```

## Functions

* `gotoPage(n)` - jump to the given page number

```JavaScript
yourList.gotoPage(3);
```

## Events

* `longlist.pageChange` - triggered when the page changes (passes the page number)

## Notes

* Items to be paged must be children of `<ul>` or `<ol>`.
* Does not support adding/removing list items.

## Unsupported Browsers

* Internet Explorer <= 8
