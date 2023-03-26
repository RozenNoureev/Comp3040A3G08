### GET /parks/info

This endpoint allows users to get information about the parks.

Parameters:

- `name` - The name of the park to search for.
- `areaLocated` - The location of where the park is located.
- `hasLake` - returns true or false whether the park has any lake, pond or river.

## Description of Resources

The Park Finder API returns data in JSON format. The following resources are available:

### Park

A Park object represents a park in Manitoba. The following attributes are available:

- `id` - ID number of the park.
- `name` - Name of the park.
- `areaLocated` - Area where the park is located.
- `hasWaterBody` - Returns `True` or `False` depeneding on whether the Park has any waterbodies(Lake, pond, river, etc) in it or not.
