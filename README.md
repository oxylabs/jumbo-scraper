# Jumbo Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs' [Jumbo Scraper](https://oxylabs.io/products/scraper-api/ecommerce/jumbo?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Jumbo website effortlessly. This brief guide showcases how Jumbo Scraper works, along with code examples to help you better understand how to use it hassle-free.

### How it works

You can get Jumbo results by providing your own URLs to our service. We can return the HTML for any page you like.

#### Python code example

The example below illustrates how you can get HTML of Jumbo page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal_ecommerce',
    'url': 'https://www.jumbo.com/producten/zuivel,-eieren,-boter/houdbare-melk-en-zuivel/'
}

# Get response.
response = requests.request(
    'POST',
    'https://realtime.oxylabs.io/v1/queries',
    auth=('user', 'pass1'),
    json=payload,
)

# Instead of response with job status and results url, this will return the
# JSON response with the result.
pprint(response.json())
```
Find code examples for other programming languages [**here**](https://github.com/oxylabs/jumbo-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html>\n<html  lang=\"nl-nl\">\n<head><meta charset=\"utf-8\">\n<meta name=\"viewport\" content=\"wid ... </html>",
      "created_at": "2024-02-20 12:45:43",
      "updated_at": "2024-02-20 12:45:47",
      "page": 1,
      "url": "https://www.jumbo.com/producten/zuivel,-eieren,-boter/houdbare-melk-en-zuivel/",
      "job_id": "7165687967263011841",
      "status_code": 200
    }
  ]
}
```
With our Jumbo Scraper, you can smoothly extract public data from any Jumbo-themed blogs or forums. Gather necessary information like comments, user engagement, or trending topics to analyze the online community sentiment and outpace your competitors. If you need any assistance, feel free to reach out to our dedicated support team via live chat or email us at hello@oxylabs.io.