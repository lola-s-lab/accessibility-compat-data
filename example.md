# Example Data Set
This is an example of what the data for ACD _could_ look like, it's an experimentation.

The data includes versions for both the browser and the assitive technology,
how it's currently displayed is inelegant and confusing, which leads to the question of how
to best display version numbers which may vary as attributes for the element may become available
in different versions of the same browser. E.g. NVDA version 1 may implement `<a>` but `href` may
be implemented in NVDA version 2.

The note section isn't included in the tabluar representaion of the data as I think this may be 
better displayed as a note/accessibility consideration highlighted on the page outside of the table.

## JSON Representation of Data
```json
"a": {
    "chrome": [
      "v140",
      {
        "nvda": ["v1.4", "supported"],
        "jaws": ["v2.4", "supported"],
      }
    ],
    "firefox": [
      "v209",
      {
        "nvda": ["v1.4", "supported"],
        "jaws": ["v2.4", "not supported"],
      }
    ],
    "edge": [
      "v56",
      {
        "nvda": ["v1.4", "not supported"],
        "jaws": ["v2.4", "supported"],
      }
    ]
    "safari": [
      "v45",
      {
        "voice-over": ["v1.4", "supported"],
      }
    ]
  "href": {
    "chrome": [
      "v300",
      {
        "nvda": ["v1.6", "supported"],
        "jaws": ["v40.4", "supported"],
      }
    ],
    "firefox": [
      "v209",
      {
        "nvda": ["v1.4", "supported"],
        "jaws": ["v2.4", "not supported"],
      }
    ],
    "edge": [
      "v56",
      {
        "nvda": ["v1.4", "not supported"],
        "jaws": ["v2.4", "supported"],
      }
    ]
    "safari": [
      "v45",
      {
        "voice-over": ["v1.4", "supported"],
      }
    ]
  }
  "note": "There may be some specific notes we want to call out here or in the accessibility considerations section."
}
```

## Tabluar Represenation of Data

|              | CHROME              |                      | FIREFOX             |                         | EDGE                   |                    | SAFARI             |
|------------- |-------------------- |--------------------- |-------------------- |------------------------ |----------------------- |------------------- |------------------- | 
|              | **NVDA**            | **JAWS**             | **NVDA**            | **JAWS**                |  **NVDA**              | **JAWS**           | **VoiceOver**      |
| a            | Supported v140/v1.4 | Supported v140/v1.4  | Supported v209/v1.4 | Not Supported v209/v2.4 | Not Supported v56/v1.4 | Supported v56/v2.4 | Supported v45/v1.4 |
| href         | Supported v300/v1.6 | Supported v500/v40.4 | Supported v209/v1.4 | Not Supported v209/v2.4 | Not Supported v56/v1.4 | Supported v56/v2.4 | Supported v45/v1.4 |

## Image Representation of Data

<img width="788" height="100" alt="A table representation of the JSON and tabular data" src="https://github.com/user-attachments/assets/bf0345d1-aaed-47f4-bbf8-eac4c229c482" />
