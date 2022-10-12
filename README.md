# bsm# For info on getting the latest rdme version and obtaining your API_DEFINITION_ID,
# see our docs: https://docs.readme.com/docs/rdme#example-syncing-an-openapi-definition
name: Sync OAS to ReadMe
on:
  push:
    branches:
      - main
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - uses: readmeio/rdme@7.3.0
        with:
          rdme: openapi [file] --key=rdme_xn8s9h9104e4cef1fcefe8bf651fa0defcc891ebd04f1b1cca7f18d25e72421cfffa86 --id=API_DEFINITION_ID
