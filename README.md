# Mongodump Action

## Example usage

```yml
name: Backup

jobs:
  backup:
    runs-on: ubuntu-latest
    steps:
      - uses: gabrielrufino/mongodump-action
        with:
          connection-string: ${{ secrets.MONGO_URI }}
      - uses: actions/upload-artifact@v3
        with:
          name: dump
          path: ${{ github.workspace }}/dump
```
