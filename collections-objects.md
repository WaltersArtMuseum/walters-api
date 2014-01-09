Walters Art Museum Collections API (Beta)
===========

## Get Objects by Collection

A collection is a group of [museum objects](https://github.com/WaltersArtMuseum/walters-api/blob/master/objects.md), i.e. pieces of art, artifacts, or similar items within the Walters Art Museum. Collections at the Walters are grouped by primarily by culture and sometimes by date. For example, the Asian Art collection contains items such as paintings, sculptures and ceramics that were made in or around the Asian continent. Collections are one of the [5 objects you can get with the Walters API](https://github.com/WaltersArtMuseum/walters-api#overview). 

This is one of 2 requests you can use to get museum collections data:
- [GET v1/collections](https://github.com/WaltersArtMuseum/walters-api/blob/master/collections-get.md) Get museum objects via a number of parameters.
- [GET v1/objects/{id}/images](https://github.com/WaltersArtMuseum/walters-api/blob/master/collections-objects.md) Get museum objects within a museum collection.

## Request

The `GET v1/collections/{id}/objects` request will get museum objects associated with a museum collection. The request accepts a number of parameters, listed below.


## Parameters

Name | Type | Description
-----|------|--------------
`id`|`integer` | Define this parameter in the request URI. Enter the ID of a collection to return all the artworks, artifacts or items in that collection. For example, `http://api.thewalters.org/v1/collections/3/objects` will return the museum objects associated with collection number 3, the manuscripts collection.
`orderBy`|`string` | Define this parameter in the request URI. Enter the name of another parameter that you wish to sort results by. For example, `http://api.thewalters.org/v1/collections/3/objects?orderBy=ObjectID` will sort results by CollectionName.
`Page`|`integer` | Define this parameter in the request URI. Results are returned in paged sets. By default, the page parameter is set to 1 so that the results will show the first page of results. Change this number to return other pages. For example, `http://api.thewalters.org/v1/collections/2/objects?page=3` for page 3. 
`pageSize`|`integer` | Define this parameter in the request URI. By default page size is 25 results. Change this number to alter the number of results per page. For example `http://api.thewalters.org/v1/collections/2/objects?pageSize=100` would produce a page with 100 results.