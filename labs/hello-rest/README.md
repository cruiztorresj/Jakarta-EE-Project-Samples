# Jakarta EE  Hello Rest Services

## This app is composed of the following architecture:

* Maven Project - builds a WAR
* Using CDI scopes on Beans, @Named
* Statelss EJB for services - uses JPA entity beans - exposes appropriate method as REST API using JAX-RS annotations
* JAX-RS Application class
* JPA entity bean to store names - uses H2 in-memory database
* Use EJB Singleton to lookup messaging connection and queue destination and inject into stateless EJB - lookup should only occur once on startup
* Servlet that returns "OK" - this is a health check - path should be [context]/health
* H2 (embedded in-memory DB) backend

## Action
Make sure you have followed the steps in the README file for this repository about running each one of these applications. Since this is a rest service, you will see nothing if you visit the mentioned URL. You will interact with this project as follows:
- Run this project with `mvn wildfly:deploy`.
- Use your favorite REST client software to send requests to `http://localhost:8080/hello-rest/api/persons`. You can use Curl too.
- See existing persons.
  ```
  curl --request GET 'http://localhost:8080/hello-rest/api/persons' --header 'Content-Type: application/json'
   ```
- Create a Person.
  ```
  curl --request POST 'http://localhost:8080/hello-rest/api/persons' \
  --header 'Content-Type: application/json' --data '{"name": "AnyName"}'
  ```
- Delete a Person. Make sure you have created a person first. Where `N` is the person index to be deleted.
  ```
  curl --request DELETE 'http://localhost:8080/hello-rest/api/persons/N' --header 'Content-Type: application/json'
  ```
