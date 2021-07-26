# JSON Resume
This extension provides IntelliSense and validation support for JSON Resume
files.

## Archived
This project has been archived as this functionality can already be configured
within Visual Studio Code.

Go to your Visual Studio Code preferences (`CTRL` + `,`), and configure the
`json.schemas` setting, which is contributed by the built-in JSON extension,
[JSON Language Features](https://code.visualstudio.com/docs/languages/json#_json-schemas-and-settings).

```json
{
  "json.schemas": [
    {
      "fileMatch": [
        "resume.json",
        "*.resume.json"
      ],
      "url": "https://raw.githubusercontent.com/jsonresume/resume-schema/v1.0.0/schema.json"
    }
  ]
}
```

You may also want to join the discussion and thumbs-up
[microsoft/vscode#26289](https://github.com/microsoft/vscode/issues/26289),
which would add support for pulling schemas from
[JSON Schema Store](https://www.schemastore.org/json/) automatically.

This is similar to the behavior the [YAML](https://marketplace.visualstudio.com/items?itemName=redhat.vscode-yaml)
extension provides. Try to create a `resume.yml` or `.resume.yml` file,
IntelliSense already works with no configuration necessary.

## Features
To use this plugin, open a JSON Resume file named either `resume.json` or with
a name ending in `.resume.json`.

### IntelliSense
To activate IntelliSense, press `CTRL` + `SPACE` where you want to enter a new
field.

![IntelliSense Preview](assets/vscode-jsonresume-intellisense-preview.gif)

### Validation
Validation is automatic. To see issues with your resume, open the `Problems`
tab.

![Validation Preview](assets/vscode-jsonresume-validation-preview.gif)
