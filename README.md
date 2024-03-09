# Build

Building the ODA Open API SDK for Node.js.

# Tooling

* Install [Node.js](https://nodejs.org/en/download/current)
* Install [npm](https://www.npmjs.com/package/npm)
* Install [OpenAPI Generator](https://openapi-generator.tech/docs/installation)

# Generate

Generate a server for each ODA Open API.

## TMF634

```bash
$ openapi-generator-cli generate --generator-name nodejs-express-server --output tmf634/server --additional-properties packageName=tmf634 -i https://raw.githubusercontent.com/tmforum-apis/TMF634_ResourceCatalog/master/TMF634-ResourceCatalog-v4.1.0.swagger.json

```

## TMF639

```bash
$ openapi-generator-cli generate --generator-name nodejs-express-server --output tmf639/server --additional-properties packageName=tmf639 -i https://raw.githubusercontent.com/tmforum-apis/TMF639_ResourceInventory/master/TMF639-ResourceInventory-v4.0.0.swagger.json
```

# Build & Test

## Build TMF 634 server
```bash
$ cd tmf634/server
$ npm start
```

## Test request to TMF 634 server
```bash
$ curl -vs -H 'Accept: application/json' http://localhost:8080/tmf-api/resourceCatalog/v4/resourceSpecification
```
