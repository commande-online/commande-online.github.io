---
layout: page
---

## Promotion API

*A promotion can be assimilated to a discount*

### Object Promotion description <a id="object"></a>

| Attribute         | Type              | Description |
|-------------------|-------------------|-------------|
| _id.$id           | ObjectId          | Object ID from the MongoDB |
| site              | num               | ID of the website |
| infos             | array Info        | Array with all the info about the promotion |
| validUntilDate    | timestamp         | Valid until the specified date |
| sendDate          | timestamp         | Promotion was sent on that day |
| oldPriceAmount    | num               | Old price of the product or bundle or what ever |
| priceAmount       | num|null          | New fixed price |
| pricePercentage   | num|null          | Discount in percentage |
| priceFreeText     | alpha|null        | New price |
| product           | Product|null      | If the promotion is linked to a product |
| picture           | alpha|null        | URL of the picture, if provided |
| listUsers         | array User        | List of users to whom the promotion has been or will be sent |
| status            | num               | Status of the promotion |
| logStatus         | array logStatus   | Audit log of the promotion | 

#### Sub-object Info description <a id="info"></a>
 
| Attribute         | Type              | Description |
|-------------------|-------------------|-------------|
| lang              | alpha             | language for the promotion description |
| shortDescription  | alpha             | Short description or title |
| longDescription   | alpha             | Long description | 


### List of promotions <a id="list"></a>

Default URL to request : /bo-management/promotions/list/  
Full URL with all parameters : /bo-management/promotions/list/{start}/{limit}   
Type of request : GET

#### Parameters 

| Parameter | Position | Default | Type | Description |
|-----------|----------|---------|------|-------------|
| {start}   | 1        | 0       | num  | Pagination, first element |
| {limit}   | 2        | 50      | num  | Pagination, number of element |

#### Return values

Array of Promotion

#### Example 1 /bo-management/promotions/list/0/50

Will retrieve the first 50 promotion of the website

#### Example 2 : /bo-management/promotions/list/2/10

Will retrieve the third set of 20 promotions of the website


### Get a Promotion <a id="get"></a>

Default URL to request : /bo-management/promotions/{id}     
Type of request : GET

#### Parameters 

| Parameter | Position | Default | Type     | Description |
|-----------|----------|---------|----------|-------------|
| {id}      | 1        | **NA**  | ObjectId | ID of the promotion to load |

#### Return values

The promotion with the matching ID




### Send a promotion <a id="send"></a>

Default URL to request : /bo-management/promotions/{id}/send     
Type of request : POST

#### Parameters 

| Parameter | Position | Default | Type   | Description |
|-----------|----------|---------|--------|-------------|
| {id}      | 1        | **NA**  | ObjectId | ID of the promotion to update |


#### Return values

JSON object with a single element "OK" with the value "1"



### Update a promotion <a id="update"></a>

Default URL to request : /bo-management/promotions/{id}     
Type of request : POST

#### Parameters 

| Parameter | Position | Default | Type   | Description |
|-----------|----------|---------|--------|-------------|
| {id}      | 1        | **NA**  | ObjectId | ID of the promotion to update |

#### POST parameters

| Parameter         | Type          | Description |
|-------------------|---------------|-------------|
| {infos}           | array Info    | Info about the promotion |
| {validUntilDate}  | timestamp     | timestamp of the end of validity |
| {product}         | ObjectId|null | ID of the product |
| {oldPriceAmount}  | num           | Old price |
| {priceAmount}     | num           | New fixed price |
| {pricePercentage} | num           | Percentage of discount |
| {priceFreeText}   | alpha         | New price |
| {picture}         | alpha         | *Not sure if it is working or not* |

#### Return values

JSON object with a single element "OK" with the value "1"




### Delete a promotion <a id="delete"></a>

Default URL to request : /bo-management/promotions/{id}     
Type of request : DELETE

#### Parameters 

| Parameter | Position | Default | Type   | Description |
|-----------|----------|---------|--------|-------------|
| {id}      | 1        | **NA**  | ObjectId | ID of the promotion to update |

#### Return values

JSON object with a single element "OK" with the value "1"
