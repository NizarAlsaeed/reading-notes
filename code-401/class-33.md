# Introduction to JSON Web Tokens
JSON Web Token (JWT) is an open standard (RFC 7519) that defines a 
compact and self-contained way for securely transmitting information between parties as a JSON object.

### Here are some scenarios where JSON Web Tokens are useful:
- Authorization: Once the user is logged in, each subsequent request will include the JWT, allowing the user
to access routes, services, and resources that are permitted with that token. 
- Information Exchange: Because JWTs can be signed—for example, using public/private key 
pairs—you can be sure the senders are who they say they are.

 a JWT typically looks like the following.
`xxxxx.yyyyy.zzzzz`

### How do JSON Web Tokens work
In authentication, when the user successfully logs in using their credentials, a JSON Web Token will be returned.
Whenever the user wants to access a protected route or resource, the user agent should send the JWT.


1. The application or client requests authorization to the authorization server. This is performed through one of the different authorization flows. For example, a typical OpenID Connect compliant web application will go through the /oauth/authorize endpoint using the authorization code flow.
2. When the authorization is granted, the authorization server returns an access token to the application.
3. The application uses the access token to access a protected resource (like an API).

### How to Use JWT Authentication with Django REST Framework
Those are three distinctive parts that compose a JWT:

`header.payload.signature`
```
header

{
  "typ": "JWT",
  "alg": "HS256"
}
```
```
payload

{
  "token_type": "access",
  "exp": 1543828431,
  "jti": "7f5997b7150d46579dc2b49167097e7b",
  "user_id": 1
}
```
```
signature

The signature is issued by the JWT backend, using the header base64 + payload base64 + SECRET_KEY. Upon each request this signature is verified.
```
