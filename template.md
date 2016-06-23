---
layout: page
---

## Template API

### Object Template description <a id="object"></a>

| Attribute         | Type              | Description                                                   |
|-------------------|-------------------|---------------------------------------------------------------|
| \_id.$id          | ObjectId          | Object ID from the MongoDB                                    |
| site              | num               | ID of the website                                             |
| name              | alpha             | Name of the template                                          |
| labelPriceSelect  | alpha             | Label to choose a price on the website                        |
| fields            | array Field       | Predefined fields that will need to be filled in a product    |
| products          | array Product     | Array of IDs of all products using this template              |
| status            | num               | Status of the page                                            |
| logStatus         | array logStatus   | Audit log of the page                                         |

#### Sub-object Version description <a id="Field"></a>

| Attribute     | Type              | Description                                                           |
|---------------|-------------------|-----------------------------------------------------------------------|
| \_id.$id      | ObjectId          | ID of the field                                                       |
| name          | alpha             | Name of the field that will be displayed on the website               |
| position      | num               | Position of the field compared to the other fields, for the website   | 
| type          | 1\|2\|3           | 1 for text \| 2 for a price \| 3 for a picture                        | 


### List of template <a id="list"></a>

Default URL to request : /bo-management/templates/list/  
Full URL with all parameters : /bo-management/templates/list/{start}/{limit}  
Type of request : GET

#### Parameters 

| Parameter | Position | Default | Type | Description                   |
|-----------|----------|---------|------|-------------------------------|
| {start}   | 1        | 0       | num  | Pagination, first element     |
| {limit}   | 2        | 50      | num  | Pagination, number of element |

#### Return values

Array of Template

#### Example 1 /bo-management/templates/list/0/50

Will retrieve the first 50 templates of the website

#### Example 2 : /bo-management/templates/list/2/10

Will retrieve the third set of 20 templates of the website



### Get a template <a id="get"></a>

Default URL to request : /bo-management/template/{id}     
Type of request : GET

#### Parameters 

| Parameter | Position | Default | Type     | Description |
|-----------|----------|---------|----------|-------------|
| {id}      | 1        | **NA**  | ObjectId | MongoID of the object to load |

#### Return values

The template matching the request




### Update a template <a id="update"></a>

Default URL to request : /bo-management/templates/{name}     
Type of request : POST

#### Parameters 

| Parameter | Position | Default | Type     | Description |
|-----------|----------|---------|----------|-------------|
| {id}      | 1        | **NA**  | ObjectId | MongoID of the object to update |

#### POST parameters


| Parameter         | Type              | Description                                                   |
|-------------------|-------------------|---------------------------------------------------------------|
| name              | alpha             | Name of the template                                          |
| labelPriceSelect  | alpha             | Label to choose a price on the website                        |
| fields            | array Field       | Updated fields with their **IDs** (!!)                        |

#### Return values

JSON object with a single element "OK" with the value "1"




### Delete a page <a id="delete"></a>

Default URL to request : /bo-management/templates/{name}  
Type of request : DELETE

#### Parameters 

| Parameter | Position | Default | Type   | Description |
|-----------|----------|---------|----------|-------------|
| {id}      | 1        | **NA**  | ObjectId | MongoID of the object to update |

#### Return values

JSON object with a single element "OK" with the value "1"
