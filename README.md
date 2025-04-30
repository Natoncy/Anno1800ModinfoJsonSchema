# Anno 1800 Modinfo JSON Schema

This repository provides a JSON Schema for validating modinfo.json files in VS Code.
This is useful for suggestions for properties, autocomplete and checking for required properties.

## How to install

1. In VS Code select the search bar at the top center and search for ">user settings json" (do not forget the ">").
2. Select the one result, it will open a settings.json file.
3. Add a property "json.schemas" (if it does not already exists) and add the following content like this:
~~~
"json.schemas": [
    {
        "fileMatch": ["modinfo.json"],
        "url": "https://raw.githubusercontent.com/Natoncy/Anno1800ModinfoJsonSchema/refs/heads/main/modinfo.schema.json"
    }
]
~~~
4. Save and restart VS Code.

## How to use

When you open your modinfo.json you should see yellow markings where there are errors.
If you hover over a property you should see a tooltip with the description and errors if any exists.
For example: Change your "Version" to "test". It should be marked yellow and the tooltip should say "String does not match the pattern of ..." and the description for the property.

Pressing Ctrl + Spacebar will give you suggestions for the current cursor position in the file.
