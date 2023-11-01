# Kairos publish action

This action will run `kubectl` to update the given deployment container with a new image
Publish the received content to [kairos](https://github.com/resuelve/kairos) server

## Inputs

| Input        | Required | Description                                                             |
|--------------|----------|-------------------------------------------------------------------------|
| kairos_url   | yes      | Kairos server publish endpoint                                          |
| kairos_token | yes      | Authentication token to be able to upload artifacts                     |
| zipile       | yes      | zipfile that will be published to Kairos server                         |

## Usage

```yaml
- name: Publish to Kairos
  uses: resuelve/kairos-publish-action@v1
    with:
      kairos_url: ${{ secrets.KAIROS_URL }}
      kairos_token: ${{ secrets.KAIROS_TOKEN }}
      zipile: PATH_TO_ZIPFILE
```

Enjoy 🎉
