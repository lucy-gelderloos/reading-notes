# Class 13 - More Spring

## [One-to-many Relationships](https://www.baeldung.com/spring-data-rest-relationships)

- Defined using `@OneToMany` or `@ManyToOne`
- In this example, many books to one library
  - books are annotated with `@ManyToOne` and `@JoinColumn`, which sets a column to join the tables on (in this case, library_id)
  - library is annotated with `@OneToMany`, which sets the "mappedBy" property
  - books have their own repository
  - books are created, then assigned to the library, and can be accessed using GET on the library

## [Spring Integration Testing](https://www.baeldung.com/integration-testing-in-spring)

- Dependencies required: junit-jupiter-engine, junit-jupiter-api, sprint-test, hamcrest-library, json-path
- On the test classes, include `@ExtendWith(SpringExtension.class)`, `@ContextConfiguration(classes = ApplicationConfig.class)`, and `@WebAppConfiguration`
- Also include `@Autowired` WebApplicationContext
- The MockMvc object makes all web application beans available for testing

Tests can:

- verify that visiting the provided route returns a specified view
- verify that visiting the provided route returns specified data
- verify that a route can handle GET requests with either path variables or query parameters
- verify that a route can handle POST requests correctly

MockMvc has some limitations - it doesn't test the whole network stack, and has a hard time handling HTTP redirects.

## Things I'd like to know more about

Is it recommended to test existing applications this way once they're running?
