---
title: search
order: 2
component: false
appliesTo: Vertical
apiProperties:
  - property: verticalKey
    type: string
    required: false
    description: The vertical key to use for searches, passed to certain components. Required if a `defaultInitialSearch` is supplied.
  - property: limit
    type: string
    required: false
    default: 20
    description: The number of results to display per page, defaults to 20. Maximum is 50.
  - property: defaultInitialSearch
    type: string
    required: false
    description: A default search to use on page load when the user hasn't provided a query. If set to "", the `SearchBar`'s `allowEmptySearch` must be set to `true`.
  - property: universalLimit
    type: object
    description: An object containing the number of results to display per vertical key. Minimum is 1. Maximum is 50.
    properties:
      - property: [verticalKey]
        type: number
        default: 20
        description: The limit for this vertical on universal 
---

## Background
The `search` configuration in the initialization is used to control the default initial search and the number of results per page. It can be used to set a default initial search on both vertical and universal search pages.

```js
    search: {
      verticalKey: 'verticalKey', //don't specify this property if universal
      limit: '20', //not applicable to universal search, see universalLimit
      defaultInitialSearch: 'What is Yext Answers?',
      universalLimit: {
        locations: 5, //only display 5 results for the locations vertical in universal
      },
    }
```
## Example
{{% codesandbox zen-mahavira-rboyd %}}
