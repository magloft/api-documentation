# Issues

API for managing issues

{% api-method method="get" host="https://www.magloft.com" path="/api/portal/v1/issues/:app_id" %}

{% api-method-summary %}
List Issues
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **returns** a list of all `issues` that belong to the magazine
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="string" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% endapi-method-path-parameters %}


{% api-method-query-parameters %}

{% api-method-parameter name="source" type="string" %}
Source type of issue
{% endapi-method-parameter %}

{% endapi-method-query-parameters %}



{% endapi-method-request %}

{% api-method-response %}

{% api-method-response-example httpCode=200 %}

```json
{
  "id": 1234,
  "title": "Welcome to MagLoft",
  "info": null,
  "hpub": null,
  "source_file": null,
  "source": "typeloft",
  "unlock_type": "free",
  "categories": null,
  "product_id": "purchase.issue_123456789",
  "product_id_apple": null,
  "product_id_google": null,
  "publication_id": null,
  "coupon_code": null,
  "dirty": false,
  "user_id": null,
  "custom_stylesheet": null,
  "custom_data": null,
  "price_tier": null,
  "cover": null
}
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}

{% api-method method="get" host="https://www.magloft.com" path="/api/portal/v1/issues/:app_id/page/:page" %}

{% api-method-summary %}
Retrieve paginated list of issues
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **returns** a page list of all `issues` that belong to the magazine
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="string" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% api-method-parameter name="page" type="string" required=true %}
The page number to list
{% endapi-method-parameter %}

{% endapi-method-path-parameters %}


{% api-method-query-parameters %}

{% api-method-parameter name="per_page" type="string" %}
Number of items to show per page
{% endapi-method-parameter %}

{% api-method-parameter name="order_by" type="string" %}
Field to sort results by
{% endapi-method-parameter %}

{% api-method-parameter name="order_dir" type="string" %}
Direction (asc, desc) to sort results by
{% endapi-method-parameter %}

{% api-method-parameter name="filter" type="string" %}
Text filter to search results by
{% endapi-method-parameter %}

{% endapi-method-query-parameters %}



{% endapi-method-request %}

{% api-method-response %}

{% api-method-response-example httpCode=200 %}

```json
{
  "total": 1,
  "page": 1,
  "records": [
    {
      "id": 1234,
      "title": "Welcome to MagLoft",
      "info": null,
      "hpub": null,
      "source_file": null,
      "source": "typeloft",
      "unlock_type": "free",
      "categories": null,
      "product_id": "purchase.issue_123456789",
      "product_id_apple": null,
      "product_id_google": null,
      "publication_id": null,
      "coupon_code": null,
      "dirty": false,
      "user_id": null,
      "custom_stylesheet": null,
      "custom_data": null,
      "price_tier": null,
      "cover": null
    }
  ]
}
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}

{% api-method method="get" host="https://www.magloft.com" path="/api/portal/v1/issues/:app_id/:id" %}

{% api-method-summary %}
Get Issue
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **returns** a specific `issue` by `id`
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="string" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="string" required=true %}
Issue ID
{% endapi-method-parameter %}

{% endapi-method-path-parameters %}




{% endapi-method-request %}

{% api-method-response %}

{% api-method-response-example httpCode=200 %}

```json
{
  "id": 1234,
  "title": "Welcome to MagLoft",
  "info": null,
  "hpub": null,
  "source_file": null,
  "source": "typeloft",
  "unlock_type": "free",
  "categories": null,
  "product_id": "purchase.issue_123456789",
  "product_id_apple": null,
  "product_id_google": null,
  "publication_id": null,
  "coupon_code": null,
  "dirty": false,
  "user_id": null,
  "custom_stylesheet": null,
  "custom_data": null,
  "price_tier": null,
  "cover": null
}
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}

{% api-method method="get" host="https://www.magloft.com" path="/api/portal/v1/issues/:app_id/:id/download" %}

{% api-method-summary %}
Download Issue
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **redirects** to a specific `issue` HPUB url
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="string" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="string" required=true %}
Issue ID
{% endapi-method-parameter %}

{% endapi-method-path-parameters %}




{% endapi-method-request %}

{% api-method-response %}

{% api-method-response-example httpCode=200 %}

```json
null
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}

