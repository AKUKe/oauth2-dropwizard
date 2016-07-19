# OAuth2-DropWizard

OAuth2-DropWizard is a dropwizard 0.9.x implementation of an OAuth2 secured RESTful server.

It provides the /oauth20 endpoint to manage oauth authentication. Authentication token is stored in an encrypted cookie on the client. This provides automatic authentication propagation on subsequent accesses to protected resources by just using the generated client cookie.

Using this cookie, a client browser (or any web/mobile app), which is by nature insecure, can then securely handle it's user's credentials and access a stateless server like DropWizard in a secure manner (no credentials stored in the sources or handled by javascript).

### Version
1.0

### Run

Build with maven then copy src/main/resources/config.template.yml to config.yml and change values according to your configuration. 
You can then run the server with the command :

```
java -jar oauth2-dropwizard-x.y.jar server config.yml
```
 
### Tech

OAuth2-DropWizard uses a number of open source projects to work properly:

* [DropWizard] - Dropwizard is a Java framework for developing ops-friendly, high-performance, RESTful web services
* [edeoliveira/APIFest OAuth2 server] - A server that implements an OAuth 2.0 server as per http://tools.ietf.org/html/rfc6749 (extensively modified fork)

[DropWizard]:http://www.dropwizard.io/
[edeoliveira/APIFest OAuth2 server]:https://github.com/edeoliveira/apifest-oauth20
