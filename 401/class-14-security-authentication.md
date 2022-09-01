# Class 14 - Security & Authentication

## [Hashing Passwords: One-Way Road to Security](https://auth0.com/blog/hashing-passwords-one-way-road-to-security/)

Passwords must be stored securely to protect your site and its users. Password hashing refers to converting passwords into data that can't be converted back into the original password (unlike encryption, which allows data to be converted back).

A hash function maps data onto a fixed-size bit string. When a hash function is described as pre-image resistant, that means it is infeasible to find an input that matches the given hashed output (so hackers can't reverse-engineer the input). Hash functions must also be deterministic, meaning they must always produce the same output given the same input, and they should be slow, to make brute-force attacks inefficient.

Salting a password hash means including a unique random value with each hashed password. This means that, even if two users have identical passwords, the hashed value won't be the same. (Hashed values could also hypothetically be the same even if the inputs are different, because hash values are of a fixed length.)

When a user logs in, the password they provide is run through the hash function; the result is compared with the hashed password in the database, and the actual password is never exposed.

## [Why you should use BCrypt to hash passwords](https://danboterhoven.medium.com/why-you-should-use-bcrypt-to-hash-passwords-af330100b861)

BCrypt is a password-hashing function that both salts hashes and increases its running time over time to help ensure brute-force attacks stay inefficient.

## [jBCrypt](https://www.mindrot.org/projects/jBCrypt/)

A java implementation of BCrypt. 

Implementation code:

```java
// Hash a password for the first time
String hashed = BCrypt.hashpw(password, BCrypt.gensalt());

// gensalt's log_rounds parameter determines the complexity
// the work factor is 2**log_rounds, and the default is 10
String hashed = BCrypt.hashpw(password, BCrypt.gensalt(12));

// Check that an unencrypted password matches one that has
// previously been hashed
if (BCrypt.checkpw(candidate, hashed))
  System.out.println("It matches");
else
  System.out.println("It does not match");
```

## Things I want to know more about

What else needs to be done to keep passwords secure.
