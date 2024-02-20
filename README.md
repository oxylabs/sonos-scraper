# Sonos Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs' [Sonos Scraper](https://oxylabs.io/products/scraper-api/ecommerce/sonos?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Sonos website effortlessly. This brief guide showcases how Sonos Scraper works, along with code examples to help you better understand how to use it hassle-free.

### How it works

You can get Sonos results by providing your own URLs to our service. We can return the HTML for any page you like.

#### Python code example

The example below illustrates how you can get HTML of Sonos page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal_ecommerce',
    'url': 'https://www.sonos.com/en-ca/shop/speaker-sets'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/sonos-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html><html lang=\"en-ca\"><head><meta charSet=\"utf-8\"/><title>Wireless Speaker Sets | Sonos< ... </html>",
      "created_at": "2024-02-20 12:57:51",
      "updated_at": "2024-02-20 12:57:53",
      "page": 1,
      "url": "https://www.sonos.com/en-ca/shop/speaker-sets",
      "job_id": "7165691020670152705",
      "status_code": 200
    }
  ]
}
```
With our Sonos Scraper, you gain seamless access to public data from every Sonos web page. Effortlessly gather essential information about product specifications, current offers or discounts, dealer information and customer rankings to understand the market better and be a step ahead of your business rivals. For any queries, interact with our support staff through live chat or email us at hello@oxylabs.io.