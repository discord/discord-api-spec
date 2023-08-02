# Discord OpenAPI Specification

This repository contains the public preview of the [OpenAPI 3.1 specification](https://github.com/OAI/OpenAPI-Specification/blob/main/versions/3.1.0.md) for [Discord's API](https://discord.com/developers/docs/reference). Currently, the spec is only available for the most recent Discord API version ([v10](https://discord.com/developers/docs/reference#api-versioning-api-versions)).

## Usage

### Spec Files

Two versions of the spec are included—the standard spec and the preview spec:

- [`openapi.json`](specs/openapi.json) is the standard spec that contains the stable, public API.
- [`openapi_preview.json`](specs/openapi_preview.json) is the preview spec which contains unstable and/or experimental API features. **This should not be considered stable** or used in production environments.

### Integrating with Postman

To use the spec with Postman, you can view the [public collection](https://www.postman.com/discord-api).

## Contributing

OpenAPI spec contents are automatically generated, and therefore **we do not allow public contributions to this repo**.

🐛 For bug fixes or improvements, you can [open an issue](https://github.com/discord/discord-api-spec/issues).