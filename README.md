# Authenticator with JWT

How to use
The authenticator application makes use of generating beans. In order to speed up delivery, I have opted to keep bean creation in the application itself as opposed to having each application generate its own beans.

1. Import the library into your Java project
2. In the starter application class with your main method, add the following:
   - @EntityScan(basePackages = {"com.reinhardt.security.domain"})
   - @EnableJpaRepositories(basePackages = "com.reinhardt.security.repository")
   - @ComponentScan(basePackages = {
        "com.reinhardt.restaurant.ordercreator"...
3. The authenticator app makes use of a secret that needs to be brought in as a system property. I am introducing this JVM variable when starting my consuming application with this argument
    - -Djwt.hashing.secret= Enter your secret
