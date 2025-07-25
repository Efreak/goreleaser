# Introduction

GoReleaser can be customized by tweaking a `.goreleaser.yaml`[^goreleaser-yaml] file.

You can generate an example config by running
[`goreleaser init`](../cmd/goreleaser_init.md) or start from scratch.

You can also check if your config is valid by running
[`goreleaser check`](../cmd/goreleaser_check.md), which will tell you if are
using deprecated or invalid options.

## JSON Schema

GoReleaser also has a [jsonschema][] file, which you can use to have better
editor support:

=== "OSS"

    ```sh
    https://goreleaser.com/static/schema.json
    ```

    You can also specify it in your `.goreleaser.yml` config file by adding a
    comment like the following:
    ```yaml
    # yaml-language-server: $schema=https://goreleaser.com/static/schema.json
    ```

=== "Pro"

    ```sh
    https://goreleaser.com/static/schema-pro.json
    ```

    You can also specify it in your `.goreleaser.yml` config file by adding a
    comment like the following:
    ```yaml
    # yaml-language-server: $schema=https://goreleaser.com/static/schema-pro.json
    ```

You can also generate it for your specific version using the
[`goreleaser jsonschema`][schema] command.

### Pin the schema version

You can pin the version by getting the schema from the GitHub tag, for example,
for `__VERSION__` (latest):

=== "OSS"

    ```sh
    https://raw.githubusercontent.com/goreleaser/goreleaser/__VERSION__/www/docs/static/schema.json
    ```

=== "Pro"

    ```sh
    https://raw.githubusercontent.com/goreleaser/goreleaser/__VERSION__/www/docs/static/schema-pro.json
    ```

[^goreleaser-yaml]:
    While most of the documentation refers to the `.goreleaser.yaml` filename
    for simplicity, a few different variants of it are actually accepted.
    In order of precedence:

    - `.config/goreleaser.yml`
    - `.config/goreleaser.yaml`
    - `.goreleaser.yml`
    - `.goreleaser.yaml`
    - `goreleaser.yml`
    - `goreleaser.yaml`
    - `.github/goreleaser.yml`
    - `.github/goreleaser.yaml`

[jsonschema]: http://json-schema.org/draft/2020-12/json-schema-validation.html
[schema]: ../cmd/goreleaser_jsonschema.md
