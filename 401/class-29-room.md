# Class 29 - Persisting Data with Room

## [Saving data with Room](https://developer.android.com/training/data-storage/room)

Room provides a way to persist data locally using SQLite, with annotation and streamlined paths that make it easier to work with SQLite APIs.

Required dependencies in build.gradle (see page for optional dependencies):

```.ignoreLang
dependencies {
    def room_version = "2.4.3"

    implementation "androidx.room:room-runtime:$room_version"
    annotationProcessor "androidx.room:room-compiler:$room_version"
```

There are three main components to a Room database:

- Database class, which provides instances of the DAOs associated with that database
- Data access objects(DAOs), which provide methods the app can use to access the database
- Data entities, which represent tables in the database

[Sample implementation](https://developer.android.com/training/data-storage/room#sample-implementation)

## [Defining data with Room entities](https://developer.android.com/training/data-storage/room/defining-data)

Each entity corresponds to a table in a Room database, and each instance of the entity represents a row of data. A Room entity is a class annotated by `@Entity`, where each field is a column in the table. By default, the table name is the same as the class name. Each entity must have a primary key, which can be its own column or a composite of multiple columns. More recent SDK versions support full-text searching of Room databases; earlier versions can be made more searchable by implementing indices.

## [Define relationships between objects](https://developer.android.com/training/data-storage/room/relationships)

Room does not allow entities to reference each other. Instead, use either an intermediate data class to hold the pairings between instances of two entities, or a multimap approach. Choose the method that works best for your app; the documentation recommends using multimap because the code is less complex (the complexity comes in on the SQL side).

Embedded objects (annotated with `@Embedded`) allow you to save an object with multiple fields as a single entry (like an address with street, city, etc.).

- *One-to-one* relationships are created by setting a variable in one of the classes (the child class) to reference the primary key of the parent class. Next, create a data class that includes the `@Relation` annotation to define which columns correspond.
- *One-to-many* relatinoships are also created by adding a variable in the child class to reference the parent class' id. Then create a relational class that holds a list of all child entities related to a parent entity.
- *Many-to-many* relationships are associated by creating a third "associative entity" with a column for each entity's primary key. Queries can be set to return a list of all items from entity A related to entity B, or vice versa.

Relationships can also be nested (example: searching for a song within a playlist within a user's account).

## [Accessing data using Room DAOs](https://developer.android.com/training/data-storage/room/accessing-data)

A DAO must be either an interface or an abstract class; it doesn't have properties, but defines methods for interacting with the database. There are some basic methods, and you can write your own with SQL queries.

### Convenience methods

- `@Insert`
- `@Update`
- `@Delete`

You can also write custom queries, for actions like finding all items or displaying only some columns of information. These queries can also take in parameters:

```java
@Query("SELECT * FROM user WHERE age > :minAge")
public User[] loadAllUsersOlderThan(int minAge);
```

Join clauses can be used to query multiple tables:

```java
@Query("SELECT * FROM book " +
       "INNER JOIN loan ON loan.book_id = book.id " +
       "INNER JOIN user ON user.id = loan.user_id " +
       "WHERE user.name LIKE :userName")
public List<Book> findBooksBorrowedByNameSync(String userName);
```

## Things I'd like to know more about

How to use more complex SQL queries to access and modify data.
