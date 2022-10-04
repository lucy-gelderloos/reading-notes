# Amazon Simple Storage Service

## [S3 User Guide](https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html)

S3 is a storage service that allows users to store, manage, and archive data. Data can be stored in different classes depending on how quickly and/or frequently it needs to be accessed or changed. You can control who can access your data, and make sure it is maintained as necessary for regulatory and compliance requirements. Data processing workflows can be automated. Storage can be logged an monitored automatically or manually.

S3 stores data as objects in buckets. An S3 account allows for up to 100 buckets, each with unlimited objects. Objects have data and metadata; the metadata is made up of key-value pairs. Each object also has a unique key. You can also use versioning to store multiple versions of an object in a bucket. Access policies can be set at the bucket level. S3 provides strong data consistency and tools for managing multiple clients writing to the same items.

## [S3 and Amplify](https://docs.amplify.aws/lib/storage/getting-started/q/platform/android/)

Instructions on adding S3 storage to an Amplify app. First add and configure storage through the CLI, then push to the cloud. Add the appropriate dependencies to the build.gradle and the initialization code to your app, then add upload methods to upload data to S3.

## Things I'd like to know more about

How this will interact with the GraphQL service we're already using.
