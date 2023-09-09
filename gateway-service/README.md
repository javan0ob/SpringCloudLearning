# gateway learning
***
## intruction
Spring Cloud Gateway aims to provide a simple, yet effective way 
to route to APIs and provide cross cutting concerns to them 
such as: security, monitoring/metrics, and resiliency.

## glossary
* Route
* Predicate
* Filter

## config yml
```yaml
#shortcut configuration
spring:
  cloud:
    gateway:
      routes:
        - id: cookie_route
          uri: https://example.org
          predicates:
            - Cookie=mycookie,mycookievalue
```
```yaml
#fully expanded arguments
spring:
  cloud:
    gateway:
      routes:
      - id: cookie_route
        uri: https://example.org
        predicates:
        - name: Cookie
          args:
            name: mycookie
            regexp: mycookievalue
```

## Route Predicate Factories
* After Route
* Before Route
* Between Route
* Cookie Route
* Header Route
* Host Route
* Method Route
* Path Route
* Query Route
* RemoteAddr Route
* Weight Route
* XForwardedRemoteAddr Route

## Filter Factories
* AddRequestHeader GatewayFilter


