# JSON Groovy Fields
Describes live templates which are good for creating `@JsonProperty` annotated fields.

Edit point is a point where a developer has to enter something: type, name, comment, etc. Each point is invoked in order as described below for each specific template.

`|` shows the final place of the cursor.

<table>
  <tr>
    <th>Template</th><th>Description and Enter points</th><th>Example of the result</th>
  </tr>
  <tr>
    <td><code>jf</code></td>
    <td>Creates a general JSON property declaration. Suggests a field type.<br/>
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
 * Groovydoc comment.
 */
@JsonProperty( 'annotation-value' )
Type fieldName|</pre>
    </td>
  </tr>
  <tr>
      <td><code>jfi</code></td>
      <td>Creates a <code>int</code> JSON property declaration.<br/>
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
  * Groovydoc comment.
  */
 @JsonProperty( 'annotation-value' )
 int fieldName|</pre>
      </td>
    </tr>
  <tr>
      <td><code>jfl</code></td>
      <td>Creates a <code>List</code> JSON property declaration. Suggests a generic type.<br/>
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
  * Groovydoc comment.
  */
 @JsonProperty( 'annotation-value' )
 List&lt;GenericType&gt; fieldName|</pre>
      </td>
    </tr>
  <tr>
    <td><code>jfs</code></td>
    <td>Creates a <code>String</code> JSON property declaration.<br/>
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
 * Groovydoc comment.
 */
@JsonProperty( 'annotation-value' )
String fieldName|</pre>
    </td>
  </tr>
  <tr>
    <td><code>jfu</code></td>
    <td>Creates a <code>UUID</code> JSON property declaration.<br/>
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
 * Groovydoc comment.
 */
@JsonProperty( 'annotation-value' )
UUID fieldName|</pre>
    </td>
  </tr>
</table>