{% api-method method="get" host="https://www.magloft.com" path="/api/portal/v1/issues/:app_id/:id/source" %}

{% api-method-summary %}
Download a specific issue source
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **redirects** to a specific `issue` source file url
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="string" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="string" required=true %}
Issue ID
{% endapi-method-parameter %}

{% endapi-method-path-parameters %}




{% endapi-method-request %}

{% api-method-response %}

{% api-method-response-example httpCode=200 %}

```json
null
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}

{% api-method method="post" host="https://www.magloft.com" path="/api/portal/v1/issues/:app_id" %}

{% api-method-summary %}
Create an Issue
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **creates** a new `issue` and **returns** the saved `issue`
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="string" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% endapi-method-path-parameters %}



{% api-method-body-parameters %}

{% api-method-parameter name="user_id" type="string" %}
Issue User ID
{% endapi-method-parameter %}

{% api-method-parameter name="title" type="string" %}
Issue Title
{% endapi-method-parameter %}

{% api-method-parameter name="info" type="string" %}
Issue information
{% endapi-method-parameter %}

{% api-method-parameter name="date" type="string" %}
Issue publish date
{% endapi-method-parameter %}

{% api-method-parameter name="product_id" type="string" %}
Issue product id
{% endapi-method-parameter %}

{% api-method-parameter name="product_id_apple" type="string" %}
Issue product id (Apple)
{% endapi-method-parameter %}

{% api-method-parameter name="product_id_google" type="string" %}
Issue product id (Google)
{% endapi-method-parameter %}

{% api-method-parameter name="unlock_type" type="string" %}
Unlock Type
{% endapi-method-parameter %}

{% api-method-parameter name="price_tier" type="string" %}
Issue price tier
{% endapi-method-parameter %}

{% api-method-parameter name="design_id" type="string" %}
Issue typeloft theme id
{% endapi-method-parameter %}

{% api-method-parameter name="cover" type="string" %}
Issue Cover
{% endapi-method-parameter %}

{% api-method-parameter name="hpub" type="string" %}
Issue HPUB Path
{% endapi-method-parameter %}

{% api-method-parameter name="source_file" type="string" %}
Issue Source File
{% endapi-method-parameter %}

{% api-method-parameter name="source" type="string" %}
Source type of issue
{% endapi-method-parameter %}

{% api-method-parameter name="categories" type="string" %}
Issue categories
{% endapi-method-parameter %}

{% api-method-parameter name="properties" type="string" %}
Issue properties
{% endapi-method-parameter %}

{% api-method-parameter name="status" type="string" %}

{% endapi-method-parameter %}

{% api-method-parameter name="create_pages" type="string" %}

{% endapi-method-parameter %}

{% api-method-parameter name="publish" type="string" %}

{% endapi-method-parameter %}

{% endapi-method-body-parameters %}

{% endapi-method-request %}

{% api-method-response %}

{% api-method-response-example httpCode=200 %}

```json
{
  "id": 1234,
  "title": "Welcome to MagLoft",
  "info": null,
  "hpub": null,
  "source_file": null,
  "source": "typeloft",
  "unlock_type": "free",
  "categories": null,
  "product_id": "purchase.issue_123456789",
  "product_id_apple": null,
  "product_id_google": null,
  "publication_id": null,
  "coupon_code": null,
  "dirty": false,
  "user_id": null,
  "custom_stylesheet": null,
  "custom_data": null,
  "price_tier": null,
  "cover": null
}
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}

{% api-method method="put" host="https://www.magloft.com" path="/api/portal/v1/issues/:app_id/:id" %}

{% api-method-summary %}
Update an Issue
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **updates** a specific `issue` by `id` and **returns** the updated `issue`
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="string" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="string" required=true %}
Issue ID
{% endapi-method-parameter %}

{% endapi-method-path-parameters %}



{% api-method-body-parameters %}

{% api-method-parameter name="title" type="string" %}
Issue Title
{% endapi-method-parameter %}

{% api-method-parameter name="info" type="string" %}
Issue information
{% endapi-method-parameter %}

{% api-method-parameter name="date" type="string" %}
Issue publish date
{% endapi-method-parameter %}

{% api-method-parameter name="product_id" type="string" %}
Issue product id
{% endapi-method-parameter %}

{% api-method-parameter name="product_id_apple" type="string" %}
Issue product id (Apple)
{% endapi-method-parameter %}

