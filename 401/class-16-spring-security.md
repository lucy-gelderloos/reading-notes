# Class 16 - Spring Security

## [Spring Security Architecture](https://spring.io/guides/topicals/spring-security-architecture/)

### Authentication

Main interface is `AuthenticationManager`, which has one method (`authenticate()`). This method returns true if the input is valid, an exception if the input is not valid, or `null` if it can't determine. Groups of related resources may each have their own Authentication Manager.

An `AuthenticationProvider` is similar to the Authentication Manager, but it can also specify which type of authentication it supports. A `ProviderManager` can manage a chain of Authentication Providers to handle multiple types of authentication. Provider Managers can reference a parent if their authentication returns null, or return null if there is no parent to consult.

Spring Security provides some tools, including `AuthenticationManagerBuilder`, to help speed up setup.

### Authorization

The `AccessDecisionManager` delegates to chains of `AccessDecisionVoter` instances, which looks at an `Authentication` and an `Object` that has been configured with `ConfigAttributes`. In most setups, access will be granted if one of the Access Decision Voters returns yes.

### Web Security

Spring web security is based on Servlet filters. Filters can decide to handle requests themselves, or can modify a request or response as it passes through. This ensures the request gets to the right servlet in the right configuration. Filters can be ordered either in their own configuration or in a controller. Spring Security is a filter (with more internal filters).

Filter chains can be customized depending on which resources are being secured. Access to a front-end UI might be handled differently than access to an API.

### Method Security

Spring Security can be configured to limit access to a specified Java method.

### Getting user info in Spring Security

```java
@RequestMapping("/foo")
public String foo(Principal principal) {
  Authentication authentication = (Authentication) principal;
  User = (User) authentication.getPrincipal();
  ... // do stuff with user
}
```

## [Spring Security Cheat Sheet](https://github.com/codefellows/seattle-java-401d2/blob/master/SpringAuthCheatSheet.md)

Reference this cheat sheet when setting up a project with Spring Security.

## Things I want to know more about

How to arrange sites most efficiently for security.
