## Here is the json request file by drabhishek 

```
{
  "url": "https://gaffa.dev/blog",
  "proxy_location": null,
  "async": false,
  "max_cache_age": 0,
  "max_media_bandwidth": null,
  "time_limit": null,
  "settings": {
    "record_request": false,
    "actions": [
      {
        "type": "wait",
        "selector": "article",
        "timeout": 5000
      },
      {
        "type": "parse_json",
        "model": "gpt-4o-mini",
        "output_type": "inline",
        "selector": "article",
        "data_schema": {
          "name": "BlogPost",
          "description": "Extract title, author, and summary from a Gaffa blog article",
          "fields": [
            {
              "type": "string",
              "name": "title",
              "description": "Title of the blog post"
            },
            {
              "type": "string",
              "name": "author",
              "description": "Author of the article"
            },
            {
              "type": "string",
              "name": "summary",
              "description": "Short summary explaining the blog post"
            }
          ]
        }
      }
    ]
  }
}
```