{% api-method-parameter name="product_id_google" type="string" %}
Issue product id (Google)
{% endapi-method-parameter %}

{% api-method-parameter name="unlock_type" type="string" %}
Unlock Type
{% endapi-method-parameter %}

{% api-method-parameter name="price_tier" type="string" %}
Issue price tier
{% endapi-method-parameter %}

{% api-method-parameter name="cover" type="string" %}
Issue Cover
{% endapi-method-parameter %}

{% api-method-parameter name="hpub" type="string" %}
Issue HPUB Path
{% endapi-method-parameter %}

{% api-method-parameter name="source_file" type="string" %}
Issue Source File
{% endapi-method-parameter %}

{% api-method-parameter name="source" type="string" %}
Source type of issue
{% endapi-method-parameter %}

{% api-method-parameter name="categories" type="string" %}
Issue categories
{% endapi-method-parameter %}

{% api-method-parameter name="status" type="string" %}

{% endapi-method-parameter %}

{% api-method-parameter name="custom_data" type="string" %}
Custom Data Hash
{% endapi-method-parameter %}

{% api-method-parameter name="custom_data[language]" type="string" %}

{% endapi-method-parameter %}

{% api-method-parameter name="custom_data[copy_of]" type="string" %}

{% endapi-method-parameter %}

{% api-method-parameter name="properties" type="string" %}
Issue properties
{% endapi-method-parameter %}

{% api-method-parameter name="properties[-baker-page-turn-tap]" type="string" %}

{% endapi-method-parameter %}

{% api-method-parameter name="properties[-baker-vertical-bounce]" type="string" %}

{% endapi-method-parameter %}

{% api-method-parameter name="properties[-baker-max-zoom-level]" type="string" %}

{% endapi-method-parameter %}

{% api-method-parameter name="properties[-baker-dual-spread]" type="string" %}

{% endapi-method-parameter %}

{% api-method-parameter name="properties[default_orientation]" type="string" %}

{% endapi-method-parameter %}

{% api-method-parameter name="properties[orientation_phone]" type="string" %}

{% endapi-method-parameter %}

{% api-method-parameter name="properties[orientation_tablet]" type="string" %}

{% endapi-method-parameter %}

{% api-method-parameter name="properties[converted_to_typeloft]" type="string" %}

{% endapi-method-parameter %}

{% api-method-parameter name="properties[reverse_page_order]" type="string" %}

{% endapi-method-parameter %}

{% api-method-parameter name="properties[link_style]" type="string" %}

{% endapi-method-parameter %}

{% api-method-parameter name="properties[allowed_devices]" type="string" %}

{% endapi-method-parameter %}

{% api-method-parameter name="properties[allowed_platforms]" type="string" %}

{% endapi-method-parameter %}

{% api-method-parameter name="properties[navigator]" type="string" %}

{% endapi-method-parameter %}

{% api-method-parameter name="properties[cover_colors]" type="string" %}

{% endapi-method-parameter %}

{% api-method-parameter name="properties[features]" type="string" %}

{% endapi-method-parameter %}

{% api-method-parameter name="properties[web_url]" type="string" %}

{% endapi-method-parameter %}

{% endapi-method-body-parameters %}

{% endapi-method-request %}

{% api-method-response %}

{% api-method-response-example httpCode=200 %}

