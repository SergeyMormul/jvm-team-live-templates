# JSON Groovy Fields
Describes live templates which are good for creating `@JsonProperty` annotated fields.

Edit point is a point where a developer has to enter something: type, name, comment, etc. Each point is invoked in order as described below for each specific template.

> Currently autoimport of an annotation is not supported.

`|` shows the final place of the cursor.

<table>
  <tr>
    <th>Template</th><th>Description and Enter points</th><th>Example of the result</th>
  </tr>
  <tr>
    <td><code>jf</code></td>
    <td>Creates a general JSON property declaration. Suggests a field type. Adds an extra empty line below.<br/>
      Enter points:<br/>
      <ol>
        <li>Type</li>
        <li>Name</li>
        <li>Annotation value</li>
        <li>Groovydoc comment</li>
      </ol>
    </td>
    <td>
      <pre lang='Groovy'>
/**
 * Groovydoc about field.
 */
@JsonProperty( 'annotation-value' )
Type fieldName
<br/>
|</pre>
    </td>
  </tr>
  <tr>
      <td><code>jfl</code></td>
      <td>Creates a <code>List</code> JSON property declaration. Suggests a generic type. Adds an extra empty line below.<br/>
        Enter points:<br/>
        <ol>
          <li>Generic Type</li>
          <li>Name</li>
          <li>Annotation value</li>
          <li>Groovydoc comment</li>
        </ol>
      </td>
      <td>
        <pre lang='Groovy'>
 /**
  * Groovydoc about field.
  */
 @JsonProperty( 'annotation-value' )
 List<GenericType> fieldName
 <br/>
 |</pre>
      </td>
    </tr>
  <tr>
    <td><code>jfs</code></td>
    <td>Creates a <code>String</code> JSON property declaration. Adds an extra empty line below.<br/>
      Enter points:<br/>
      <ol>
        <li>Name</li>
        <li>Annotation value</li>
        <li>Groovydoc comment</li>
      </ol>
    </td>
    <td>
    <pre lang='Groovy'>
/**
 * Groovydoc about field.
 */
@JsonProperty( 'annotation-value' )
String fieldName
<br/>
|</pre>
    </td>
  </tr>
  <tr>
    <td><code>jfu</code></td>
    <td>Creates a <code>UUID</code> JSON property declaration. Adds an extra empty line below.<br/>
      Enter points:<br/>
      <ol>
        <li>Name</li>
        <li>Annotation value</li>
        <li>Groovydoc comment</li>
      </ol>
    </td>
    <td>
    <pre lang='Groovy'>
/**
 * Groovydoc about field.
 */
@JsonProperty( 'annotation-value' )
UUID fieldName
<br/>
|</pre>
    </td>
  </tr>
</table>
