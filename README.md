# REST Client

REST Client is a Visual Studio Code extension developed by Huachao Mao that enables developers to send HTTP requests and view responses directly within the VS Code editor. It supports RFC 2616 HTTP request format using .http and .rest files, GraphQL queries, cURL commands, multiple authentication schemes (Basic, Digest, SSL Client Certificates, Azure AD, AWS Signature v4, AWS Cognito), environment and file variables, request chaining, cookie management, code generation to multiple languages, and response saving. The extension is installed via the VS Code Marketplace under the identifier `humao.rest-client`.

**VS Code Marketplace:** [humao.rest-client](https://marketplace.visualstudio.com/items?itemName=humao.rest-client)  
**GitHub:** [github.com/Huachao/vscode-restclient](https://github.com/Huachao/vscode-restclient)

## Tags

`Clients` `HTTP Client` `IDE Extension` `VS Code` `API Testing` `GraphQL` `cURL`

## Timestamps

- **Created:** 2026-03-27
- **Modified:** 2026-05-02

## APIs

| Name | Description | URL |
|---|---|---|
| REST Client | VS Code extension for HTTP requests | [VS Code Marketplace](https://marketplace.visualstudio.com/items?itemName=humao.rest-client) |

## Artifacts

| Type | Name | Link |
|---|---|---|
| Documentation | README | [GitHub README](https://github.com/Huachao/vscode-restclient#readme) |
| Getting Started | Usage Guide | [GitHub Usage](https://github.com/Huachao/vscode-restclient#usage) |
| JSON Schema | HTTP Request Schema | [json-schema/rest-client-request-schema.json](json-schema/rest-client-request-schema.json) |
| JSON Structure | Request Structure | [json-structure/rest-client-request-structure.json](json-structure/rest-client-request-structure.json) |
| JSON-LD Context | REST Client Context | [json-ld/rest-client-context.jsonld](json-ld/rest-client-context.jsonld) |
| Vocabulary | REST Client Vocabulary | [vocabulary/rest-client-vocabulary.yml](vocabulary/rest-client-vocabulary.yml) |
| Example | GET Request Example | [examples/rest-client-get-request-example.json](examples/rest-client-get-request-example.json) |
| Example | Request Chaining Example | [examples/rest-client-request-chaining-example.json](examples/rest-client-request-chaining-example.json) |

## Quick Example

Create a file `requests.http`:

```http
@host = https://api.example.com
@token = your-token-here

### Get User
GET {{host}}/v1/users/42 HTTP/1.1
Authorization: Bearer {{token}}
Accept: application/json

### Create User
POST {{host}}/v1/users HTTP/1.1
Content-Type: application/json
Authorization: Bearer {{token}}

{
  "name": "Jane Doe",
  "email": "jane@example.com"
}
```

Press `Ctrl+Alt+R` (Windows/Linux) or `Cmd+Alt+R` (macOS) to send the request under the cursor.

## Key Features

- **.http and .rest file format** for authoring requests as text files
- **Multiple requests per file** separated by `###`
- **Environment variables** for switching between dev/staging/production
- **Request chaining** via `# @name` and `{{requestName.response.body.$.field}}`
- **GraphQL support** with query and variables
- **cURL import/export** — run curl commands directly
- **Code generation** — export to Python, JavaScript, C#, Java, and more
- **Authentication** — Basic, Digest, Azure AD, AWS Signature v4, Certificates
- **System variables** — `{{$guid}}`, `{{$timestamp}}`, `{{$randomInt}}`

## Installation

```
F1 → ext install humao.rest-client
```

Or search "REST Client" in VS Code Extensions panel.

## Maintainers

**Kin Lane** — kin@apievangelist.com
