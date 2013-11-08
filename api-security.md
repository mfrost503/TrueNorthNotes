# Securing your REST API
# Chris Cornutt - @enygma

* Security is the difficulty with APIs
* Security is planned, don't just drop it in
* Security is easy to ignore, not just Auth*, everything
* Security is compromise, has to be balanced with usability
* Poor usability leads to users not using your software
* Availability/Scalability/Reliability
* Version the API

## Auth in detail
### HTTP Basic/Gigest
* Everything is sent in plaintext
* Use https
* Authorization: Basic username:password (in plaintext)
* base64_encoded - can be base64_decoded when not encrypted
* Digest provides same method, but includes nonce and opaque values
* Use SSL or don't use at all
* Even on internal networks, if someone gets inside you are vulnerable

### Shared Tokens
* Information that your user has that you provide them
* Difficult to maintain, service provided has to provide/use/track them
* Static, used as part of the request
* Not encryption

### OAuth v2
* Handshake - redirect user to service, redirect back to your application
* Service provider is responsible for keeping your credentials safe
* Burden of identity
* Complex to implement a server
* It's not about Authorization, it's about Authentication
* Authentication proves who the person is first
* Authorization ensures they have access to a specific resource
* Delegation, user is "allowed to do this action"

### Shared Certificates
* Stronger protection than passwords
* Stronger when randomly generated
* More randomization allows for easier use of encryption
* No private information involved if randomly generated - hard to reproduce
* Doesn't convey information about the user, just a form of identification between client and server
* Difficult to deploy

## Not Just Auth
### Rate Limiting
* Rate Limiting - restricting amount of requests able to be made in a timeframe
* No rate limit leaves yourself open to DDoS attacks
* Limit types of requests, GETs are different that PUT/POST
* All about time
### Throttling
* Limiting the size of the request
* Could send thousands of records in one request
* Slow them down
* Limiting bandwidth usage

### Filtering/Escaping
* If APIs are the primary source, you have to escape differently (JSON Injection, XML injection)
* Don't assume the user is going to provide you with right information
* Validate the information that is coming
* Proxy allows you to modify request before it's sent in
* Attackers will most likely not use your javascript front-end to attack
* Open text fields are harder to validate and filter

### Direct Object References
* On OWASP Top 10
* A3: Direct Object References
* Guessable common urls are bad
* ID integers are easily guessable use GUIDs or hashed values that are hard to guess/reproduce
* Provide information on how quickly your service is growing

### Error Conditions
* Don't provide any information that the users don't need
* Providing file system information give an attack more information about your application (structure, etc)

## Good Practices
* Use HTTPS (always)
* Are cases where it's been broken, but it requires other attacks (man in the middle)
* A little extra overhead, but worth it
* Prevent leakage
* Access control is a consideration when providing information back to user
* Be stateless (HTTP is stateless), don't have a session on the user side
* Validate token on each request in OAuth
* Refresh request can provide a new token
* Auth on a resource, not URI - think of data you are protecting not the URI
* Importance of HTTP status
* Use generated keys and not passwords
* Provide an alternative that has been generated for them
* 2-Factor Authentication
* Signing with hashes (public/private key)
* Public key is sent with request
* Private hash allows user to create signature
* Prevents man in the middle attack
* Allows you to protect against man in the middle attacks as long as private key stays private
* Method permissioning - higher restrictions on important actions
* Secure Input Parsing - parse the input correctly, to prevent malicious data
* PHP XML parsing can take your system down if you don't check it
* Can turn it off, but it makes it difficult

## Think Simple
* Keep it simple
* Think about your needs
* Think about how you want to protect your data
