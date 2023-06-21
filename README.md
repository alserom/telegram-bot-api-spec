# Telegram Bot API specification [![Bot API version](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fgithub.com%2Falserom%2Ftelegram-bot-api-spec%2Fraw%2Fmain%2Fversion.json&query=%24.version&style=flat-square&logo=telegram&label=Bot%20API&color=2CA5E0)](https://core.telegram.org/bots/api)

[![Validation status](https://github.com/alserom/telegram-bot-api-spec/actions/workflows/validate.yml/badge.svg?branch=main)](https://github.com/alserom/telegram-bot-api-spec/actions/workflows/validate.yml?query=branch%3Amain)
[![Scraping status](https://github.com/alserom/telegram-bot-api-spec/actions/workflows/scrape.yml/badge.svg?branch=main)](https://github.com/alserom/telegram-bot-api-spec/actions/workflows/scrape.yml?query=branch%3Amain)

This repository contains [Telegram Bot API](https://core.telegram.org/bots/api) specifications in a comfortable format for autogenerating any kind of *telegram-bot-related* libs and modules.

Automatically checking for any changes in official docs runs ***every day at 20:00 UTC***. In case of any update is detected - this repository will be updated too (<sub><sup>*as soon as someone will check, approve & merge automatically created PR :tired_face:*</sup></sub>).

## About files

| File                                  | Description |
| - | - |
| [spec.json](spec.json)                | Description of Telegram Bot API docs as JSON specification in a custom format. Check out the `spec.schema.json` document to understand the format. Also, check notes about [Data type definitions](#data-type-definitions). |
| [spec.min.json](spec.min.json)        | A compressed version of the `spec.json` file. |
| [spec.schema.json](spec.schema.json)  | JSON Schema document to annotate and validate `spec.json & spec.min.json`. |
| [openapi.json](openapi.json)          | Description of Telegram Bot API docs as OpenAPI specification. Uses `OAS 3.1.0`. |
| [openapi.min.json](openapi.min.json)  | A compressed version of the `openapi.json` file. |
| [version.json](version.json)          | Holds the current Bot API version under the `version` key. Nothing more. Can be used to show a pretty badge :wink: |

### Data type definitions

> This notes regards data types used in the `spec.json` specification.

Here how possible data types are described.

**Scalars:**
- `string`
- `int32`
- `int64`
- `float`
- `boolean`

**Objects:** Just an object name that starts with a capital letter. E.g. `User`, `Chat`, `Message`, etc.

**Arrays:** Describes in format `array<type|type2|typeN>`. For example:
- `array<Message>` - this means that *EACH ITEM* of this array has the type `Message`.
- `array<Message|string>` - this means that *EACH SEPARATE ITEM* of this array can be the type  `Message` or a type `string`.
- `array<>` or `array` - this means that *EACH SEPARATE ITEM* of this array can be of any type.

## Links

Check these resources to find out what is Telegram Bots and how to work with them.

- [Official Telegram docs - Bots: An introduction for developers](https://core.telegram.org/bots)
- [Official Telegram docs - Detailed Guide to Bot Features](https://core.telegram.org/bots/features)
- [Official Telegram docs - Full API Reference for Developers](https://core.telegram.org/bots/api)

## Alternatives

Here are some alternatives which inspire me to create this repository. They are pretty good but do not meet my needs, so maybe you will be interested.

- [PaulSonOfLars/telegram-bot-api-spec](https://github.com/PaulSonOfLars/telegram-bot-api-spec)  
Repository with a simple JSON description of the telegram bot API which updates itself every day. Also, have a scraper written in Python.
- [sys-001/telegram-bot-api-versions](https://github.com/sys-001/telegram-bot-api-versions)  
Repository with schemas for all versions of the Telegram bot API. Contains schemas in `postman`, `openapi`, and `custom` JSON formats.

## Contributing

If you want to improve this repository, feel free to create PRs and open issues to discuss what you would like to improve or change.

Also, take a look at the [alserom/tg-bot-api-spec](https://github.com/alserom/tg-bot-api-spec) tool that is used to generate spec files. In most cases, changes regarding spec files should be applied to this tool.

## License

[![Licence](https://img.shields.io/github/license/alserom/tg-bot-api-spec?style=flat-square)](LICENSE.md)
