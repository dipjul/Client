# Client

### MySql database is used
### Spring Oauth 2.0 is used for security

## REST APIs

#### GET `/clients`
#### GET `/clients/{id}`
#### POST `/clients`
#### PUT `/clients/{id}`
#### DELETE `/clients/{id}`

## For changing database:
- Change the dependencies on pom.xml file
- Change the details on src/main/resources/application.properties

## Running for the first time:
- Uncomment the below code on DataInitializer.java
```java
        this.users.save(User.builder()
            .username("user")
            .password(this.passwordEncoder.encode("password"))
            .roles(Arrays.asList( "ROLE_USER"))
            .build()
        );

        this.users.save(User.builder()
            .username("admin")
            .password(this.passwordEncoder.encode("password"))
            .roles(Arrays.asList("ROLE_USER", "ROLE_ADMIN"))
            .build()
        );
```
