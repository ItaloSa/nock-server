# Nock Mock Server

[![npm](https://img.shields.io/npm/v/nock-mock-server.svg)](https://www.npmjs.com/package/nock-mock-server)
[![License](https://img.shields.io/github/license/italosa/nock-mock-server.svg)](https://github.com/italosa/nock-mock-server/blob/main/LICENSE.md)

A simple mock server powered by [nock](https://github.com/nock/nock).

## Installation

Install the package using npm:

```sh
npm install nock-mock-server
```

## Usage

Create a mock server instance and add mocks:

```js
// index.js
const { NockMockServer } = require("nock-mock-server");

const PORT = 3000;
const nockServer = new NockMockServer();

nockServer.addMock((nockInstance) => {
  nockInstance.get("/").reply(200, { message: "Hello World" });
});

nockServer.start(PORT, () => {
  console.log("Nock server started");
});
```

## Examples

You can find more examples in the [examples](./examples/) directory.

<!-- ## Contributing

Contributions are welcome! Please see the [contributing guidelines](CONTRIBUTING.md) for more information. -->

## License

This project is licensed under the MIT License. See the [LICENSE](https://github.com/italosa/nock-mock-server/blob/main/LICENSE.md) file for details.
