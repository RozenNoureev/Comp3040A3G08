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
