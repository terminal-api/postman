# Terminal Postman Collection

## Usage 🚀

1. Download the generated collection [here](./postman/terminal.postman_collection.json) ✨
2. Import the collection into Postman
3. Setup a Postman environment for both Sandbox + Production (learn more about Postman environments [here](https://learning.postman.com/docs/sending-requests/managing-environments/)):
    - Sandbox:
      - Download the template sandbox environment [here](./postman/environments/sandbox.postman_environment.json)
      - Import environment into Postman
      - Set `secretKey` to your Terminal Sandbox Secret key
    - Production:
      - Download the template production environment [here](./postman/environments/production.postman_environment.json)
      - Import environment into Postman
      - Set `secretKey` to your Terminal Production Secret key
4. Select the environment you want to use in the top right corner of Postman
5. Make requests!

### Getting Started Video 🎥

Here's a video that shows you how you can get started with Terminal

<div>
    <a href="https://www.loom.com/share/c8f94e90f97146a58b94401c2838166c">
      <p>Creating Your First Connection with Terminal - Watch Video</p>
    </a>
    <a href="https://www.loom.com/share/c8f94e90f97146a58b94401c2838166c">
      <img style="max-width:300px;" src="https://cdn.loom.com/sessions/thumbnails/c8f94e90f97146a58b94401c2838166c-with-play.gif">
    </a>
  </div>

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

Terminal uses connection tokens to authenticate requests targeting a specific connection. Please set a `connectionToken` variable in your environment variables if you'd like to act on a specific connection. You can retrieve connection tokens in the dashboard or by calling `GET /connections`.

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