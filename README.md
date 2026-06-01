# `Create missing release`

Create a GitHub release for a given tag if the release does not already exist.

## Example Usage

```yaml
  create-release:
    runs-on: ubuntu-latest
    steps:
      - uses: infrabits/ci-create-missing-release@main
        with:
          tag: example
          github-token: ${{ secrets.GITHUB_TOKEN }}
```

### With artifacts

```yaml
  create-release:
    runs-on: ubuntu-latest
    steps:
      - uses: infrabits/ci-create-missing-release@main
        with:
          tag: example
          github-token: ${{ secrets.GITHUB_TOKEN }}
          artifacts: |
            dist/*.tar.gz
            dist/*.zip
```
