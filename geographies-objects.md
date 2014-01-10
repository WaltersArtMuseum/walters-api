Walters Art Museum Collections API (Beta)
=========================================

## Get Objects by Geography

Geographies are locations on Earth where the various museum [objects](https://github.com/WaltersArtMuseum/walters-api/blob/master/objects.md) have been created. Each geography  will have a geo type, display name, latitude and longitude (if available), and geography id.

This is one of 3 requests you can use to get geographical information about the Walters Collection:
- [GET v1/museum/geographies](https://github.com/WaltersArtMuseum/walters-api/blob/master/geographies-get.md) Get object geographies via a number of parameters.
- [GET v1/museum/geographies/{id}/objects](https://github.com/WaltersArtMuseum/walters-api/blob/master/geographies-objects.md) Get museum objects associated with a given geography.
- [GET /v1/geographies/geotype/{term:string}/objects](https://github.com/WaltersArtMuseum/walters-api/blob/master/geographies-objects-geotype.md)

## Request

The `GET v1/museum/geographies/{id}/objects` request will get museum objects associated with a specific geographic location. The request accepts a number of parameters, listed below.


## Parameters

Name | Type | Description
-----|------|--------------
`id`|`integer` | Define this parameter in the request URI. Enter the ID of a collection to return all the artworks, artifacts or items in that collection. For example, `http://api.thewalters.org/v1/geographies/3/objects` will return the museum objects associated with geography number 3.
`Page`|`integer` | Define this parameter in the request URI. Results are returned in paged sets. By default, the page parameter is set to 1 so that the results will show the first page of results. Change this number to return other pages. For example, `http://api.thewalters.org/v1/collections/2/objects?page=3` for page 3. 
`pageSize`|`integer` | Define this parameter in the request URI. By default page size is 25 results. Change this number to alter the number of results per page. For example `http://api.thewalters.org/v1/collections/2/objects?pageSize=100` would produce a page with 100 results.