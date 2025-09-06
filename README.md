# Mix Hawk Music - MkDocs

This repository serves the mirrored content of mixhawkmusic.com via MkDocs.

## Local preview

Prerequisites: Python 3 and mkdocs installed

  ```shell
  python -m venv venv
  source venv/bin/activate 
  pip install mkdocs-material
  pip install mkdocs-mermaid2-plugin
  ```

Run the local server:
```shell
source venv/bin/activate
mkdocs serve
```
Open http://127.0.0.1:8000 in your browser.

## Rebuild the mirror (optional)
If you need to refresh the mirrored site assets/content:

```bash
wget \
  --mirror \
  --convert-links \
  --page-requisites \
  --adjust-extension \
  --no-parent \
  --reject "index.html?*" \
  -e robots=off \
  --wait=1 \
  --random-wait \
  -P ./site \
  http://mixhawkmusic.com/
```

