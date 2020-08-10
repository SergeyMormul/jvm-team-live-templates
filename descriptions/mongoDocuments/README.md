# Mongo Documents
Describes live templates which are good to use in creating data classes which describes MongoDB collections.

Very specific templates, may be not useful in general, bu still goo for creating a data class to represent MongoDB collection.

> Wrapped - marked as that are wrapped examples to keep proper readability of the whole table.

`|` shows the final place of the cursor.

<table>
  <tr>
    <th>Template</th><th>Description and Enter points</th><th>Example of the result</th>
  </tr>
  <tr>
    <td><code>doce</code></td>
    <td>Creates three standard annotations for MongoDB document class.</td>
    <td>
      <pre lang='Groovy'>
@Document
@Canonical
@EqualsAndHashCode( excludes = [|] )</pre>
    </td>
  </tr>
  <tr>
    <td><code>ciopt</code></td>
    <td>Creates an optimistic concurrency compound index annotation.</td>
    <td>
      Wrapped: the result will be in a line.
      <pre lang='Groovy'>
@CompoundIndex( name = 'optimistic_concurrency_idx', 
                def = "{ '_id': 1, 'version': 1 }" )
    </td>
  </tr>
  <tr>
    <td><code>ci</code></td>
    <td>Creates a compound index annotation.<br/>
      Enter points:<br/>
      <ol>
        <li>Index name</li>
        <li>First indexed field name</li>
        <li>Second indexed field name</li>
      </ol>
    </td>
    <td>
      Wrapped: the result will be in a line.
      <pre lang='Groovy'>
@CompoundIndex( name = 'index_name', 
                def = "{ 'first-field': 1, 'second-field': 1| }", 
                unique = true )</pre>
    </td>
  </tr>
  <tr>
    <td><code>fnames</code></td>
    <td>Creates a nested immutable class to describe document field names.</td>
    <td>
      <pre lang='Groovy'>
/**
 * Contains mongo field name constants, which are publicly accessible.
 */
@Immutable
static final class FieldNames {
    public static final String MIME_TYPE = 'mime-type'
    public static final String ID = '_id'
    public static final String VERSION = 'version'
    |
}</pre>
    </td>
  </tr>
  <tr>
      <td><code>name</code></td>
      <td>Creates a field name variable.<br/>
      Creates an underlined capitalized name of the variable based on the value.<br/>
        Enter points:<br/>
        <ol>
          <li>Value of the field name variable</li>
        </ol>
      </td>
      <td>
        <pre lang='Groovy'>
public static final String FIELD_NAME = 'field-name'
|</pre>
      </td>
  </tr>
  <tr>
    <td><code>ids</code></td>
    <td>Creates a document id field of type <code>String</code>. Adds an extra empty line below.</td>
    <td>
      <pre lang='Groovy'>
/**
 * Mongo generated id of the document.
 */
@Id
@Field( FieldNames.ID )
String id
<br/>
|</pre>
    </td>
  </tr>
  <tr>
    <td><code>idu</code></td>
    <td>Creates a document id field of type <code>UUID</code>. Adds an extra empty line below.</td>
    <td>
      <pre lang='Groovy'>
/**
 * Mongo generated id of the document.
 */
@Id
@Field( FieldNames.ID )
UUID id
<br/>
|</pre>
    </td>
  </tr>
  <tr>
    <td><code>ver</code></td>
    <td>Creates a document version field declaration. Adds an extra empty line below.</td>
    <td>
      <pre lang='Groovy'>
/**
 * A version field used to implement optimistic locking on entities.
 */
@Version
@Field( FieldNames.VERSION )
Long version
<br/>
|</pre>
    </td>
  </tr>
  <tr>
    <td><code>df</code></td>
    <td>Creates a general document field. Suggests a field type. Adds an extra empty line below.<br/>
      Enter points:<br/>
      <ol>
        <li>Type</li>
        <li>Name of the field</li>
        <li>Value for <code>@Field</code></li>
        <li>Groovydoc comment</li>
      </ol>
    </td>
    <td>
      <pre lang='Groovy'>
/**
 * Groovydoc comment.
 */
@Field( FieldNames.VALUE )
Type filedName
<br/>
|</pre>
    </td>
  </tr>
  <tr>
    <td><code>dfs</code></td>
    <td>Creates a <code>String</code> document field. Adds an extra empty line below.<br/>
      Enter points:<br/>
      <ol>
        <li>Name of the field</li>
        <li>Value for <code>@Field</code></li>
        <li>Groovydoc comment</li>
      </ol>
    </td>
    <td>
      <pre lang='Groovy'>
/**
 * Groovydoc comment.
 */
@Field( FieldNames.VALUE )
String fieldName
<br/>
|</pre>
    </td>
  </tr>
  <tr>
    <td><code>dfl</code></td>
    <td>Creates a <code>long</code> document field. Adds an extra empty line below.<br/>
      Enter points:<br/>
      <ol>
        <li>Name of the field</li>
        <li>Value for <code>@Field</code></li>
        <li>Groovydoc comment</li>
      </ol>
    </td>
    <td>
      <pre lang='Groovy'>
/**
 * Groovydoc comment.
 */
@Field( FieldNames.VALUE )
long fieldName
<br/>
|</pre>
    </td>
  </tr>
</table>

## Surroundings
Describes the surround live templates for mongo documents. Surround live templates can be invoked by short cut `Ctr+Alt+J`.

`|` shows the place of the cursor.

### Compound indexes
`CIS`

To surround the annotation `@CompoundIndex` by the annotation `@CompoundIndexes`, put a cursor at the line of the former and press `Ctr+Alt+J` and choose `CIS` template. 
Then you can use `ci` live template to add another `@CompoundIndex`. 

**Before**
```groovy
@CompoundIndex( name = 'index_name', def = "{ 'first-field': 1, 'second-field': 1 }", unique = true )|
```
**After**
```groovy
@CompoundIndexes( [@CompoundIndex( name = 'index_name', def = "{ 'first-field': 1, 'second-field': 1 }", unique = true ),
        |] )
```