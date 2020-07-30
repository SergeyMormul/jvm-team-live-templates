# Mongo Documents
Describes live templates which are good to use in creating data classes which describes MongoDB collections.

Very specific templates, may be not useful in general, bu still goo for creating a data class to represent MongoDB collection.
> Currently autoimport of an annotation is not supported.

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
      <pre lang='Groovy'>
@CompoundIndex( name = 'user_date', 
                def = "{ 'externaUserId': 1, 'dateCode': 1| }", 
                unique = true )</pre>
    </td>
  </tr>
  <tr>
    <td><code>F</code></td>
    <td>Creates a nested imutable class to describe document field names.</td>
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
    <td><code>tltype</code></td>
    <td>Creates a standard tl-type field declaration. Adds an extra empty line below.<br/>
      Enter points:<br/>
      <ol>
        <li>TL type atribute value</li>
      </ol>
    </td>
    <td>
      <pre lang='Groovy'>
/**
 * Indicates the schema that this structure 
 * adheres to using the standard mime-type notation.
 * Typically left to its default value.
 */
@SuppressWarnings( 'GroovyUnusedDeclaration' )
@Field( FieldNames.MIME_TYPE )
final String mimeType = 'application/bson;tl-type=user-document;version=1.0.0'
<br/>
|</pre>
    </td>
  </tr>
  <tr>
    <td><code>df</code></td>
    <td>Creates a general document field. Suggests field type. Adds an extra empty line below.<br/>
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
 * Represents the date the document is related to.
 */
@Field( FieldNames.TYPE )
Type typeField
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
 * Represents the langguage the document is related to.
 */
@Field( FieldNames.LANGUAGE )
String language
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
 * Represents the date the document is related to in milliseconds since Epoch.
 */
@Field( FieldNames.DATE_CODE )
long dateCode
<br/>
|</pre>
    </td>
  </tr>
</table>
