# DotNetCoreWebAPI 

This is a dotnetcore WebAPI sample with CRUD operations under REST verbs of HTTP.
Added the auth0 security scheme, allowing edit, post and delete only with a presence of a token in call.

## Installation

TBD.


## Usage
Go to Postman or Insomnia or even by a CLI interface and hit:
```bash
curl --insecure https://localhost:5001/api/glossary

curl --insecure https://localhost:5001/api/glossary/jwt

curl --insecure \
  --verbose \
  --request POST \
  --url https://localhost:5001/api/glossary \
  --header 'content-type: application/json' \
  --header 'authorization: Bearer YOUR_TOKEN' \
  --data '{ "term": "MFA", "definition": "An authentication process that considers multiple factors."}'

curl --insecure \
  --request PUT \
  --url https://localhost:5001/api/glossary \
  --header 'content-type: application/json' \
  --header 'authorization: Bearer YOUR_TOKEN' \
  --data '{ "term": "JWT", "definition": "An open, industry standard RFC 7519 method for representing claims securely between two parties. Auth0 uses JWT format for ID Tokens."}'

curl --insecure \
  --request DELETE \
  --url https://localhost:5001/api/glossary/openid
  --header 'authorization: Bearer YOUR_TOKEN' \
```


## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/)