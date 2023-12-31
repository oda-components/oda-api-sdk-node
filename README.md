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
$ openapi-generator-cli generate --generator-name nodejs-express-server --output tmf634 --additional-properties packageName=tmf634 -i https://tmf-open-api-table-documents.s3.eu-west-1.amazonaws.com/OpenApiTable/4.1.0/swagger/TMF634-ResourceCatalog-v4.1.0.swagger.json

```

## TMF639

```bash
$ openapi-generator-cli generate --generator-name nodejs-express-server --output tmf639 --additional-properties packageName=tmf639 -i https://tmf-open-api-table-documents.s3.eu-west-1.amazonaws.com/OpenApiTable/4.0.0/swagger/TMF639-ResourceInventory-v4.0.0.swagger.json
```

# Build & Test

## Build TMF 634 server
```bash
$ cd tmf634
$ npm start
```

## Test request to TMF 634 server
```bash
$ curl -vs -H 'Accept: application/json' http://localhost:8080/tmf-api/resourceCatalog/v4/resourceSpecification
```
