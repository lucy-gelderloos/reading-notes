# Class 12 - Accessing Data; Comparing Repositories

## [Accessing Data with JPA](https://spring.io/guides/gs/accessing-data-jpa/)

Spring Data JPA (*Java Persistence API*) allows us to persist data in a Java application by storing data in a query-able relational database. Some key points:

- Data is stored as a JPA entity, annotated as `@Entity`
- If you want to map the data to a specific table, use `@Table`; otherwise, the class will be mapped to a table of the same name
- To generate a unique ID, annotate as `@Id` and `@Generated`
- Un-annotated properties are mapped to columns of the same name
- Data is stored in a repository interface, which extends (and inherits methods from) `CrudRepository`
- Spring JPA automatically creates an instance of the repository when it runs
- You'll need a class to access and modify the data

## [CrudRepository, JpaRepository, and PagingAndSortingRepository in Spring Data](https://www.baeldung.com/spring-data-repositories)

Every Spring data repository extends `Repository`, but with slightly different features and functionality.

### `CrudRepository` (extends `Repository`)

Provides all basic query functions:

- save
- findOne
- findAll
- count
- delete
- exists

### `PagingAndSortingRepository` (extends `CrudRepository`)

Allows data to be paginated and sorted. Paginated objects need at least a page size (how many results to show per page), a current page number, and a way to sort the results.

### `JPARepository` (extends `PagingAndSortingRepository`)

Provides more ways of working with data, including:

- findAll (can optionally sort on provided condition)
- save
- flush
- saveAndFlush
- deleteInBatch

## Things I'd like to know more about

How persistent is data stored this way? Where is it stored?
