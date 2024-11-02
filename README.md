# FleetWorks Documentation

### 👩‍💻 Development

Install the [Mintlify CLI](https://www.npmjs.com/package/mintlify) to preview the documentation changes locally. To install, use the following command

```
npm i -g mintlify
```

Install `openapi-generator-cli`

```
npm install @openapitools/openapi-generator-cli -g
```

Run the following command at the root of your documentation (where mint.json is)

```
openapi-generator-cli generate -g openapi -i openapi/fleetworks.yaml -o openapi --additional-properties="outputFileName=fleetworks_openapi.json"

mintlify dev
```

### 😎 Publishing Changes

Install our Github App to autopropagate changes from youre repo to your deployment. Changes will be deployed to production automatically after pushing to the default branch. Find the link to install on your dashboard.

#### Troubleshooting

- Mintlify dev isn't running - Run `mintlify install` it'll re-install dependencies.
- Page loads as a 404 - Make sure you are running in a folder with `mint.json`
