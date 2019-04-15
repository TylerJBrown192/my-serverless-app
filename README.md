# My Serverless App

Startup: 
* `npm i`
* Configure `serverless` AWS credentials https://serverless.com/framework/docs/providers/aws/guide/credentials/
* `serverless deploy --verbose`
* `export BASE_DOMAIN=<'endpoints' serverless deploy output result>`
* Get base url response:
  * `curl -H "Content-Type: application/json" -X GET ${BASE_DOMAIN}`
* Create a user:
  * `curl -H "Content-Type: application/json" -X POST ${BASE_DOMAIN}/users -d '{"userId": "alexdebrie1", "name": "Alex DeBrie"}'`
* Retrieve said user:
  * `curl -H "Content-Type: application/json" -X GET ${BASE_DOMAIN}/users/alexdebrie1`