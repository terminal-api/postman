# Terminal Postman Collection

## Usage 🚀

1. Download the generated collection [here](./postman) ✨
2. Import the collection into Postman
3. Setup a Postman environment (learn more about Postman environments [here](https://learning.postman.com/docs/sending-requests/managing-environments/)):
    - Sandbox:
      - Create a new environment called `Terminal Sandbox`
      - Add a variable called `secretKey` and set it to your Terminal Sandbox Secret key
      - Add a variable called `baseUrl` and set it to `https://api.sandbox.withterminal.com/tsp/v1`
    - Production:
      - Create a new environment called `Terminal Production`
      - Add a variable called `secretKey` and set it to your Terminal Production Secret key
      - Add a variable called `baseUrl` and set it to `https://api.withterminal.com/tsp/v1`
4. Select the environment you want to use in the top right corner of Postman
5. Make requests!

### Variables

This collection uses the following variables to make it easy to chain requests together:
- `baseUrl`
- `secretKey`
- `connectionToken`
- `vehicleId`
- `driverId`
- `syncId`

> **Note:** You can set these variables in your environment or collection. Some will be set automatically for you based on the response of previous requests.

### Connection Tokens

Terminal uses connection tokens to authenticate requests targeting a specific connection. Please set a `connectionToken` variable in your collection's variables to use connection tokens. You can retrieve connection tokens in the dashboard or by calling `GET /connections`.

> **Note:** When calling `POST /public-token/exchange` the connection token is set automatically for you upon successful exchange.

## Development ⚒️

#### Setup Project
Setup the project if you haven't already:

```bash
git clone git@github.com:terminal-api/postman.git
npm install
```

#### Generate Collection
Generate the collection using the following command:

```bash
npm run generate
```