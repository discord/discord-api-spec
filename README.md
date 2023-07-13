# Discord OpenAPI Specification

This repository contains the [OpenAPI specification](https://spec.openapis.org/oas/latest.html) for [Discord's API](https://discord.com/developers/docs/reference). Currently, the spec is only for the most recent Discord API version ([v10](https://discord.com/developers/docs/reference#api-versioning-api-versions)).

> ⚙️ OpenAPI spec contents are automatically generated, and therefore we do not allow public contributions to this repo. For bug fixes or improvements, you can [open an issue](https://github.com/discord/discord-api-spec/issues).

## Usage

### Spec Files

Two versions of the spec are included—the standard spec and the preview spec:

- [`openapi.json`](specs/openapi.json) is the standard spec that contains the stable, public API. If you're using the spec in a production environment, you should use this spec.
- [`openapi_preview.json`](specs/openapi_preview.json) is the preview spec which contains unstable and/or experimental API features. **This should not be considered stable** nor used in production environments.

### Integrating with Postman

To use the spec with Postman, you can view the [public collection](https://www.postman.com/discord-api).