```json
{
  "id": 1234,
  "title": "Welcome to MagLoft",
  "info": null,
  "hpub": null,
  "source_file": null,
  "source": "typeloft",
  "unlock_type": "free",
  "categories": null,
  "product_id": "purchase.issue_123456789",
  "product_id_apple": null,
  "product_id_google": null,
  "publication_id": null,
  "coupon_code": null,
  "dirty": false,
  "user_id": null,
  "custom_stylesheet": null,
  "custom_data": null,
  "price_tier": null,
  "cover": null
}
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}

{% api-method method="post" host="https://www.magloft.com" path="/api/portal/v1/issues/:app_id/:id/clone/:magazine_id" %}

{% api-method-summary %}
Clone an Issue
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **creates** a new `issue` by cloning an existing `issue` and **returns** the saved `issue`
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="string" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="string" required=true %}
Issue ID
{% endapi-method-parameter %}

{% api-method-parameter name="magazine_id" type="string" %}
Cloned Issue target magazine ID
{% endapi-method-parameter %}

{% endapi-method-path-parameters %}



{% api-method-body-parameters %}

{% api-method-parameter name="user_id" type="string" required=true %}
Issue User ID
{% endapi-method-parameter %}

{% api-method-parameter name="cloneTitle" type="string" required=true %}
Cloned Issue title
{% endapi-method-parameter %}

{% endapi-method-body-parameters %}

{% endapi-method-request %}

{% api-method-response %}

{% api-method-response-example httpCode=200 %}

```json
{
  "id": 1234,
  "title": "Welcome to MagLoft",
  "info": null,
  "hpub": null,
  "source_file": null,
  "source": "typeloft",
  "unlock_type": "free",
  "categories": null,
  "product_id": "purchase.issue_123456789",
  "product_id_apple": null,
  "product_id_google": null,
  "publication_id": null,
  "coupon_code": null,
  "dirty": false,
  "user_id": null,
  "custom_stylesheet": null,
  "custom_data": null,
  "price_tier": null,
  "cover": null
}
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}

{% api-method method="put" host="https://www.magloft.com" path="/api/portal/v1/issues/:app_id/:id/convert" %}

{% api-method-summary %}
Convert Issue
{% endapi-method-summary %}

{% api-method-description %}
This endpoint converts an `issue` from PDF, EPUB or Folio
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="string" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="string" required=true %}
Issue ID
{% endapi-method-parameter %}

{% endapi-method-path-parameters %}




{% endapi-method-request %}

{% api-method-response %}

{% api-method-response-example httpCode=200 %}

```json
{
  "id": 1234,
  "title": "Welcome to MagLoft",
  "info": null,
  "hpub": null,
  "source_file": null,
  "source": "typeloft",
  "unlock_type": "free",
  "categories": null,
  "product_id": "purchase.issue_123456789",
  "product_id_apple": null,
  "product_id_google": null,
  "publication_id": null,
  "coupon_code": null,
  "dirty": false,
  "user_id": null,
  "custom_stylesheet": null,
  "custom_data": null,
  "price_tier": null,
  "cover": null
}
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}

{% api-method method="put" host="https://www.magloft.com" path="/api/portal/v1/issues/:app_id/:id/pack" %}

{% api-method-summary %}
Pack an issue to HPUB
{% endapi-method-summary %}

{% api-method-description %}
This endpoint pack an `issue` to HPUB and **returns** the `issue`
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="string" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="string" required=true %}
Issue ID
{% endapi-method-parameter %}

{% endapi-method-path-parameters %}




{% endapi-method-request %}

{% api-method-response %}

{% api-method-response-example httpCode=200 %}

```json
{
  "id": 1234,
  "title": "Welcome to MagLoft",
  "info": null,
  "hpub": null,
  "source_file": null,
  "source": "typeloft",
  "unlock_type": "free",
  "categories": null,
  "product_id": "purchase.issue_123456789",
  "product_id_apple": null,
  "product_id_google": null,
  "publication_id": null,
  "coupon_code": null,
  "dirty": false,
  "user_id": null,
  "custom_stylesheet": null,
  "custom_data": null,
  "price_tier": null,
  "cover": null
}
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}

{% api-method method="put" host="https://www.magloft.com" path="/api/portal/v1/issues/:app_id/:id/process_links" %}

{% api-method-summary %}
Process Filename
{% endapi-method-summary %}

{% api-method-description %}
This endpoint process an `issue` filename links in TypeLoft Pages and **returns** an `empty response`  with status `204`
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="string" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="string" required=true %}
Issue ID
{% endapi-method-parameter %}

{% endapi-method-path-parameters %}




{% endapi-method-request %}

{% api-method-response %}

{% api-method-response-example httpCode=200 %}

```json
null
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}

{% api-method method="delete" host="https://www.magloft.com" path="/api/portal/v1/issues/:app_id/:id" %}

{% api-method-summary %}
Delete Issue
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **deletes** a specific `issue` by `id` and **returns** an `empty response`  with status `204`
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="string" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="string" required=true %}
Issue ID
{% endapi-method-parameter %}

{% endapi-method-path-parameters %}




{% endapi-method-request %}

{% api-method-response %}

{% api-method-response-example httpCode=200 %}

```json
null
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}

