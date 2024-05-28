# API RESTful. 

## Description.
RESTful API created with the aim of practicing RESTful standards.

## Installation Instruction.

### Requirements.
* Java 22.
* Springboot 3.3.0.

## Instruction for use
### The REST API to the example app is described below.

## Get list.
### Request.
    `GET /api/products`
        http://127.0.0.1:8080/api/products

### Response.
    [
        {
            "idProduct": "13818cbb-6685-4356-bf4d-0e8d9009c8f5",
            "name": "Monito Dell Inspiron",
            "value": 1366.00,
            "links": [
                {
                    "rel": "self",
                    "href": "http://127.0.0.1:8080/api/products/13818cbb-6685-4356-bf4d-0e8d9009c8f5"
                }
            ]
        },
    ]

## Get a specific product.
### Request.
`GET /api/products/id`
    http://127.0.0.1:8080/api/products/ad009468-dbc4-4944-a3cc-756638dee3ad

### Response
    {
        "idProduct": "ad009468-dbc4-4944-a3cc-756638dee3ad",
        "name": "Notebook Sansung Galaxy Book2",
        "value": 2400.00,
        "_links": {
            "Product list": {
                "href": "http://127.0.0.1:8080/api/products"
            }
        }
    }

## Creating a new product.
### Request.
    `POST /api/products`
        http://localhost:8080/api/products
        {
            "name": "test",
            "value": 0.0
        }

### Response.
    {
	    "idProduct": "5bdd1e86-1bdc-41a2-bb2d-b49e3aff3d93",
	    "name": "teste",
	    "value": 0.0
    }

## Change a specific product.
### Request.
`PUT /api/products/id`
http://127.0.0.1:8080/api/products/ad009468-dbc4-4944-a3cc-756638dee3ad

### Response.
    {
        "idProduct": "ad009468-dbc4-4944-a3cc-756638dee3ad",
        "name": "Notebook Sansung Galaxy Book2",
        "value": 2400.00
    }

## Delete a specific product.
### Request.
`DELETE /api/products/id`
http://127.0.0.1:8080/api/products/ad009468-dbc4-4944-a3cc-756638dee3ad

### Response.
    Product was deleted with success!

## License.
### Educational use.