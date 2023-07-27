# Groovy Routine
Describes live templates which are good to use during routine code writing in Groovy.

Edit point is a point where a developer has to enter something: type, name, comment, etc. Each point is invoked in order as described below for each specific template.

`|` shows the final place of the cursor.

<table>
  <tr>
    <th>Template</th><th>Description and Enter points</th><th>Example of the result</th>
  </tr>
  <tr>
    <td><code>def</code></td>
    <td>Creates a variable declaration. <br/>
      Enter points:<br/>
      <ol>
        <li>Variable name</li>
        <li>Value</li>
      </ol>
    </td>
    <td><pre lang='Groovy'>def name = 'John Doe'|</pre></td>
  </tr>
  <tr>
      <td><code>const</code></td>
      <td>Creates a constant.<br/>
        Creates an underlined capitalized constant name based on the value.<br/>
        Enter points:<br/>
        <ol>
          <li>Value of the constant</li>
          <li>Groovydoc comment</li>
        </ol>
      </td>
      <td>
        <pre lang='Groovy'>
/**
 * Groovydoc comment.
 */
private static final String CONSTANT = 'constant'
|</pre>
      </td>
  </tr>
  <tr>
    <td><code>f</code></td>
    <td>Creates a general field declaration. Suggests a field type.<br/>
      Enter points:<br/>
      <ol>
        <li>Type</li>
        <li>Name</li>
        <li>Groovydoc comment</li>
      </ol>
    </td>
    <td>
      <pre lang='Groovy'>
/**
 * Groovydoc comment.
 */
Type fieldName
|</pre>
    </td>
  </tr>
  <tr>
    <td><code>fs</code></td>
    <td>Creates a <code>String</code> field declaration.<br/>
      Enter points:<br/>
      <ol>
        <li>Name</li>
        <li>Groovydoc comment</li>
      </ol>
    </td>
    <td>
    <pre lang='Groovy'>
/**
 * Groovydoc comment.
 */
String fieldName
|</pre>
    </td>
  </tr>
  <tr>
    <td><code>fi</code></td>
    <td>Creates an <code>int</code> field declaration.<br/>
      Enter points:<br/>
      <ol>
        <li>Name</li>
        <li>Groovydoc comment</li>
      </ol>
    </td>
    <td>
    <pre lang='Groovy'>
/**
 * Groovydoc comment.
 */
int fieldName
|</pre>
    </td>
  </tr>
</table>
