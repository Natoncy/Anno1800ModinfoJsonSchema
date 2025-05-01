# Anno 1800 Modinfo JSON Schema

This repository provides a JSON Schema for validating `modinfo.json` files in Visual Studio Code.  
It enables features like autocomplete, property suggestions, and validation of required fields and values.

The rules are based on: [https://github.com/anno-mods/Modinfo/blob/master/modinfo-format.md](https://github.com/anno-mods/Modinfo/blob/master/modinfo-format.md)

## Installation

To enable the schema in VS Code:

1. Open the Command Palette (`Ctrl+Shift+P`).
2. Search for and select **"Open User Settings (JSON)"**.
3. Add (or extend) the `json.schemas` section with the following:

   ```json
   "json.schemas": [
       {
           "fileMatch": ["modinfo.json"],
           "url": "https://raw.githubusercontent.com/Natoncy/Anno1800ModinfoJsonSchema/refs/heads/main/modinfo.schema.json"
       }
   ]
   ```

4. Save the file and restart VS Code.

## Usage

Once configured:

- Opening a `modinfo.json` file will automatically apply the validation.
- Errors will be highlighted with yellow lines.
- Hovering over properties displays tooltips with descriptions and validation messages.
  - For example, setting `"Version": "test"` will trigger a validation warning because it doesn't match the expected pattern.
- Press `Ctrl + Space` to see autocomplete suggestions for the current cursor position.
