---
layout: default
---

## Commande-Online.fr is providing an API for myCOL

![Commande-Online.fr SAS](http://commande-online.fr/img/corporate/logoCOL.png)

### List of API available

| URL                                      | Type   | Description |
|------------------------------------------|--------|-------------|
| /bo-management/pages/list/               | GET    | List of all pages |
| /bo-management/pages/list/update         | GET    | List of pages that have been updated |
| /bo-management/pages/{name}              | GET    | Load a page |
| /bo-management/pages/{name}              | POST   | Update a page |
| /bo-management/pages/{name}              | DELETE | Delete a page |
| /bo-management/promotions/list/          | GET    | List of all promotions |
| /bo-management/promotions/{name}         | GET    | Load a promotion |
| /bo-management/promotions/{name}         | POST   | Update a promotion |
| /bo-management/promotions/{name}         | DELETE | Delete a promotion |
| /bo-management/promotions/{name}/send    | POST   | Send a promotion to the users |
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
