# Group Tag
Tags are small labels users can apply to various resources and are primarily used to help focus searches.

## Tag [/tag/{name}]
A single Tag object.

Each Tag has the following properties:

- **id**: the id of the tag
- **user**: username of the person who created the tag (**todo:** inconsistent? Seen created_by used on other resources)
- **name**: the name of the tag
- **description**: a description of what the tag means

+ Parameters
    + name (required, string, `Featured`) ... String `name` of the Tag.
    
+ Model (application/json)

    JSON representation of Tag Resource.

    + Body

            {
                "user": null,
                "description": "A description of Ubuntu",
                "id": 5,
                "name": "Ubuntu"
            }

### Retrieve a Tag [GET]
+ Response 200 (application/json)

    [Tag][]          

## Tags Collection [/tag]
Collection of all Tags.

+ Model (application/json)

    JSON representation of Tags Collection Resource.

    + Body

            [
                {
                    "user": null,
                    "description": "A description of SpliceGrapher",
                    "id": 1,
                    "name": "SpliceGrapher"
                },
                {
                    "user": null,
                    "description": "A description of xGDBvm",
                    "id": 2,
                    "name": "xGDBvm"
                },
                {
                    "user": null,
                    "description": "A description of R",
                    "id": 3,
                    "name": "R"
                },
                {
                    "user": null,
                    "description": "Featured applications receive priority ordering over non-featured applications",
                    "id": 4,
                    "name": "Featured"
                },
                {
                    "user": null,
                    "description": "A description of Ubuntu",
                    "id": 5,
                    "name": "Ubuntu"
                }
            ]

### List all Tags [GET]
+ Response 200 (application/json)

    [Tags Collection][]

### Create a Tag [POST]
Create a Tag.  You must specify the following properties:

- **name**: a name for the tag
- **description**: a description of the tag

+ Request (application/json)

        {
            "name": "Tag name",
            "description": "A description of the tag."
        }

+ Response 201 (application/json)

    [Tag][]
