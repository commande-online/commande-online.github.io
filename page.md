---
layout: default
---

## Page API

### List of pages <a id="list"></a>

Default URL to request : /bo-management/pages/list/  
Type of request : GET

#### Parameters 

| Parameter | Position | Default | Type | Description |
|-----------|----------|---------|------|-------------|
| {start}   | 1        | 0       | num  | Pagination, start of the page |
| {limit}   | 2        | 50       | num  | Pagination, start of the page |

#### Return values

Array of pages

#### Example 1 /bo-management/pages/list/0/50

Will retrieve the first 50 pages of the website


#### Example 2 : /bo-management/pages/list/2/10

Will retrieve the third set of 20 pages of the website