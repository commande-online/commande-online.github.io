---
layout: page
---

## Page API

### Object Page description <a id="object"></a>

| Attribute     | Type              | Description |
|---------------|-------------------|-------------|
| _id.$id       | ObjectId          | Object ID from the MongoDB |
| site          | num               | ID of the website |
| name          | alpha             | Name of the url used for the page on the website |
| title         | alpha             | Title of the page |
| lang          | alpha             | Two letter language identification |
| versions      | array Version     | Array of all saved versions of the page |
| comment       | bool              | If comments are enabled or not |
| tags          | array alpha       | Array of all current tags |
| comments      | array Comment     | Array of all saved comments |
| links         | array alpha       | Array of all links for all the related pages in the different languages |
| status        | num               | Status of the page |
| logStatus     | array logStatus   | Audit log of the page |
| last_refresh  | timestamp         | Timestamp of the last action on the object | 

#### Sub-object Version description <a id="version"></a>
 
| Attribute     | Type              | Description |
|---------------|-------------------|-------------|
| user          | num               | ID of the user who created this version |
| date          | date ISO format   | Date of creation |
| text          | alpha             | Text of the page in the given version | 

#### Sub-object Comment description <a id="comment"></a>
 
| Attribute     | Type              | Description |
|---------------|-------------------|-------------|
| user          | num               | ID of the user who created this version |
| date          | date ISO format   | Date of creation |
| comment       | alpha             | Text |
| reply         | num               | *Not used at the moment* |
| status        | num               | Status of the comment |


### List of pages <a id="list"></a>

Default URL to request : /bo-management/pages/list/  
Full URL with all parameters : /bo-management/pages/list/{start}/{limit}   
Type of request : GET

#### Parameters 

| Parameter | Position | Default | Type | Description |
|-----------|----------|---------|------|-------------|
| {start}   | 1        | 0       | num  | Pagination, first element |
| {limit}   | 2        | 50      | num  | Pagination, number of element |

#### Return values

Array of Page

#### Example 1 /bo-management/pages/list/0/50

Will retrieve the first 50 pages of the website

#### Example 2 : /bo-management/pages/list/2/10

Will retrieve the third set of 20 pages of the website


### List of pages updated <a id="list-update"></a>

Default URL to request : /bo-management/pages/list/update 
Full URL with all parameters : /bo-management/pages/list/update/{since}   
Type of request : GET

#### Parameters 

| Parameter | Position | Default | Type      | Description |
|-----------|----------|---------|-----------|-------------|
| {since}   | 1        | *TODAY* | timestamp | Pagination, first element |

#### Return values

Array of Page



### Get a page <a id="get"></a>

Default URL to request : /bo-management/pages/{name}     
Type of request : GET

#### Parameters 

| Parameter | Position | Default | Type   | Description |
|-----------|----------|---------|--------|-------------|
| {name}    | 1        | **NA**  | alpha  | Name of the page to load |

#### Return values

The page matching the request




### Update a page <a id="update"></a>

Default URL to request : /bo-management/pages/{name}     
Type of request : POST

#### Parameters 

| Parameter | Position | Default | Type   | Description |
|-----------|----------|---------|--------|-------------|
| {name}    | 1        | **NA**  | alpha  | Name of the page to load |

#### POST parameters


| Parameter | Type   | Description |
|-----------|--------|-------------|
| {title}    | alpha  | Title of the page |
| {comment}    | 0|1  | Flag to know if the comments are activated |
| {tags}    | alpha  | All tags concatenated with ";" |
| {versions}   | array of Versions | Only the last occurrence will be used and saved in the DB  |
| {name}   | alpha | Name of the page |
| {lang}   | alpha | Two letters language of the page |
| {links}   | array of alpha | List of all links for related pages in different language. Warning, the list is overwritten |

#### Return values

JSON object with a single element "OK" with the value "1"




### Delete a page <a id="delete"></a>

Default URL to request : /bo-management/pages/{name}     
Type of request : DELETE

#### Parameters 

| Parameter | Position | Default | Type   | Description |
|-----------|----------|---------|--------|-------------|
| {name}    | 1        | **NA**  | alpha  | Name of the page to load |

#### Return values

JSON object with a single element "OK" with the value "1"
