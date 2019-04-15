# My Serverless App

## Startup
* Ensure you have Node.js (at least LTS) and NPM installed on your machine
* Configure `serverless` AWS credentials https://serverless.com/framework/docs/providers/aws/guide/credentials/

### Local Development
* `npm i`
* `serverless dynamodb install`
* `serverless offline start`
* Interact with the app at `localhost:3000`

### AWS Deployment
* `serverless deploy --verbose`
* `export BASE_DOMAIN=<'endpoints' serverless deploy output result>`
* Get base url response:
  * `curl -H "Content-Type: application/json" -X GET ${BASE_DOMAIN}`
* Create a user:
  * `curl -H "Content-Type: application/json" -X POST ${BASE_DOMAIN}/users -d '{"userId": "alexdebrie1", "name": "Alex DeBrie"}'`
* Retrieve said user:
  * `curl -H "Content-Type: application/json" -X GET ${BASE_DOMAIN}/users/alexdebrie1`