# Manitoba Parks API

## API Description

The Park Finder API for Manitoba is designed to provide information about parks situated in Manitoba, Canada, allowing users to access details such as park location and other features. This API enables users to search for parks using different criteria, including park name and location. Additionally, the API is publicly accessible and can be integrated into any application requiring park-related data in Manitoba.

## List of Endpoints

The Manitoba Parks API includes the following endpoints:

### GET /parks

It gives a list of all the parks in Manitoba.

Parameters:

None

### GET /parks/{id}

Each park has a unique ID, it will return the name and info of the park the park whose ID is provided as a parameter.

Parameters:

- `id` - The ID of the park to retrieve.

### GET /parks/info

This endpoint allows users to get a list of parks and their information filtered by specified parameters.

Parameters:

- `name` - Name of the park.
- `areaLocated` - Area where the park is located.
- `hasWaterBody` - Accepts a `true` or `false` value and returns a list of parks that either have bodies of water or don't.

## Type of parameters

The Park Finder API returns data in JSON format. The following resources are available:

| Parameter  | Type    | 
| :-------:  | :--:    |
| id         |  int    | 
| name       | String  | 
| areaLocated| String  | 
| hasWaterBody| Boolean |
| waterBody| List |

## Resource Description

The Manitoba Parks API returns data in JSON format. The following resources are available:

### Park

A Park object represents a park in Manitoba. The following fields are available:

- `id` - The unique ID of the park, represented by a decimal number.
- `name` - The name of the park.
- `areaLocated` - The location of the park, either described by city/RM or using regions as described by [Canada's travel website](https://www.comeexplorecanada.com/manitoba).
- `waterBody` - Describes the type of body of water that can be found at the park, if there is one.

```json
{
 "id": 'int',
 "name": 'String',
 "areaLocated": 'String',
 "waterBody": 'List' 
}
```

## Sample Request with Sample Response

### Request : 1

[www.parksmb.com/parks/1]()

### Response
```json
{
 {
  "id": 1,
  "name": "Birds Hill Park",
  "areaLocated": "RM of Springfield",
  "waterBody": ["Man-Made Beach"]
 }
 "status":"OK"
} 
```
### Request : 2

[www.parksmb.com/parks]()

### Response
``` json
{
 {
   "Birds Hill Park",
   "Chitak Lake park reserve",
   "Duck Mountain Provincial Park",
   "Saint Vital Park",
   "Birds hill Provincial Park",
   "Turtle Mountain Provencial Park"
 }
 "status":"OK"
}
```

### Request : 3

[www.parksmb.com/parks/info?hasWaterBody=true]()

### Response
```json
[
 {
  "id": 1,
  "name": "Birds Hill Park",
  "areaLocated": "RM of Springfield",
  "waterBody": ["Man-Made Beach"]
 },
 {
 "id": 4,
  "name": "Saint Vital Park",
  "areaLocated": "Winnipeg",
  "waterBody": ["Pond"]
 }
 "status":"OK"
] 
```

### Request : 4

[www.parksmb.com/parks/info?areaLocated=parkland]()

### Response
```json
[
 {
  "id": 3,
  "name": "Duck Mountain Provincial Park",
  "areaLocated": "Parkland",
  "waterBody": ["Lake"]
 },
 {
 "id": 7,
  "name": "Riding Mountain National Park",
  "areaLocated": "Parkland",
  "waterBody": ["Lake"]
 }
 "status":"OK"
] 
```
