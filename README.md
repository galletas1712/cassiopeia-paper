## Build
To build, ensure tectonic is installed and run the following:
```
tectonic -X build
```

The output PDF will be at `build/index/index.pdf`.

## VSCode

To compile on save in VSCode, add the following to settings.
```json
"latex-workshop.latex.recipe.default": "tectonic",
"latex-workshop.latex.autoBuild.run": "onSave",
"latex-workshop.latex.outDir": "%WORKSPACE_FOLDER%/build/index",
"latex-workshop.view.pdf.viewer": "tab",
"latex-workshop.latex.recipes": [
    {
    "name": "tectonic",
    "tools": ["tectonic"]
    }
],
"latex-workshop.latex.tools": [
    {
    "name": "tectonic",
    "command": "tectonic",
    "args": ["-X", "build", "--keep-intermediates", "--keep-logs"],
    "env": {}
    }
],
"latex-workshop.bibtex-format.sort.enabled": true,
```