# e-conomic-soap-api

* Java 11 compatible
* Just clone
* Do: mvn install


Then add following dependency to your project:
```xml
<dependency>
    <groupId>soj.nobelium</groupId>
    <artifactId>e-conomic</artifactId>
    <version>1.0</version>
</dependency>
```

With this Java code you can interact with the api:
```java
var service = new EconomicWebService();

var session = service.getEconomicWebServiceSoap12();

((BindingProvider) session).getRequestContext().put(BindingProvider.SESSION_MAINTAIN_PROPERTY, true);

// You need to create the tokens in e-conomic administration console 
session.connectWithToken("tokel1", "token2");

// Do your interaction on the session object

// Disconnect the session after use
session.disconnect();

```
