# Discord OpenAPI Specification

This repository contains the public preview of the [OpenAPI 3.1 specification](https://github.com/OAI/OpenAPI-Specification/blob/main/versions/3.1.0.md) for [Discord's API](https://discord.com/developers/docs/reference). Currently, the spec is only available for the most recent Discord API version ([v10](https://discord.com/developers/docs/reference#api-versioning-api-versions)).

> ⚠️ The public preview of the OpenAPI spec is subject to breaking changes without advance notice, and should not be used within production environments.

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

## Spec conventions
- This is a preview and it may be not correct. If you find discrepancies between the spec and our [docs](https://discord.com/developers/docs), other than the ones mentioned below, let us know, and follow the docs, not the spec.
- Even though we define `anyOf` and `oneOf` unions, they all mean that only one type from the list can be used as a data format. E.g. `anyOf: {'Cat', 'Dog'}`, still means that you can either pass `Cat` or `Dog`, not `Cat+Dog`. This is signified by the custom extension `x-discord-union: oneOf`. We use `anyOf` when we technically can’t use `oneOf`. One of the reasons to do that is e.g. when all the fields are optional and the passed in data could be validated with more than one format.
- We avoid over-specifying response fields and merely define field types, like `int32`, and we avoid defining specific minimums, maximums, etc.
- Some fields typed as strings in our docs may be typed as ints in the spec. Our API accepts strings for int fields if they are parseable as ints. We think it’ll be more precise to spec these int-parseable strings as ints.

## Known issues
- (almost) All nullable fields are additionally marked as optional and all optional fields are additionally marked as nullable.
- Operations and fields don’t have descriptions.
- Operations don’t have tags.
- Flag fields don’t detail specific flag values and their meaning.
- Optional query args are typed as nullable, even though it doesn’t make much sense.