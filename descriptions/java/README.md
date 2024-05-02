# Java
Describes additional live templates to the standard Java section.

Edit point is a point where a developer has to enter something: type, name, comment, etc. Each point is invoked in order as described below for each specific template.

`|` shows the final place of the cursor.

<table>
  <tr>
    <th>Template</th><th>Description and Enter points</th><th>Example of the result</th>
  </tr>
  <tr>
    <td><code>var</code></td>
    <td>Creates a variable declaration. <br/>
      Enter points:<br/>
      <ol>
        <li>Variable name</li>
        <li>Value</li>
      </ol>
    </td>
    <td><pre lang='Java'>var name = "John Doe";|</pre></td>
  </tr>
  <tr>
    <td><code>prf</code></td>
    <td>Creates a private final modifier.</td>
    <td>
      <pre lang='Java'>private final |</pre>
    </td>
  </tr>
  <tr>
      <td><code>con</code></td>
      <td>Creates a constant.<br/>
        Creates an underlined capitalized constant name based on the value.<br/>
        Enter points:<br/>
        <ol>
          <li>Value of the constant</li>
          <li>Javadoc</li>
        </ol>
      </td>
      <td>
        <pre lang='Java'>
/**
 * Javadoc.
 */
public static final String CONSTANT = "constant";
|</pre>
      </td>
  </tr>
</table>
