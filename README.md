# REST Client

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
