# Read: 16 - Spring Authentication

## Spring Security Architecture

Application security boils down to two more or less independent problems: authentication (who are you?) and authorization (what are you allowed to do?).

### Authentication
The main strategy interface for authentication is AuthenticationManager, which has only one method:

```
public interface AuthenticationManager {

  Authentication authenticate(Authentication authentication)
    throws AuthenticationException;
}
```

the authenticate() method above can do 3 things:
1. Return an Authentication (normally with authenticated=true) if it can verify that the input represents a valid principal.
2. Throw an AuthenticationException if it believes that the input represents an invalid principal.
3. Return null if it cannot decide.

### Authorization 
After authentication successful, we can move on to authorization, and the core strategy here is AccessDecisionManager. 

An AccessDecisionVoter considers an Authentication (representing a principal) and a secure Object, which has been decorated with ConfigAttributes:

```
boolean supports(ConfigAttribute attribute);

boolean supports(Class<?> clazz);

int vote(Authentication authentication, S object,
        Collection<ConfigAttribute> attributes);
```

### Web Security
- Spring Security in the web tier (for UIs and HTTP back ends) is based on Servlet Filters .

- The client sends a request to the application, and the container decides which filters and which servlet apply to it based on the path of the request URI.

- Spring Security is installed as a single Filter in the chain, and its concrete type is FilterChainProxy.

- the security filter is a @Bean in the ApplicationContext, and it is installed by default so that it is applied to every request.

- There can be multiple filter chains all managed by Spring Security in the same top level FilterChainProxy and all are unknown to the container.

![web-security](https://lh3.googleusercontent.com/proxy/MnWVPeu3N8GhZNR6MwxaDjAJXKdE-ubwx-QXKGMDF-cd-rzKziDfFcnBAhJvr4y-a1EtMRPC0kNlGUiVCiddcU7Daj1cvs0sy5hPxUIB1Vd7Iw)


**cheat sheet for spring auth:**
[spring auth cheat sheet](https://github.com/codefellows/seattle-java-401d2/blob/master/SpringAuthCheatSheet.md)


