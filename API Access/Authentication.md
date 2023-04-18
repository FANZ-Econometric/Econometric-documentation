## Econometric.Api Authentication

- For an in depth discussion on the authentication used refer to the Pure Farming documentation: https://developer.purefarming.com/authentication/
- It is assumed that the developer has knowledge of calling web apis, any reference to code will assume a knowledge of ASP.NET Web Api.
- An Access Key needs to be acquired and passed as a Bearer token with an API request
- To obtain an Access Key you would use the Pure Farming sign in url e.g. https://signin{environment}/auth/realms/moa/protocol/openid-connect/token
where {environment} is environment to sign in to
- The credentials (Client Id, Client Secret) would need to be passed as a AuthenticationHeaderValue

