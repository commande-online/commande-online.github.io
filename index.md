---
layout: default
---

## Commande-Online.fr is providing an API for myCOL

![Commande-Online.fr SAS](http://commande-online.fr/img/corporate/logoCOL.png)

### API v2.6

| URL                                                           | Type   | Description |
|---------------------------------------------------------------|--------|-------------|
| [/bo-management/pages/list/](/page.html#list)                 | GET    | List of all pages |
| [/bo-management/pages/list/update](/page.html#list-update)    | GET    | List of pages that have been updated |
| [/bo-management/pages/{name}](/page.html#get)                 | GET    | Load a page |
| [/bo-management/pages/{name}](/page.html#update)              | POST   | Update a page |
| [/bo-management/pages/{name}](/page.html#delete)              | DELETE | Delete a page |
| [/bo-management/promotions/list/](/promotion.html#list)       | GET    | List of all promotions |
| [/bo-management/promotions/{name}](/promotion.html#get)       | GET    | Load a promotion |
| [/bo-management/promotions/{name}](/promotion.html#update)    | POST   | Update a promotion |
| [/bo-management/promotions/{name}](/promotion.html#delte)     | DELETE | Delete a promotion |
| [/bo-management/promotions/{name}/send](/promotion.html#send) | POST   | Send a promotion to the users |
| /bo-management/templates/list/           | GET    | List of all templates |
| /bo-management/templates/{name}          | GET    | Load a template |
| /bo-management/templates/{name}          | POST   | Update a template |
| /bo-management/templates/{name}          | DELETE | Delete a template |
| /bo-management/categories/list/          | GET    | List of all categories |
| /bo-management/categories/list/update    | GET    | List of categories that have been updated |
| /bo-management/categories/{name}         | GET    | Load a category |
| /bo-management/categories/{name}         | POST   | Update a category |
| /bo-management/categories/{name}         | DELETE | Delete a category |
| /bo-management/products/list/            | GET    | List of all products |
| /bo-management/products/list/update      | GET    | List of products that have been updated |
| /bo-management/products/{name}           | GET    | Load a product |
| /bo-management/products/{name}           | POST   | Update a product |
| /bo-management/products/{name}           | DELETE | Delete a product |
| /bo-management/medias/list/              | GET    | List of all medias |
| /bo-management/medias/{name}             | GET    | Load a media |
| /bo-management/medias/{name}             | POST   | Update a media |
| /bo-management/medias/{name}             | DELETE | Delete a media |
| /bo-management/medias                    | POST   | Upload a media |
| /bo-management/carts/list/               | GET    | List of all carts |
| /bo-management/carts/list/update         | GET    | List of carts that have been updated |
| /bo-management/carts/{name}              | GET    | Load a cart |
| /bo-management/carts/{name}              | POST   | Update a cart |
| /bo-management/carts/{name}              | DELETE | Delete a cart |
| /bo-management/users/list/               | GET    | List of all users |
| /bo-management/users/list/update         | GET    | List of users that have been updated |
| /bo-management/users/search/{query}      | GET    | Search for a user |
| /bo-management/users/{name}              | GET    | Load a user |
| /bo-management/users/{name}              | POST   | Update a user |
| /bo-management/users/{name}              | DELETE | Delete a user |
| /bo-management/languages                 | GET    | List of available languages |

### Error object

In case a request doesn't work properly, an error is thrown on the server and sent back to the caller through a JSON object