<h1 align="center">OpenAPI Command Line Tool</h1>

[![CI](https://github.com/openapistack/openapicmd/workflows/CI/badge.svg)](https://github.com/openapistack/openapicmd/actions?query=workflow%3ACI)
[![License](http://img.shields.io/:license-mit-blue.svg)](https://github.com/openapistack/openapicmd/blob/main/LICENSE)
[![npm version](https://img.shields.io/npm/v/openapicmd.svg)](https://www.npmjs.com/package/openapicmd)
[![npm downloads](https://img.shields.io/npm/dw/openapicmd.svg)](https://www.npmjs.com/package/openapicmd)
![npm type definitions](https://img.shields.io/npm/types/openapicmd.svg)
[![Buy me a coffee](https://img.shields.io/badge/donate-buy%20me%20a%20coffee-orange)](https://buymeacoff.ee/anttiviljami)

<p align="center">openapicmd - The CLI for all things OpenAPI and Swagger</p>

<p align="center"><i>Battle-tested in production. <a href="https://openapistack.co/users/">See who uses openapi-stack →</a></i></p>

# Install

```
npm install -g openapicmd
openapi help
```

# Features
- [x] Parse local and remote JSON/YAML OpenAPI definition files
- [x] Generate TypeScript types from OpenAPI definitions
- [x] Emit client-oriented types for openapi-client-axios
- [x] Optionally strip metadata and prune unreferenced components before generation

# Commands
<!-- commands -->
* [`openapi help [COMMAND]`](#openapi-help-command)
* [`openapi typegen [DEFINITION]`](#openapi-typegen-definition)

## `openapi help [COMMAND]`

Display help for openapi.

```
USAGE
  $ openapi help [COMMAND...] [-n]

ARGUMENTS
  [COMMAND...]  Command to show help for.

FLAGS
  -n, --nested-commands  Include all nested commands in the output.

DESCRIPTION
  Display help for openapi.
```

_See code: [@oclif/plugin-help](https://github.com/oclif/plugin-help/blob/v6.2.8/src/commands/help.ts)_

## `openapi typegen [DEFINITION]`

Generate types from openapi definition

```
USAGE
  $ openapi typegen [DEFINITION] [-h] [-D] [-B] [-R /] [-H <value>...] [-V] [-S http://localhost:9000...] [-I
    {"info":{"version":"1.0.0"}}...] [-E x-internal] [-C default|all|openapi_client_axios] [-U] [-b <value>] [-A]

ARGUMENTS
  [DEFINITION]  input definition file

FLAGS
  -A, --[no-]type-aliases                       Generate module level type aliases for schema components defined in spec
  -B, --bundle                                  resolve remote $ref pointers
  -C, --strip=default|all|openapi_client_axios  Strip optional metadata such as examples and descriptions from
                                                definition
  -D, --dereference                             resolve $ref pointers
  -E, --exclude-ext=x-internal                  Specify an openapi extension to exclude parts of the spec
  -H, --header=<value>...                       add request headers when calling remote urls
  -I, --inject={"info":{"version":"1.0.0"}}...  inject JSON to definition with deep merge
  -R, --root=/                                  override API root path
  -S, --server=http://localhost:9000...         override servers definition
  -U, --[no-]remove-unreferenced                Remove unreferenced components, you can skip individual component being
                                                removed by setting x-openapicmd-keep to true
  -V, --validate                                validate against openapi schema
  -b, --banner=<value>                          include a banner comment at the top of the generated file
  -h, --help                                    Show CLI help.

DESCRIPTION
  Generate types from openapi definition

EXAMPLES
  $ openapi typegen ./openapi.yml > openapi.d.ts
```

_See code: [src/commands/typegen.ts](https://github.com/openapistack/openapicmd/blob/v3.0.0/src/commands/typegen.ts)_
<!-- commandsstop -->

## Commercial support

For assistance with using openapicmd in your company, reach out at support@openapistack.co.

## Contributing

`openapicmd` is Free and Open Source Software. Issues and pull requests are more than welcome!
