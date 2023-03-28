# Manitoba Parks API

## API Description

The Park Finder API for Manitoba is a RESTful API designed to provide information about parks in the province of Manitoba, Canada. This API can be used to obtain details about parks such as their location, amenities, trails, and events. It allows users to search for parks based on different criteria, such as park name, location, and amenities. The API is publicly accessible and can be used by any application that requires park-related information in Manitoba.

## List of Endpoints

The Manitoba Parks API includes the following endpoints:

### GET /parks

It gives the name and info of all the parks in Manitoba.

Parameters:

None

### GET /parks/{id}

Each park has a unique ID, it will return the name and info of the park the park whose ID is provided as a parameter.

Parameters:

- `id` - The ID of the park to retrieve.

### GET /parks/info

This endpoint allows users to get information about the parks.

Parameters:

- `name` - Name of the park.
- `areaLocated` - Area where the park is located.
- `hasWaterBody` - Returns `True` or `False` depeneding on whether the Park has any waterbodies(Lake, pond, river, etc) in it or not.

## Type of parameters

The Park Finder API returns data in JSON format. The following resources are available:

| Parameter  | Type    | 
| :-------:  | :--:    |
| id         |  int    | 
| name       | String  | 
| areaLocated| String  | 
| hasWaterBody| Boolean |

## Resource Description

The Manitoba Parks API returns data in JSON format. The following resources are available:

### Park

A Park object represents a park in Manitoba. The following fields are available:

- `id` - The unique ID of the park, represented by a decimal number.
- `name` - The name of the park.
- `areaLocated` - The location of the park, either described by city/RM or using regions as described by [Canada's travel website](https://www.comeexplorecanada.com/manitoba).
- `waterBody` - Describes the type of body of water that can be found at the park, if there is one.

## Sample Request with Sample Response

### Request : 1

[www.parksmb.com/parks/1]()

### Response

```json
{
  "id": 1,
  "name": "Birds Hill Park",
  "areaLocated": "RM of Springfield",
  "waterBody": ["Man-Made Beach"]
}

### Request : 2

[www.parksmb.com/parks]()

### Response

```json
{
  "Chitak Lake park reserv",
  "Birds Hill Park",
  "Duck Mountain Provencial Park",
  "Saint Vital Park",
  "Birds hill Provincial Park",
  "Turtle Mountain Provencial Park"
}
