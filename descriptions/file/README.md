# File
Describes additional file templates.

Follow the standard file or class creation procedure to use a template, such as: `Right Click -> New` on a package; `Alt+Insert` on a package; `Ctrl+Alt+Insert` in the editor.

Depending on the template one or a few new files will be created in the current package. 

There are the following templates added so far to create a file or s few files at once:
* [Mongo Repository](#mongo-repository) 
* [Mongo Repository with Extension](#mongo-repository-with-extension)

## Mongo Repository
Crates a single interface of mongo repository. The specific database collection name should be entered in the creation modal.
The result will look like the following:
```groovy
package com.transparent.package

import org.springframework.data.mongodb.repository.MongoRepository

/**
 * Talks to {@link CollectionName} collection in MongoDB.
 */
interface CollectionNameRepository extends MongoRepository<CollectionName, String> {


}
```

## Mongo Repository with Extension
Similar to [Mongo Repository](#mongo-repository) creates three classes for the repository:
* interface CollectionNameRepository
* interface CollectionNameRepositoryExtension
* class CollectionNameRepositoryImpl

The classes will be formatted properly with necessary relations between each other.

