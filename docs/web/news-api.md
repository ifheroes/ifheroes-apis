## News Endpoint

### Endpoint

`GET https://api.ifheroes.de/v1/news`

### Description

The News endpoint provides the latest news updates related to the Infinityheroes Minecraft server. This endpoint does not require an API key and can be accessed publicly. The response is a JSON array containing news items with details such as the news number, the path to the JSON file, the date of the news, and a unique file ID.

### Example Request

```sh
curl -X GET "https://api.ifheroes.de/v1/news"
```

### Example Response

The response is a JSON array of news objects. Below is an example of the returned data:

```json
[
    {
        "number": "1",
        "path": "https://localhost:8080/exports/05-22-2024_21-11-38.json",
        "date": "22-05-2024",
        "file_id": "22052024091138"
    },
    {
        "number": "2",
        "path": "https://localhost:8080/exports/05-22-2024_21-11-33.json",
        "date": "22-05-2024",
        "file_id": "22052024091133"
    },
    {
        "number": "3",
        "path": "https://localhost:8080/exports/05-22-2024_21-11-29.json",
        "date": "22-05-2024",
        "file_id": "22052024091129"
    }
]
```

### Response Parameters

- `number`: A string representing the unique number assigned to the news item.
- `path`: A string URL pointing to the JSON file containing detailed information about the news item.
- `date`: A string representing the date when the news was published, formatted as `dd-mm-yyyy`.
- `file_id`: A string representing a unique identifier for the news file.

### Usage

This endpoint is useful for retrieving the latest news updates regarding the Infinityheroes server. Developers can use this information to display news on their applications or websites, keeping the community informed about the latest developments and updates.

### Notes

- Ensure your application can handle the structure of the JSON response.
- The example URLs provided in the `path` parameter are placeholders. In a real scenario, these URLs will point to actual resources.

For further assistance or inquiries, please contact our support team via our [Discord server](https://ifheroes.de/discord).
```

This description provides a detailed overview of the `https://api.ifheroes.de/v1/news` endpoint, including its usage, response format, and example requests and responses.