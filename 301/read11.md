# read11: Authentication

## What is OAuth

**What is OAuth?**

**OAuth** is an open-standard authorization protocol or framework that describes how unrelated servers and services can safely allow authenticated access to their assets without actually sharing the initial, related, single logon credential. In authentication parlance, this is known as secure, third-party, user-agent, delegated authorization.

<br/>

**Give an example of what using OAuth would look like.**

For example, when creating a new account at **GitHub**, you have many options to how one want to create an account, and mostly people choose their same email address. This email address might also be used on **facebook**, **amazon** and many applications and services.

<br/>

**How does OAuth work? What are the steps that it takes to authenticate the user?**

- OAuth essentially allows the user, via an authentication provider that they have previously successfully authenticated with, to give another website/service a limited access authentication token for authorization to additional resources.
- **OAuth** only works using `HTTPS`
  <br/>
  if a user has already signed into one website or service and, then initiates a feature/transaction that needs to access another unrelated site or service. The following happens:

1. The first website connects to the second website on behalf of the user, using **OAuth**, providing the user’s verified identity.
2. The second site generates a one-time `token` and a one-time `secret` unique to the transaction and parties involved.
3. The first site gives this `token` and `secret` to the initiating user’s client software.
4. The client’s software presents the request `token` and `secret` to their authorization provider (which may or may not be the second site).
5. If not already authenticated to the authorization provider, the client may be asked to authenticate. After authentication, the client is asked to approve the authorization transaction to the second website.
6. The user approves (or their software silently approves) a particular transaction type at the first website.
7. The user is given an approved `access token` (notice it’s no longer a request token).
8. The user gives the approved `access token` to the first website.
9. The first website gives the `access token `to the second website as proof of authentication on behalf of the user.
10. The second website lets the first website access their site on behalf of the user.
11. The user sees a successfully completed transaction occurring.
12. **OAuth** is not the first authentication/authorization system to work this way on behalf of the end-user. In fact, many authentication systems, notably Kerberos, work similarly. What is special about **OAuth** is its ability to work across the web and its wide adoption. It succeeded with adoption rates where previous attempts failed (for various reasons).

<br/>

**What is OpenID?**

**OpenID** is another security technology, that work in the same category of **OAuth**, but in a different level. While auth in **OAuth** represent authorization not authentication, in **OpenID** it is about authentication.

as a commenter on `StackOverflow` _pithily_ put it: "OpenID is for humans logging into machines, OAuth is for machines logging into machines on behalf of humans."

In practice **OpenID** was difficult to implement on the developer side, and never really became that appealing to users, especially as there was competition in that space.

<br/>

</br>

## Authorization and Authentication flows

**What is the difference between authorization and authentication?**
**authentication** is the process of verifying who a user is, while **authorization** is the process of verifying what they have access to.
<br/>

**What is Authorization Code Flow?**
Authorization Code Flow is the exchange of an **Authorization** **Code** for a `token`.
<br/>

**What is Authorization Code Flow with Proof Key for Code Exchange (PKCE)?**
It is an additional security required by mobile and native applications during authentication. **OAuth** 2.0 provides a version of the Authorization Code Flow which makes use of a **Proof Key for Code Exchange (PKCE)**.  
<br/>

**What is Implicit Flow with Form Post?**
**Implicit Flow** is intended for Public Clients, or applications which are unable to securely store Client Secrets.

**Implicit Flow** is not considered a best practice for requesting `Access Tokens`, but when used with **Form Post response mode**, it does offer a streamlined workflow if the application needs only an `ID token` to perform user authentication.
<br/>

**What is Client Credentials Flow?**
It is used with machine-to-machine (M2M) applications, where **User-Name** and **Password** used for humans have no meanings.  
<br/>

**What is Device Authorization Flow?**
It is used with devices that have minimal inputs, or not easy to enter input with them like gaming controllers, the device asks the user to go to a link on their computer or smartphone and authorize the device.  
<br/>

**What is Resource Owner Password Flow?**
Though it is not recommended, highly-trusted applications can use the **Resource Owner Password Flow**, which requests that users provide credentials (username and password), typically using an interactive form. The **Resource Owner Password Flow** should only be used when **redirect-based flows** (like the Authorization Code Flow) cannot be used.

<br/><br/>

# References :

[What is OAuth](https://www.csoonline.com/article/3216404/what-is-oauth-how-the-open-authorization-framework-works.html) <br/>
[Authorization and Authentication flows](https://auth0.com/docs/flows) <br/>
