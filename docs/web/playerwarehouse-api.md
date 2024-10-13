# Player-Warehouse (Work in progress)

The playerdata Management endpoint provides the latest playerpprofiles for the Infinityheroes Minecraft server. This endpoint requires an API key and can´t be accessed publicly. The response is a JSON array containing playerdata items such as the name, UUID, language, gamemode data such as coins etc.


## Get player profile - Endpoint

`GET https://api.ifheroes.de/v1/warehouse`

### Description

Get the basic player profile with every information.

### Example Request

```sh
curl -X GET "https://api.ifheroes.de/v1/warehouse/?uuid={UUID}"
```

### Example Response

The response is a JSON array of news objects. Below is an example of the returned data:

```json
{
  "basicData": {
    "version": "v1",
    "uuid": "cc0cf164-e630-498b-8f11-4f6a52467a77",
    "name": "I_Dev"
  },
  "advancedData": {
    "language": "DE"
  },
  "pluginData": {
    "values": "{\"coretest\":{\"coins\":100}}"
  }
}
```

### Response Parameters

**basicData**
- `version`: A string representing the version who last modified this data set.
- `uuid`: A string representing the UUID of the player. This UUID is provided by Mojang. Its also the primary identifier for the playerwarehouse.
- `name`: A string representing the name of the player.

**advancedData**
- `language`: A string representing the current langauage from the player on the server.

**pluginData**
- `values`: A variable string that is handled by the infinityheroes core plugin. The layout can be different in every playerprofile.

### Usage

This endpoint is useful for retrieving data from players regarding the Infinityheroes server. Developers can use this information to display profile information in their applications or websites.

### Notes

- Ensure your application can handle the structure of the JSON response.
- The example URLs provided in the `path` parameter are placeholders. In a real scenario, these URLs will point to actual resources.

For further assistance or inquiries, please contact our support team via our [Discord server](https://ifheroes.de/discord).


This description provides a detailed overview of the `https://api.ifheroes.de/v1/warehouse` endpoint, including its usage, response format, and example requests and responses.
