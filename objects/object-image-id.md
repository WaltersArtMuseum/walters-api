Walters Art Museum Collections API 
===============================================================================

## Get Object Images by ID

The `GET v1/objects/{id}/images` request will get the images of an artwork. Use the id parameter to specify which artwork's images to get.


## A Note About Images
There are some [important things to understand about the images](/images.md) available through this API.


## Parameters

Name | Type | Description
-----|------|--------------
`apikey` | `string` | This parameter is required to be defined in every API request. Please [obtain an API key](http://api.thewalters.org/) and include it in your API requests as follows: `http://api.thewalters.org/v1/objects?apikey={your_api_key}`. Be sure to replace `{your_api_key}` with your actual key. 
`id` | `integer` | Define this parameter in the request URI. For example, `http://api.thewalters.org/v1/objects/37626/images` will get images the object record for "The Ideal City."


## Response

Here is an example of a typical response.

```
{
    "Items": [
        {
            "ObjectID": 37626,
            "MediaXrefID": 16742,
            "ImageURL": "http://static.thewalters.org/images/PS1_37.677_FntAftTrt_DD_T09.jpg",
            "Filename": "PS1_37.677_FntAftTrt_DD_T09.jpg",
            "MediaType": "Image",
            "MediaView": "Front",
            "Rank": 1,
            "IsPrimary": true
        },
        {
            "ObjectID": 37626,
            "MediaXrefID": 42090,
            "ImageURL": "http://static.thewalters.org/images/PS1_37.677_DetB2_DD_T12.jpg",
            "Filename": "PS1_37.677_DetB2_DD_T12.jpg",
            "MediaType": "Image",
            "MediaView": "Detail",
            "Rank": 59,
            "IsPrimary": false
        },
        {
            "ObjectID": 37626,
            "MediaXrefID": 42091,
            "ImageURL": "http://static.thewalters.org/images/PS1_37.677_DetB3__DD_T12.jpg",
            "Filename": "PS1_37.677_DetB3__DD_T12.jpg",
            "MediaType": "Image",
            "MediaView": "Detail",
            "Rank": 60,
            "IsPrimary": false
        },
        {
            "ObjectID": 37626,
            "MediaXrefID": 42092,
            "ImageURL": "http://static.thewalters.org/images/PS1_37.677_DetB4_DD_T12.jpg",
            "Filename": "PS1_37.677_DetB4_DD_T12.jpg",
            "MediaType": "Image",
            "MediaView": "Detail",
            "Rank": 61,
            "IsPrimary": false
        },
        {
            "ObjectID": 37626,
            "MediaXrefID": 42093,
            "ImageURL": "http://static.thewalters.org/images/PS1_37.677_DetB5_DD_T12.jpg",
            "Filename": "PS1_37.677_DetB5_DD_T12.jpg",
            "MediaType": "Image",
            "MediaView": "Detail",
            "Rank": 62,
            "IsPrimary": false
        }
    ],
    "PageSize": 0,
    "Page": 0,
    "NextPage": false,
    "PrevPage": false,
    "ReturnStatus": true,
    "ReturnCode": 200,
    "ReturnMessage": []
}
```

`Get Object Images by ID` is one of 3 requests you can use to get museum objects:
- [GET v1/objects](objects-get.md) Get museum objects via a number of parameters.
- [GET v1/objects/{id}](objects-id.md) Get extended details about a museum object by referencing an object ID.
- [GET v1/objects/{id}/images](object-image-id.md) Get images of a museum object by referencing an object ID.