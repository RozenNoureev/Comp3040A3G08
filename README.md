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




## Resource Description

The Manitoba Parks API returns data in JSON format. The following resources are available:

### Park

A Park object represents a park in Manitoba. The following attributes are available:

- `id` - The unique ID of the park, represented by a decimal number.
- `name` - The name of the park.
- `areaLocated` - The location of the park, either described by city/RM or using regions as described by [Canada's travel website](https://www.comeexplorecanada.com/manitoba).
- `waterBody` - Describes the type of body of water that can be found at the park, if there is one.

## Sample Request with Sample Response

### Request 

[www.parksmb.com/parks/1]()

### Response

```json
{
  "id": 1,
  "name": "Birds Hill Park",
  "areaLocated": "RM of Springfield",
  "waterBody": ["Man-Made Beach"]
}