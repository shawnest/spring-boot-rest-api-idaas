# Spring Boot REST API w IDaaS provider

Sample library implementing a Spring Boot based REST API protected by JWT tokens issued by an IDaaS provider. The repository is tested with [Auth0](https://auth0.com/), but any other major IDaaS provider should be integrable with minor changes.

## Installation
**1. Clone the application**

```bash
git clone https://github.com/shawnest/spring-boot-rest-api-idaas.git
```

**2. Register at one of the IDaaS providers. For example [Auth0](https://auth0.com/).**

**3. Create a client and the API application at the provider. For example [Auth0 tutorial](https://auth0.com/docs/quickstart/backend/java-spring-security5/01-authorization)**

**4. Change the audience and issuer-uri in the application.properties file according to the values provided by the IDaaS provider**

```yml
spring.security.oauth2.resourceserver.jwt.audience=<YOUR-AUDIENCE>
spring.security.oauth2.resourceserver.jwt.issuer-uri=<YOUR-ISSUER-URI>
```

**5. Run the application**

```cmd
./gradlew bootRun
```

## Usage

You can integrate the REST API with any type of client that can authenticate using the corresponding identity provider.

For example you can use Postman to test the API. For further details please check [Auth0 community question about getting access token in Postman](https://community.auth0.com/t/getting-user-auth-token-in-postman/66413).


## Contributing

Pull requests are welcome. For major changes, please open an issue first
to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License

[Apache 2.0](https://choosealicense.com/licenses/apache-2.0/)